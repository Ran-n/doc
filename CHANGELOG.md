[//]: # ( ---------------------------------------------------------------------- )
[//]: # (+ Authors: 	Ran# <ran.hash@proton.me> )
[//]: # (+ Created: 	2026/05/05 19:02:30.613699 )
[//]: # (+ Revised: 	2026/05/06 18:21:49.489028 )
[//]: # ( ---------------------------------------------------------------------- )

# Changelog

All notable changes to this project are documented here.

---

## [2026-05-06]

### Added
- `README.md` — contributing section linking to CONTRIBUTING.md

### Changed
- `LICENSE` — PBL v2.0 audit fixes and score model update:
  - Clause 3: suspension-to-termination transition now requires written notice; termination is final once communicated
  - Clause 6: "constitutes a resolution" rephrased to "may pass any resolution unilaterally"
  - Clause 10: "majority ownership vote" replaced with defined term "resolution vote"
  - Clause 17: 30-day continuation window now runs from change-of-control date, not notification date; insolvency added as a change-of-control trigger
  - Clause 20: Opened field must match commit timestamp; commit timestamp governs on divergence
  - Clause 22: ballot validity condition "non-zero ownership" now explicitly measured at vote-open time
  - Clause 23: EXCUSED decrement rule for absence track added; participation penalty for Administrative Notice silence removed
  - Clause 25: silence on an Administrative Notice no longer triggers a track increment or warning file
  - Clause 26: abeyance abandonment vote now requires resolution vote; minimum 2-year wait before abandonment vote may be called
  - Clause 29: declination wording corrected (all-or-nothing per entitlement type); heir deadline now protected with 30-day minimum from date of declination; contested entitlements now have a fallback when the Founder is the deceased party
  - Clause 32: Founder-as-violator gap closed — any owner may initiate the 60-day resolution vote; AI non-disclosure added explicitly to the violation triggers
  - Clause 35: truncated sentence restored — non-response to audit request may be treated as commercial violation
  - Clause 41: AI disclosure now requires explicit identification in the submission message; non-disclosure deemed misrepresentation for clause 32 purposes
  - Clause 42: Key Rotation Window "extend" restriction aligned with definition ("beyond 24 hours")
  - Clause 44: sole-owner dormancy provision added; extended-absence review mechanism added for when a Commercial Agent is already designated
  - Definitions — Quorum: now requires at least one YES or NO ballot; votes with no substantive ballots fail quorum
  - Definitions — Absence Track: EXCUSED decrement rule added
  - Definitions — Floor / Undiluted Share: [x%] notation clarified as floor (guaranteed minimum, exempt from dilution); Undiluted Share above the floor must be explicitly noted in the CONTRIBUTORS file
  - Definitions — Governance Artifact: new definition added covering all files that form the official governance record
  - Participation score no longer stored in the CONTRIBUTORS file; tracks recorded exclusively in warning files; Absent/Abstain/Score fields removed from CONTRIBUTORS file format

### Removed
- `licenses/pbl_v2.0.md` — removed from archive; will be re-added before next version upgrade
- `voto.md` — deleted governance voting specification

### Added
- `LICENSE` / `licenses/pbl_v2.0.md` — clause 25: administrative notice
- `LICENSE` / `licenses/pbl_v2.0.md` — continued PBL v2.0 improvements:
  - Clause 3: definition of "before deploying"
  - Clause 17: change of control and acquisition handling
  - Clause 23: decrement mechanics and full reset
  - Clause 24: floor-as-stripping-floor clarification
  - Clause 29: declined successor, existing owner succession, contested entitlements
  - Clause 35: audit statement minimum required fields
  - Participation score: definition precision and reset rule
  - Absence track: mid-cycle decrement rule
  - Abstention track: mid-cycle decrement rule
  - Clauses 26–44: renumbered and all cross-references updated

---

## [2026-05-05]

### Added
- `CONTRIBUTORS` — authoritative ownership and revenue record for this project
- `CONTRIBUTING.md` — contribution guidelines
- `voto.md` — governance voting documentation
- `licenses/pbl_v2.0.md` — archived copy of PBL v2.0

### Changed
- `LICENSE` — major governance improvements to PBL v2.0:
  - Fix: Key Rotation Window clause reference corrected (39 → 40)
  - Add: `Declared Absence` definition and `EXCUSED` ballot token — no penalty for owners on declared leave
  - Add: 48-hour minimum advance notice requirement for declared absences
  - Add: `Quorum` redefined as participation requirement; `Resolution` added as the passing concept
  - Add: Founder Dormancy now based on 3+ consecutive ABSENT votes instead of months of silence
  - Add: Absence track resets to zero on any ballot including EXCUSED, for all owners
  - Add: 14-day cure window with written notice before commercial agreement suspension
  - Add: Fork succession abeyance clause for unresolved inherited ownership
  - Add: Emergency GPG key replacement process for compromised keys
  - Add: Audit right (clause 34) — owners may request revenue records from licensees once per year
  - Add: `Governance Communication` definition
  - Strengthen: Git history tampering provisions in clauses 31 and 39
- `README.md` — updated license version reference (v1.0 → v2.0)

---

## [2026-04-18]

### Added
- `LICENSE` — PayBack License (PBL) v1.0
- `licenses/` — folder for archived license versions
- `donations.md` — donation addresses (Bitcoin, Monero, Wownero)

### Changed
- `README.md` — added PBL license section and donations link

### Renamed
- `doazons.md` → `donations.md`

---

## [2022-03-20 – 2022-03-22]

### Removed
- `doazons.html` — deleted HTML donation page

---

## [2021-08-22 – 2021-10-17]

### Added
- Initial project structure
- `doazóns.md` — donation addresses (Galician)
- Code of conduct files (`coc_en.md`, `coc_cas.md`, `coc_gz.md`, `coc_eo.md`)
- `README.md`

### Removed
- `coc/` folder — code of conduct folder removed
