[//]: # ( ---------------------------------------------------------------------- )
[//]: # (+ Authors: 	Ran# <ran.hash@proton.me> )
[//]: # (+ Created: 	2026/05/05 )
[//]: # (+ Revised: 	2026/05/05 17:24:05.124698 )
[//]: # ( ---------------------------------------------------------------------- )

# Voto

CLI and GUI tool for managing PBL governance votes in a repository.

Voto handles the full lifecycle of a vote as defined by the PayBack License
(PBL) v2.0: opening a vote, casting ballots, verifying signatures, closing
the vote, applying results, and issuing warnings.

---

## Overview

A Voto-managed repository contains a `governance/` folder at the root:

```
governance/
  votes/
    <YYYY-MM-DD>_<slug>/
      <YYYY-MM-DD>_<slug>.vote
      CONTRIBUTORS.proposed         (only if vote modifies CONTRIBUTORS)
      <fingerprint>.ballot
      <fingerprint>.sig
      ...
  warnings/
    <YYYY-MM-DD>_warning-<absent|abstain>-<pseudonym>.warn
```

---

## Commands

### `voto open <slug> [--deadline <YYYY-MM-DD>]`

Opens a new vote.

- Creates `governance/votes/<YYYY-MM-DD>_<slug>/`
- Creates `<YYYY-MM-DD>_<slug>.vote` with:
  - Description prompt (user input)
  - Opened date (today)
  - Deadline (default: 7 days from today, minimum 48 hours)
  - Files section (empty until files are attached)
  - Ownership snapshot (read from current CONTRIBUTORS)
  - Ballots section with `—` for each owner
- Stages the new folder for commit

### `voto attach <vote-slug> <file>`

Attaches a file to an open vote.

- Copies the file into the vote folder
- Computes its BLAKE3 hash
- Adds it to the Files section of the `.vote` file
- If the file is `CONTRIBUTORS.proposed`, validates its format

### `voto cast <vote-slug> <YES|NO|ABSTAIN>`

Casts the current user's ballot on an open vote.

- Identifies the user by their GPG key (must match a CONTRIBUTORS entry)
- Creates `<fingerprint>.ballot` with:
  - Pseudonym
  - Vote (YES, NO, or ABSTAIN)
  - Vote-on (slug)
  - Vote-hash (BLAKE3 hash of the .vote file at cast time)
  - Timestamp (UTC timestamp of when the ballot was cast)
- Signs the ballot with the user's GPG key, producing `<fingerprint>.sig`
- Updates the BALLOTS section of the `.vote` file
- Stages all three changes for commit

### `voto status <vote-slug>`

Shows the current state of a vote.

- Lists all ballots cast so far
- Shows outstanding (—) ballots
- Shows current yes vs no count (abstentions excluded)
- Shows whether the voting window is still open
- Shows whether any threshold has been reached

### `voto verify <vote-slug>`

Verifies all ballots in a vote folder.

- For each `<fingerprint>.ballot` + `<fingerprint>.sig` pair:
  - Verifies the GPG signature against the ballot file
  - Confirms the fingerprint matches the GPG field in CONTRIBUTORS
  - Confirms the pseudonym matches the CONTRIBUTORS entry
  - Confirms the owner held non-zero ownership at vote open time
  - Confirms the Vote-hash matches the BLAKE3 hash of the .vote file as
    it existed when the ballot was cast
- Reports any invalid or missing ballots

### `voto close <vote-slug>`

Closes a vote after the deadline has passed or all owners have voted.

- Runs `voto verify` first; aborts if any signature is invalid
- Counts yes vs no (abstentions excluded)
- Marks any remaining `—` ballots as ABSENT in the `.vote` file
- Records the result (PASSED or FAILED) in the `.vote` file
- If PASSED and `CONTRIBUTORS.proposed` is present:
  - Verifies BLAKE3 hash of `CONTRIBUTORS.proposed` matches the Files entry
  - Replaces `CONTRIBUTORS` with `CONTRIBUTORS.proposed`
- Automatically issues warnings for any ABSENT or ABSTAIN ballots:
  - Creates `governance/warnings/<YYYY-MM-DD>_warning-<absent|abstain>-<pseudonym>.warn`
  - Updates the Absent, Abstain, and Score fields in CONTRIBUTORS for each affected owner
- Stages all changes for commit

### `voto warn <pseudonym> <absent|abstain> <vote-slug>`

Manually issues a warning to an owner. Called automatically by `voto close`
but can be used directly if a warning needs to be issued outside of that flow.

- Creates `governance/warnings/<YYYY-MM-DD>_warning-<absent|abstain>-<pseudonym>.warn`
- The warning file contains:
  - Pseudonym
  - Reason (absent or abstain)
  - Vote slug
  - Current absence track, abstention track, and participation score
    after incrementing
- Updates the Absent, Abstain, and Score fields in CONTRIBUTORS for that owner
- Stages changes for commit

### `voto flags`

Lists all owners who have reached a stripping threshold.

- Reads all warning files from `governance/warnings/`
- Computes current absence track, abstention track, and participation score
  per owner
- Reports owners where:
  - Absence track ≥ 2, or
  - Abstention track ≥ 4, or
  - Participation score ≥ 3
- Does not take any action — informational only

---

## Ballot Format

```
Pseudonym  <pseudonym>
Vote       <YES | NO | ABSTAIN>
Vote-on    <YYYY-MM-DD>_<slug>
Vote-hash  <BLAKE3 hash of the .vote file at cast time>
Timestamp  <YYYY-MM-DD HH:MM:SS UTC>
```

---

## Vote File Format

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 VOTE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

 <description>

─────────────────────────────────────────────────────────────────────────────
 METADATA
─────────────────────────────────────────────────────────────────────────────

 Opened    <YYYY-MM-DD HH:MM:SS UTC>
 Deadline  <YYYY-MM-DD HH:MM:SS UTC>

 Files
   <filename>   <BLAKE3 hash>
   ...

─────────────────────────────────────────────────────────────────────────────
 OWNERSHIP SNAPSHOT
─────────────────────────────────────────────────────────────────────────────

 <Pseudonym>   <ownership %>
 ...

─────────────────────────────────────────────────────────────────────────────
 BALLOTS
─────────────────────────────────────────────────────────────────────────────

 <Pseudonym>   <YES | NO | ABSTAIN | ABSENT | —>
 ...

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Rules

- All file hashes use BLAKE3
- All signatures use GPG detached armored signatures
- The `.vote` file is a living document — updated as ballots are cast, never signed
- The `.ballot` + `.sig` pair is the cryptographic proof of each vote
- A vote passes when yes votes exceed no votes (abstentions excluded)
- The voting window default is 7 days, minimum 48 hours
- CONTRIBUTORS may only be updated after a passed vote; all artifacts must be committed alongside it
- Stripping thresholds are prerequisites for calling a stripping vote, not automatic triggers

---

## Notes

- Voto does not push to remote — the user commits and pushes manually
- Voto requires GPG and b3sum to be installed
- The user's GPG key must match the fingerprint in their CONTRIBUTORS entry
- GUI is a future goal; CLI is the initial target
