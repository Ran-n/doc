PayBack License (PBL)
Version 2.0

Copyright (c) 2026 Ran#  <ran.hash@proton.me>

─────────────────────────────────────────────────────────────────────────────
PREAMBLE
─────────────────────────────────────────────────────────────────────────────

This software is free for people. It is not free for profit.

If you use this work — or any modified, extended, or derived version of it —
to generate revenue, you owe a share of that revenue to the people who built
it. This applies regardless of how much the code was changed. If this work
is in the chain, its authors are in the chain.

─────────────────────────────────────────────────────────────────────────────
DEFINITIONS
─────────────────────────────────────────────────────────────────────────────

"Founder"
    The original author of the project, as identified in the CONTRIBUTORS
    file. The Founder holds 100% of ownership rights unless explicitly
    relinquished under the terms of this license. The Founder may operate
    under a pseudonym; their legal identity is recorded in the CONTRIBUTORS
    file under the Name field and may be disclosed to establish authorship
    in legal proceedings.

"Contributor"
    Any person who has made a meaningful contribution — defined as
    implementing features, fixing bugs, or making non-trivial code changes —
    and who is listed in the CONTRIBUTORS file.

"Meaningful Contribution"
    A contribution of features, fixes, or substantive code changes. Changes
    limited to documentation, formatting, or comments do not qualify.

"Ownership"
    The right to make decisions about the project, including merging
    contributions, changing the license, and transferring ownership. Ownership
    is expressed as a percentage and grants proportional voting rights and
    proportional patent holdings. Ownership is separate from revenue share.

"Revenue Share"
    The portion of commercial revenue a party is entitled to receive under a
    commercial agreement. Defined per contributor in the CONTRIBUTORS file.

"Patent Holdings"
    The proportional stake in any patents covering the software, held in
    accordance with ownership percentage. Patent holdings follow ownership
    changes automatically.

"Floor"
    A minimum percentage of ownership or revenue that is guaranteed to a
    party and cannot be diluted by the addition of new contributors. Floors
    are recorded in the CONTRIBUTORS file using the [x%] notation.

"Undiluted Share"
    A revenue share or ownership percentage that is locked and exempt from
    dilution when new contributors are added. Recorded explicitly in the
    CONTRIBUTORS file.

"Dilutable Share"
    A revenue share or ownership percentage that is reduced proportionally
    when new contributors are added to the distributable pool.

"Distributable Pool (Revenue)"
    The portion of revenue available for distribution among contributors.
    Calculated as: 100% minus the Founder's revenue floor, minus the sum
    of all undiluted revenue shares.

"Distributable Pool (Ownership)"
    The portion of ownership available for distribution among contributors.
    Calculated as: 100% minus the Founder's ownership floor, minus the sum
    of all undiluted ownership shares.

"Quorum"
    A vote that passes when yes votes exceed no votes among all ownership
    holders, with abstentions excluded from the count. All ownership holders
    must cast a ballot (YES, NO, or ABSTAIN) within the voting window. Owners
    who fail to cast a ballot before the deadline are automatically marked
    ABSENT — ABSENT is recorded by the system, not cast by the owner.

"Voting Window"
    The period during which owners must cast their ballot. The default
    window is 7 days. The proposer may extend it but not shorten it below
    48 hours. The window opens when the vote record file is committed to
    the repository.

"Absence Track"
    A per-owner counter tracking votes where the owner was marked ABSENT.
    Resets to zero after a stripping vote resolves. A stripping vote may be
    called against an owner once their absence track reaches 2.

"Abstention Track"
    A per-owner counter tracking votes where the owner voted ABSTAIN.
    Resets to zero after a stripping vote resolves. A stripping vote may be
    called against an owner once their abstention track reaches 4.

"Participation Score"
    A combined score calculated as: (absence track × 2) + abstention track.
    A stripping vote may be called against an owner once their participation
    score reaches 3, independent of the individual track thresholds.

─────────────────────────────────────────────────────────────────────────────
PERMISSIONS
─────────────────────────────────────────────────────────────────────────────

You are free to:

  - Use this software for personal, academic, or non-commercial purposes
  - Study, copy, and modify the source code
  - Distribute original or modified versions, provided this license is kept
    intact and all authors listed in CONTRIBUTORS are credited

─────────────────────────────────────────────────────────────────────────────
CONDITIONS
─────────────────────────────────────────────────────────────────────────────

1. ATTRIBUTION
   All distributions — original or modified — must retain this license and
   credit all authors listed in the CONTRIBUTORS file.

2. SHARE-ALIKE
   Any modified or derived version must be released under this same license
   (PBL v2.0 or later).

3. COMMERCIAL USE REQUIRES AGREEMENT
   "Commercial use" means any use where this software, or a derivative of it,
   directly or indirectly contributes to generating revenue. This includes
   but is not limited to:

     - Selling the software or a product that includes it
     - Using it in a paid service, SaaS, or subscription product
     - Using it internally in a for-profit business to reduce costs or
       increase output
     - Incorporating it into a larger product that is sold or monetized

   If your use is commercial, you must contact the Founder before deploying
   and negotiate a revenue-share agreement. No fixed percentage is set here —
   terms are agreed between parties. Operating commercially without an
   agreement is a violation of this license.

─────────────────────────────────────────────────────────────────────────────
OWNERSHIP
─────────────────────────────────────────────────────────────────────────────

4. COPYRIGHT
   Copyright remains solely with the Founder regardless of the number or
   significance of contributions made by others. Contributing to this project
   does not transfer, share, or diminish the Founder's copyright.

5. PSEUDONYMITY
   Authors and contributors may operate under a pseudonym. The use of a
   pseudonym does not affect the validity of copyright, ownership, or revenue
   entitlements established under this license. Legal names are recorded
   privately in the CONTRIBUTORS file under the Name field and may be
   disclosed solely for the purpose of establishing identity in legal
   proceedings. No party is required to disclose their legal identity
   publicly.

6. OWNERSHIP PERCENTAGE
   Ownership is tracked in the CONTRIBUTORS file. The Founder begins at 100%
   ownership. Ownership may be transferred to a contributor only via quorum
   vote and the governance process defined in clauses 19–24. Relinquished
   ownership dilutes all existing dilutable ownership shares evenly, drawn
   from the distributable ownership pool. Since the Founder holds 100%
   ownership by default, the Founder constitutes quorum unilaterally until
   ownership is shared.

7. FOUNDER OWNERSHIP FLOOR
   The Founder is guaranteed a minimum ownership of 30% at all times. This
   is the default floor. The floor cannot be diluted by the addition of
   contributors. It ensures the Founder retains meaningful voting power
   regardless of how much ownership is shared. The floor may be changed
   only by quorum vote, and the new value must be recorded in the
   CONTRIBUTORS file.

8. VOTING
   All project decisions are governed by a vote among ownership holders.
   Any owner may call a vote. A vote passes when yes votes exceed no votes
   after all ballots are cast or the voting window expires. Abstentions are
   excluded from the count. All votes must be recorded and verified via
   the governance process defined in clauses 19–22. Since the Founder holds
   100% ownership by default, the Founder constitutes quorum unilaterally
   until ownership is shared.

   Ballot options:
     YES         — in favour of the proposed change
     NO          — against the proposed change
     ABSTAIN     — present but not counted on either side
     ABSENT      — did not vote before the deadline; recorded automatically

─────────────────────────────────────────────────────────────────────────────
PATENTS
─────────────────────────────────────────────────────────────────────────────

9. PATENT OWNERSHIP
   Patents covering the software are held proportionally to ownership
   percentage as recorded in the CONTRIBUTORS file. By submitting a
   contribution, the contributor irrevocably assigns to the existing
   ownership pool all patent rights in their contribution, distributed
   proportionally among current owners. Patent holdings follow ownership
   changes automatically — when ownership is transferred via quorum vote,
   patent holdings adjust accordingly.

10. PATENT LICENSE TO USERS
    Owners grant all users a non-exclusive, worldwide, royalty-free patent
    license to use the software for non-commercial purposes only, to the
    extent of their patent holdings. No patent license is granted for
    commercial use beyond what is negotiated in a commercial agreement.
    Enforcement of any patent covering this software requires a majority
    ownership vote.

11. NO SUBLICENSING OF PATENTS
    Patent licenses granted under this license are personal and
    non-transferable. No party may sublicense, assign, or transfer their
    patent rights or patent license to any third party without a quorum vote.

─────────────────────────────────────────────────────────────────────────────
REVENUE SHARE
─────────────────────────────────────────────────────────────────────────────

12. FOUNDER REVENUE FLOOR
    The Founder is guaranteed a minimum revenue share of 30% on every
    commercial agreement. This is the default floor. The floor cannot be
    diluted by the addition of contributors. The floor may be changed only
    by quorum vote, and the new value must be recorded in the CONTRIBUTORS
    file.

13. CONTRIBUTOR REVENUE SHARE
    Contributors listed in the CONTRIBUTORS file are entitled to a share of
    commercial revenue as recorded therein. A contributor's share takes
    effect only upon being listed in the CONTRIBUTORS file. Listing always
    requires a quorum vote following a meaningful contribution. A
    contributor's share may be dilutable or undiluted, and may include a
    floor, as determined by the quorum vote at the time of listing. Since
    the Founder holds 100% ownership by default, the Founder constitutes
    quorum unilaterally until ownership is shared.

14. REVENUE DILUTION
    When a new contributor is added to the distributable revenue pool, their
    share is drawn evenly from all existing dilutable revenue shares — the
    Founder's revenue above their floor and all non-undiluted contributor
    shares — reducing each proportionally. Undiluted shares and floors are
    exempt from this reduction.

15. OWNERSHIP DILUTION
    When ownership is transferred to a contributor via quorum vote, the
    transferred percentage is drawn evenly from all existing dilutable
    ownership shares — the Founder's ownership above their floor and all
    non-undiluted contributor ownership shares — reducing each
    proportionally. Undiluted ownership shares and floors are exempt from
    this reduction.

16. CONTRIBUTOR FLOORS AND UNDILUTED SHARES
    A quorum vote may grant any contributor a floor and/or an undiluted
    share on their revenue, ownership, or both, as recognition of
    exceptional or significant contribution. All such grants must be
    recorded explicitly in the CONTRIBUTORS file and verified via the
    governance process defined in clauses 19–22. Floors and undiluted shares
    granted to contributors follow the same mechanics as the Founder's
    floor: exempt from dilution, recorded with the [x%] notation. Since the
    Founder holds 100% ownership by default, the Founder constitutes quorum
    unilaterally until ownership is shared.

17. NO SUBLICENSING
    Commercial agreements are personal and non-transferable. A commercial
    licensee may not sublicense, resell, assign, or transfer their commercial
    agreement or any rights granted thereunder to any third party. Any
    attempted sublicense or transfer is void and constitutes a violation of
    this license.

─────────────────────────────────────────────────────────────────────────────
CONTRIBUTORS FILE
─────────────────────────────────────────────────────────────────────────────

18. CONTRIBUTORS FILE
    Every project under this license must maintain a CONTRIBUTORS file at the
    root of the repository. This file is the authoritative record of
    ownership percentages, revenue shares, patent holdings, floors, undiluted
    status, participation tracking, and succession. Its format is defined in
    this license and must be followed exactly.

    The CONTRIBUTORS file format is:

    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
     CONTRIBUTORS
    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

     Authoritative record of ownership and revenue shares for this project.
     Governed by the PayBack License (PBL) v2.0.

    ──────────────────────────────────────────────────────────────────────────
     LEGEND
    ──────────────────────────────────────────────────────────────────────────

     ⁕     founder
     [x%]  undiluted floor

    ──────────────────────────────────────────────────────────────────────────
     SUMMARY                                    OWNERSHIP    REVENUE
    ──────────────────────────────────────────────────────────────────────────

     ⁕ Founder Pseudonym                        100% [30%]   100% [30%]
       Contributor Pseudonym                       0%          12% [8%]
       Contributor Pseudonym                       0%           8%

    ──────────────────────────────────────────────────────────────────────────
     DETAILS
    ──────────────────────────────────────────────────────────────────────────

     ⁕ Founder Pseudonym
       Pseudonym            Founder Pseudonym
       Name                 Legal Name
       Role                 Founder
       Email                founder@example.com
       GPG                  AABB CCDD EEFF 0011 2233 4455 6677 8899 AABB CCDD
       Ownership            100% [30%]
       Revenue              100% [30%]
       Absent               0
       Abstain              0
       Score                0
       Successor-Ownership  (optional)
       Successor-Revenue    (optional)

       Contributor Pseudonym
       Pseudonym            Contributor Pseudonym
       Name                 Legal Name
       Role                 Contributor
       Email                contrib@example.com
       GPG                  1122 3344 5566 7788 99AA BBCC DDEE FF00 1122 3344
       Ownership              0%
       Revenue               12% [8%]
       Absent                 0
       Abstain                0
       Score                  0
       Successor-Revenue    (optional)

    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

    Field definitions:

      ⁕           Founder marker
      [x%]        Undiluted floor — this share cannot be diluted by new
                  contributors
      SUMMARY     Quick-reference table of all ownership and revenue shares
      DETAILS     Full entry per contributor with contact and GPG key
      Pseudonym   Public identity used in authorship, attribution, and
                  project artifacts; may differ from the legal name
      Name        Full legal name; used to establish identity in legal
                  proceedings; may differ from the pseudonym
      Role        Founder or Contributor
      Email       Contact address
      GPG         Full GPG key fingerprint used to sign ballots
      Ownership   Current ownership percentage granting voting rights and
                  proportional patent holdings; total must equal 100%;
                  bracketed value is the floor
      Revenue     Current revenue share percentage; all values are resolved
                  — no dynamic placeholders; bracketed value is the floor
      Absent      Current absence track count; resets after a stripping vote
      Abstain     Current abstention track count; resets after a stripping vote
      Score       Current participation score: (Absent × 2) + Abstain
      Successor-Ownership  Present only if the holder has a non-zero ownership
                           percentage. Optional; pseudonym or legal name of the
                           person who inherits the ownership stake upon death or
                           permanent incapacitation. If blank, the ownership
                           stake passes to the holder's legal heirs.
      Successor-Revenue    Present only if the holder has a non-zero revenue
                           share. Optional; pseudonym or legal name of the
                           person who inherits the revenue share upon death or
                           permanent incapacitation. If blank, the revenue share
                           passes to the holder's legal heirs. May name a
                           different person than Successor-Ownership.

─────────────────────────────────────────────────────────────────────────────
GOVERNANCE
─────────────────────────────────────────────────────────────────────────────

19. GOVERNANCE STRUCTURE
    The reference implementation for managing governance artifacts is Voto,
    a CLI and GUI tool that automates the creation, signing, verification,
    and closing of votes. Its use is recommended but not required.
    All governance artifacts are stored in the governance/ folder at the
    root of the repository, organised as follows:

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

20. VOTE RECORD FORMAT
    All project votes must be recorded as a vote record file, regardless
    of whether they modify the CONTRIBUTORS file.

    Each vote must concern exactly one subject. Bundling multiple unrelated
    decisions into a single vote is not permitted. The only permitted exception
    is a combined ownership-and-revenue stripping vote under clause 24, where
    both are explicitly stated in the vote description and the vote slug.

    The slug must be a concise, descriptive, kebab-case phrase that
    unambiguously identifies the subject and outcome of the vote, such that
    the filename alone conveys the nature of the decision to an uninformed
    reader (e.g. add-jane-doe-as-contributor,
    change-founder-revenue-floor-to-40pct,
    approve-commercial-agreement-with-acme).

    The vote record file is a living document — it is updated each time
    an owner casts their ballot. It is never directly signed. The
    cryptographic proof of each ballot is the corresponding .ballot and
    .sig file pair. The vote record must follow this format:

    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
     VOTE
    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

     <description of the decision — the headline of the vote>

    ──────────────────────────────────────────────────────────────────────
     METADATA
    ──────────────────────────────────────────────────────────────────────

     Opened    <YYYY-MM-DD>
     Deadline  <YYYY-MM-DD>

     Files
       <filename>   <BLAKE3 hash>
       ...

    ──────────────────────────────────────────────────────────────────────
     OWNERSHIP SNAPSHOT
    ──────────────────────────────────────────────────────────────────────

     <Pseudonym>   <ownership %>
     ...

    ──────────────────────────────────────────────────────────────────────
     BALLOTS
    ──────────────────────────────────────────────────────────────────────

     <Pseudonym>   <YES | NO | ABSTAIN | ABSENT | —>
     ...

    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

    The Files section lists every file relevant to the vote that must be
    present in the vote folder. Each file is listed with its BLAKE3 hash
    so that any party can verify the exact content that was voted on.
    For votes that modify CONTRIBUTORS, CONTRIBUTORS.proposed must be
    listed. The Files section may be omitted for votes with no associated
    files. The — symbol in BALLOTS indicates a ballot not yet cast.

21. BALLOT FORMAT
    Each owner casts their vote by creating a ballot file containing their
    pseudonym, their vote, the vote slug, and the date of their ballot:

      Pseudonym  <pseudonym>
      Vote       <YES | NO | ABSTAIN>
      Vote-on    <YYYY-MM-DD>_<slug>
      Date       <YYYY-MM-DD>

    The ballot file is stored as:
      governance/votes/<YYYY-MM-DD>_<slug>/<fingerprint>.ballot
    The owner then produces a detached GPG signature of their ballot file,
    stored as:
      governance/votes/<YYYY-MM-DD>_<slug>/<fingerprint>.sig
    After committing their ballot and signature, the owner also updates the
    BALLOTS section of the .vote file to reflect their vote and commits it.

22. VERIFICATION
    A vote passes when yes votes exceed no votes after all owners have
    voted or the voting window has expired. Abstentions are excluded from
    the count. A ballot is valid when:
      - The .sig file verifies against the corresponding .ballot file
      - The signing key fingerprint matches the GPG field of the owner's
        entry in the CONTRIBUTORS file at the time of the vote
      - The pseudonym in the .ballot file matches the owner's CONTRIBUTORS
        entry
      - The owner holds a non-zero ownership percentage
    The CONTRIBUTORS file may only be updated after the vote passes and
    all artifacts are committed to the repository alongside it.

23. ABSENCE AND ABSTENTION TRACKING
    After each vote, if an owner is marked ABSENT or ABSTAIN, their
    respective track is incremented and a warning file is created at:
      governance/warnings/<YYYY-MM-DD>_warning-<absent|abstain>-<pseudonym>.warn

    The warning file must follow this format:

      Pseudonym  <pseudonym>
      Reason     <absent | abstain>
      Vote       <YYYY-MM-DD>_<slug>
      Absent     <absence track after incrementing>
      Abstain    <abstention track after incrementing>
      Score      <participation score after incrementing>

    The CONTRIBUTORS file must be updated to reflect the new Absent,
    Abstain, and Score values for the affected owner.

    Track thresholds — any of the following enables a stripping vote to
    be called; none of them mandate it:
      - Absence track reaches 2
      - Abstention track reaches 4
      - Participation score reaches 3

    Thresholds are prerequisites for calling a stripping vote, not
    automatic triggers. No action is required until an owner chooses to
    call one. Both tracks and the participation score reset to zero after
    a stripping vote resolves, regardless of outcome.

24. OWNERSHIP STRIPPING
    Once any threshold defined in clause 23 is reached, any owner may
    call a vote to strip or reduce the flagged owner's ownership.

    A stripping vote concerns ownership only by default. Revenue share is
    not affected unless the vote explicitly states that both ownership and
    revenue are being stripped, in which case the single vote may cover
    both as a permitted exception under clause 20. A vote to strip revenue
    alone, without stripping ownership, may also be called as a separate
    vote — it does not require the ownership stripping thresholds to be met.

    If the stripping vote passes, the flagged owner's ownership is
    redistributed evenly among all remaining owners via the standard
    dilution mechanics. If revenue is also stripped, the flagged owner's
    revenue share is likewise redistributed evenly among all remaining
    contributors via the standard dilution mechanics.

    The stripped owner may earn ownership again through meaningful
    contribution and a subsequent quorum vote, as with any new contributor.

─────────────────────────────────────────────────────────────────────────────
FORKS AND DERIVATIVES
─────────────────────────────────────────────────────────────────────────────

25. FORK REQUIREMENTS
    Any fork or derivative of this software must be released under this same
    license (PBL v2.0 or later). The original Founder's ownership and revenue
    floors as recorded in the original project's CONTRIBUTORS file at the
    time of the fork carry over unchanged into the fork's CONTRIBUTORS file.
    The forker may not reduce or remove the original Founder's floors. Any
    person wishing to be listed as a contributor in a fork must be added via
    a quorum vote in the fork, subject to the same governance process as the
    original project. Any changes to the original Founder's floors in the
    fork require a quorum vote among the fork's ownership holders.

    At the moment of forking, the fork's ownership holders and their
    respective percentages are identical to those of the original project's
    CONTRIBUTORS file at the time of the fork. The forker does not
    automatically acquire any ownership in the fork by virtue of forking.
    Any person — including the forker — who wishes to be listed as an owner
    in the fork must be approved via a quorum vote among the fork's inherited
    ownership holders. Until such a vote occurs, quorum in the fork is
    constituted by the same ownership holders and percentages carried over
    from the original project.

─────────────────────────────────────────────────────────────────────────────
TRADEMARKS
─────────────────────────────────────────────────────────────────────────────

26. NO TRADEMARK GRANT
    This license does not grant any rights to use the Founder's name,
    pseudonym, project name, logos, or any associated marks, whether
    registered or unregistered. No such rights are implied by the terms
    of this license.

27. FORK NAMING RESTRICTION
    A fork of this software may not use the original project's name, or any
    name confusingly similar to it, or present itself as the official version
    of the original project, without written permission granted by a majority
    ownership vote of the original project's ownership holders.

─────────────────────────────────────────────────────────────────────────────
SUCCESSION
─────────────────────────────────────────────────────────────────────────────

28. SUCCESSION
    Ownership and revenue share are heritable independently. Any holder may
    designate separate successors for each via the Successor-Ownership and
    Successor-Revenue fields in the CONTRIBUTORS file. The
    Successor-Ownership field is present only for holders with a non-zero
    ownership percentage; the Successor-Revenue field is present only for
    holders with a non-zero revenue share. Both fields are optional.

    Upon the death or permanent incapacitation of a holder:
      - Their ownership percentage and patent holdings pass to their
        designated Successor-Ownership. If no Successor-Ownership is named,
        ownership passes to their legal heirs in accordance with applicable
        inheritance law.
      - Their revenue share passes to their designated Successor-Revenue.
        If no Successor-Revenue is named, the revenue share passes to their
        legal heirs in accordance with applicable inheritance law.

    Successor-Ownership and Successor-Revenue may name different people.
    A holder's legal heirs receive only what the holder did not explicitly
    designate to a named successor.

    The successor or heirs must notify the remaining ownership holders and
    update the CONTRIBUTORS file via the standard governance process.

─────────────────────────────────────────────────────────────────────────────
LICENSE VERSIONING
─────────────────────────────────────────────────────────────────────────────

29. VERSION PINNING
    Each project is governed by the version of the PBL under which it was
    released. A newer version of the PBL does not automatically apply to
    projects released under an older version. Previous distributions of a
    project remain governed by the version of the license under which they
    were made, even if the project subsequently upgrades to a newer version.
    Upgrading a project to a newer PBL version requires a quorum vote and
    applies only to distributions made after the upgrade.

─────────────────────────────────────────────────────────────────────────────
CONTRIBUTOR AGREEMENT
─────────────────────────────────────────────────────────────────────────────

30. CONTRIBUTION WARRANTY
    By submitting a contribution to this project — whether via pull request,
    patch, or any other means — the contributor warrants that:
      a) The contribution is their original work and they have the right to
         submit it under the terms of this license.
      b) The contribution does not knowingly infringe any third-party
         copyright, patent, trademark, or other intellectual property right.
      c) They irrevocably assign all patent rights in their contribution to
         the existing ownership pool, distributed proportionally among current
         owners in accordance with clause 9.
      d) They accept the terms of this license in full, including the
         commercial use and revenue share clauses.
    Submission of a contribution constitutes acceptance of these terms
    without requiring a separate signed agreement.

31. CONTRIBUTOR TERMINATION
    If a contributor violates any term of this license — including but not
    limited to submitting contributions that infringe third-party rights,
    misrepresenting authorship, or engaging in bad-faith governance — all
    rights granted to that contributor under this license terminate
    immediately and permanently. Revenue share and ownership entitlements
    recorded in the CONTRIBUTORS file are suspended pending resolution. The
    Founder may initiate a quorum vote to formally remove the contributor
    and redistribute their shares.

    "Bad-faith governance" includes, without limitation, any of the
    following acts:

      a) Forging or tampering with a ballot file or signature, or casting
         a ballot under a key that is not the contributor's own as recorded
         in the CONTRIBUTORS file.

      b) Casting a ballot while knowing that the GPG key used has been
         compromised, without first disclosing the compromise to the other
         ownership holders.

      c) Deliberately manipulating the voting window — including extending
         it without cause, or committing a vote record with a fabricated
         open or deadline date — to influence the outcome of a vote.

      d) Calling votes repetitively and without legitimate purpose with
         the intent to exhaust, harass, or coerce other ownership holders.

      e) Committing changes to the CONTRIBUTORS file outside the governance
         process defined in clauses 19–22, or altering any governance
         artifact after it has been committed.

      f) Misrepresenting the subject or scope of a vote in the vote record
         or slug in order to obtain approval for a decision that would not
         have passed under its true description.

      g) Deliberately failing to record an ABSENT status, a warning file,
         or a participation track increment after a vote, with the intent
         of shielding an owner from a stripping vote.

      h) Coordinating with a third party outside the governance process to
         acquire, transfer, or exercise ownership or revenue rights in
         circumvention of a quorum vote.

    This list is illustrative, not exhaustive. Any act whose evident purpose
    is to corrupt, circumvent, or weaponise the governance process constitutes
    bad-faith governance under this clause.

─────────────────────────────────────────────────────────────────────────────
ENFORCEMENT
─────────────────────────────────────────────────────────────────────────────

32. COMMERCIAL VIOLATION
    Violation of the commercial clause — including use without an agreement,
    deliberate obfuscation of the software's presence in a product, or
    relabeling to avoid attribution — revokes all rights granted by this
    license immediately and permanently. The Founder reserves the right to
    pursue compensation for unlicensed commercial use retroactively.

33. NO REVENUE THRESHOLD
    There is no minimum revenue threshold for the commercial use requirement.
    Any use that generates revenue — regardless of amount — constitutes
    commercial use and requires a prior agreement with the Founder. There
    are no exemptions based on revenue size, project scale, or intent.

34. WAIVER
    Failure by the Founder or any rights holder to enforce any provision of
    this license at any time does not constitute a waiver of the right to
    enforce that provision in the future. No waiver of any breach shall be
    construed as a waiver of any subsequent breach.

35. SEVERABILITY
    If any provision of this license is found to be invalid, illegal, or
    unenforceable by a court of competent jurisdiction, that provision shall
    be modified to the minimum extent necessary to make it enforceable, or
    severed if modification is not possible. The remaining provisions of this
    license shall continue in full force and effect.

36. GOVERNING LAW AND JURISDICTION
    This license shall be governed by and construed in accordance with the
    laws of Spain. The copyright protections granted by this license extend
    to all jurisdictions that are signatories to the Berne Convention for
    the Protection of Literary and Artistic Works, as amended, and to any
    other applicable international copyright treaty. The Founder reserves
    the right to enforce this license and pursue remedies in any jurisdiction
    where a violation occurs or where the violator operates or holds assets,
    without waiving the right to pursue remedies in any other jurisdiction.
    Parties who cannot resolve a dispute through good-faith negotiation agree
    to submit to binding arbitration under the WIPO Arbitration Rules before
    resorting to litigation.

─────────────────────────────────────────────────────────────────────────────
SIGNATURES AND LEGAL WEIGHT
─────────────────────────────────────────────────────────────────────────────

37. GPG SIGNATURES AS CONSENT
    A GPG-signed ballot, as defined in clause 21, constitutes a binding
    expression of consent by the signing party under this license. By
    signing a ballot, the signing party confirms they have read, understood,
    and agree to be bound by the decision being voted on. GPG signatures
    produced in accordance with this license are intended to carry the same
    legal weight as a digital signature under applicable electronic signature
    law, including but not limited to the eIDAS Regulation (EU) 910/2014.

38. CONTRIBUTORS FILE AS RECORD
    The CONTRIBUTORS file, maintained in accordance with clause 18 and
    amended only through the governance process defined in clauses 19–22,
    constitutes the authoritative record of ownership and revenue
    entitlements under this license. Parties listed therein are bound by
    its contents. Changes made outside the defined governance process have
    no legal effect.

─────────────────────────────────────────────────────────────────────────────
DISCLAIMER
─────────────────────────────────────────────────────────────────────────────

THIS SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE, TITLE, AND NON-INFRINGEMENT. THE AUTHORS
AND OWNERSHIP HOLDERS DO NOT WARRANT THAT THE SOFTWARE IS ERROR-FREE, THAT
DEFECTS WILL BE CORRECTED, OR THAT THE SOFTWARE IS FREE OF VIRUSES OR OTHER
HARMFUL COMPONENTS.

TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, IN NO EVENT SHALL THE
AUTHORS, OWNERSHIP HOLDERS, CONTRIBUTORS, OR ANY PARTY INVOLVED IN THE
CREATION, PRODUCTION, OR DISTRIBUTION OF THIS SOFTWARE BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, PUNITIVE, OR CONSEQUENTIAL
DAMAGES WHATSOEVER, INCLUDING BUT NOT LIMITED TO:

  - LOSS OF PROFITS, REVENUE, DATA, GOODWILL, OR ANTICIPATED SAVINGS
  - LOSS OF BUSINESS OR CONTRACTS
  - BUSINESS INTERRUPTION
  - PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES
  - PERSONAL INJURY OR PROPERTY DAMAGE
  - ANY OTHER PECUNIARY OR NON-PECUNIARY LOSS

ARISING OUT OF OR IN CONNECTION WITH THE USE OR INABILITY TO USE THIS
SOFTWARE, HOWEVER CAUSED AND UNDER ANY THEORY OF LIABILITY — WHETHER IN
CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) —
EVEN IF THE AUTHORS HAVE BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

THIS LIMITATION OF LIABILITY APPLIES TO THE FULLEST EXTENT PERMITTED BY
LAW IN THE APPLICABLE JURISDICTION. SOME JURISDICTIONS DO NOT ALLOW THE
EXCLUSION OR LIMITATION OF CERTAIN DAMAGES; IN SUCH JURISDICTIONS, LIABILITY
IS LIMITED TO THE MINIMUM EXTENT REQUIRED BY LAW.

─────────────────────────────────────────────────────────────────────────────
CONTACT
─────────────────────────────────────────────────────────────────────────────

To obtain a commercial license:  ran.hash@proton.me
