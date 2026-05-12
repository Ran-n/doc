[//]: # ( ---------------------------------------------------------------------- )
[//]: # (+ Authors: 	Ran# <ran.hash@proton.me> )
[//]: # (+ Created: 	2026/05/05 19:02:30.613699 )
[//]: # (+ Revised: 	2026/05/12 00:00:00.000000 )
[//]: # ( ---------------------------------------------------------------------- )

# Changelog

All notable changes to this project are documented here.

---

## [2026-05-12]

### Changed
- `LICENSE` — PBL v2.0 round 5: governance hardening, new clauses, and clause renumbering — 25 fixes:
  - **Cross-reference corrections:** AI-Generated Portion disclosure now points to clause 43 (was 41); Key Rotation Window now points to clause 44 (was 42); Commercial Agent mechanics now point to clause 45 (was 43); Founder Dormancy removal now points to clause 44 (was 42); AI Contributions section heading updated throughout
  - **Commercial Agent (Definitions + cl.45):** Agent may not modify license terms, transfer ownership, or alter revenue shares; unilateral designation by Founder permitted before ownership is shared; mechanics of designation and scope recording defined in clause 45
  - **EXCUSED-absence extension vote:** procedure for extending a leave beyond 6 months defined — owner may ballot before absence or during it without losing EXCUSED status; extension vote must conclude before the 6-month limit; if the vote fails or is not called in time, standard absence/abstention tracking resumes
  - **Stripping-vote full reset (cl.23, cl.24):** reset of absence track, abstention track, and participation score now explicitly scoped to the owner who was the subject of the stripping vote; no other owner's tracks or score are affected
  - **Founder zero-ownership voting (cl.8):** if the Founder holds zero ownership at the time of a vote the Founder has no voting rights in that vote and is excluded from the tie-break rule; a tie fails regardless
  - **Cooldown and void votes (cl.8):** a vote that was void for lack of quorum does not trigger the 30-day per-subject cooldown; it may be re-opened immediately
  - **Secret-ballot substitute tally (cl.21b):** if a proposer is unable to submit their own tally before the reveal window expires, any other ownership holder may submit it on their behalf, provided the proposer has supplied their choice and nonce in writing; the substitute signs with their own key and attaches the proposer's written disclosure; if no owner can or will submit, the proposer is treated as ABSTAIN
  - **Administrative Notice scope (cl.25):** definition of qualifying "factual changes" expanded with explicit examples of what qualifies (GPG fingerprint update after a passed rotation vote; pseudonym or contact-address correction) and explicit examples of what does not qualify and requires a resolution vote instead (altering ownership or revenue percentages; adding or removing a contributor; modifying any floor or undiluted designation)
  - **Fork revenue floor (cl.26):** Founder's minimum share now explicitly defined as a first-priority carve-out from 100 % of the fork's gross commercial revenue before any internal distribution; not applied against the fork's internal distributable pool
  - **Fork dormancy deadlock (cl.26):** if a fork record has been queued 90+ consecutive days and no vote has opened because all remaining votes were open at queuing and have still not closed, the fork vote opens automatically at the 90-day mark; those prior open votes are treated as void for purposes of unblocking the fork vote only and continue independently
  - **Fork window force majeure (cl.26):** the 48-hour fork-execution window is paused during impediments entirely outside the forker's control (platform outage, natural disaster, government action); the forker must document the impediment by committing a signed statement within 24 hours of the window expiring; absence of such statement means the lapse stands; disputes resolved by resolution vote
  - **Fork vote irrevocability (cl.26):** prose clarified — "the remaining ownership holders proceed" wording tightened to make clear that irrevocability of the fork record means the vote must proceed to conclusion, not lapse
  - **Operational continuity during contested Founder succession (cl.29):** default notices under cl.3 sent by remaining holders collectively; audit right under cl.35 exercised by resolution vote; revenue owed to Founder held in escrow until succession is confirmed; no new commercial agreement may be executed in the Founder's name until succession is confirmed or a Commercial Agent is appointed
  - **Simultaneous incapacitation of all owners (cl.29):** new rule — last valid CONTRIBUTORS file remains authoritative; all active commercial agreements suspended; successors and heirs must reconstitute governance within 180 days; if none come forward, any party with evidence of a prior commercial relationship may apply to a competent court for appointment of a trustee; forking rights unaffected
  - **Violation notice triggers and retroactive claim limit (cl.33):** the 60-day window for the Founder to call a stripping vote now runs from the earliest of: written notice delivered to the Founder's recorded contact address; a governance artifact documenting the violation committed to the repository; or the Founder's written acknowledgement committed to the repository; retroactive compensation claims limited to five years preceding the date of written documentation; limitation does not apply where the violation involved deliberate concealment, fraud, or wilful misrepresentation
  - **Audit right during contested succession (cl.35):** if the Founder is deceased or permanently incapacitated and succession is unresolved, the audit right is exercised by the remaining ownership holders acting collectively by resolution vote; revenue statements received during contested succession are held until a valid successor or heir is confirmed
  - **Commercial-use dispute presumption and payment terms (cl.3):** where the parties dispute whether software use is a material input, the use is presumed commercial unless the asserting party demonstrates in writing that the software has no measurable effect on revenue-generating activity; new payment-terms paragraph states that specific percentages, frequency, currency, and method are defined in each commercial agreement; non-cash consideration valued at fair market value; the license prescribes only that a valid agreement must exist before commercial use begins
  - **New clause 38 — Indemnification:** each commercial licensee indemnifies the Founder, ownership holders, contributors, and their successors and heirs against claims arising from the licensee's use, deployment, distribution, products, services, or breaches; not applicable to claims arising solely from the Founder's own unmodified software; non-commercial users have no indemnification obligation
  - **New clause 39 — Export Compliance:** parties represent compliance with applicable export control laws including EU Dual-Use Regulation (EU) 2021/821; commercial licensees solely responsible for jurisdiction-level compliance; Founder makes no representation about export eligibility to specific destinations
  - **Clause renumbering:** former cl.38 (Governing Law) → cl.40; cl.39 (GPG Signatures) → cl.41; cl.40 (CONTRIBUTORS File) → cl.42; remaining clauses shifted accordingly
  - **Governing Law / Arbitration (cl.40, formerly 38):** seat of arbitration fixed as Madrid, Spain; proceedings in English unless parties agree otherwise; one arbitrator by default; any party may request a three-arbitrator panel within 15 days of the notice of arbitration being filed
  - **GPG Signatures as Consent (cl.41, formerly 39):** eIDAS representation narrowed — GPG clearsign signatures are presented as evidence of consent and may carry probative weight as electronic signatures; they are not represented as qualified or advanced electronic signatures under eIDAS 910/2014 unless the signing party has separately obtained a qualifying certificate; parties agree GPG signatures shall be treated as sufficient for internal governance and may be admitted as evidence in arbitral or judicial proceedings governed by this license
  - **License author succession (cl.3 / PBL upgrade clause):** if the original license author is deceased, designated Successor-Revenue or legal heirs acting as custodian of the license may issue updated PBL revisions

---

## [2026-05-11] (4)

### Changed
- `LICENSE` — PBL v2.0 comprehensive audit — 22 fixes across errors, gaps, ambiguities, and edge cases:
  - **Definitions:** Quorum definition now explicitly states ABSENT does not count toward quorum (only YES/NO/ABSTAIN/EXCUSED satisfy participation); Founder Dormancy definition now states EXCUSED resets the consecutive-absent counter but does not resolve the dormancy condition; Permanent Incapacitation now requires an original physician's certificate and adds a dispute procedure; AI-Generated Portion definition clarifies post-generation editing does not change classification; Fork definition tightened — the moment any independent modification is made the copy becomes a fork; private modification outside direct contribution or an approved fork is not permitted; Absence Track and Abstention Track definitions now specify that both tracks decrement simultaneously and atomically from a single YES/NO ballot
  - **Clause 8 & 22 (Voting / Verification):** Founder tie-break rule now explicitly covers ABSENT Founder (treated the same as did not vote)
  - **Clause 9 (Patent Ownership):** Patent assignment scoped to inventions directly embodied in the submitted contribution; no longer assignable beyond scope of contribution
  - **Clause 21b (Secret Ballot):** Reveal window fixed at 48 hours, non-extendable; nonce entropy requirement set at minimum 128 bits from a CSPRNG; secrecy obligation added — disclosing commitment data before voting window closes is bad-faith governance
  - **Clause 22 (Verification):** CONTRIBUTORS file update must be in the same commit as the final seal; late ballot dispute procedure added for cases where dispute is raised after CONTRIBUTORS is already updated
  - **Clause 23 (Absence and Abstention Tracking):** Mid-cycle decrements clarified as atomic/simultaneous; EXCUSED decrement applies uniformly to all owners including Founder
  - **Clause 24 (Ownership Stripping):** Revenue-only stripping clarified — may be called at any time by any owner without threshold; stripped-to-zero owners lose voting rights but retain right to request factual correction
  - **Clause 29 (Succession):** Abeyance window aligned with clause 26 — 180-day resolution deadline added; Successor-Revenue holder inherits commercial negotiation rights upon Founder's death or incapacitation, subject to resolution vote
  - **Clause 41 (AI Contributions):** Formal disclosure format added with required AI-Disclosure, Tool, and Scope fields; "AI-Disclosure: none" required when no AI was used
  - **Clause 43 (Commercial Agent):** Unilateral designation permitted before ownership is shared; scope constraint format defined — plain-language parenthetical, disputes resolved by resolution vote
  - **Clause 44 (Founder Dormancy):** Clarified EXCUSED does not end the dormancy condition; Founder must cast an active ballot to exit dormancy
  - **Clause 3 (Commercial Use):** Commercial agreement expiration grace period of 30 days added before unlicensed status applies
  - **Clause 35 (Audit Right):** Dispute procedure for inaccurate revenue statements added — Founder must notify before escalating, 14-day cure window, arbitration before enforcement

---

## [2026-05-11] (3)

### Changed
- `LICENSE` — PBL v2.0 gap and consistency audit — 4 fixes:
  - Cross-references in clauses 16, 28, 32(e), 40, 41 corrected from "clauses 19–22" to "clauses 19–25"; the governance process includes Administrative Notices (clause 25), so the prior range understated which acts qualify as governance-compliant
  - Clause 20: bundled-vote exceptions now list both permitted cases — clause 24 (combined ownership-and-revenue stripping) and clause 26b (fork + original CONTRIBUTORS revision); previously only clause 24 was named, implicitly forbidding clause 26b's expressly bundled vote
  - Clause 29: removed duplicated definition of "Permanent incapacitation" (already defined in the Definitions section); clause 29 now references the canonical definition
  - Clause 3: added pointer to the CONTACT section so commercial users know where to find the Founder's contact address

---

## [2026-05-11] (2)

### Changed
- `LICENSE` — PBL v2.0 forking process review — 4 fixes:
  - Clause 26: original Founder's ownership floor now explicitly carries over into a fork with the same clause 7 mechanics applied within the fork; only revenue floor was previously stated
  - Clause 26b: new Founder designation now requires documented written consent before the fork vote opens; a designation without consent is void and invalidates the proposed CONTRIBUTORS file
  - Clause 26b: queue record exclusivity rule added — only one queue record may be active at a time; a second record committed while one is active has no effect; the second proposer must wait for the first vote to conclude or the first record to be voided
  - Clause 26b: queue immediate-open rule clarified — if no votes were open at the time of queuing, the fork vote opens immediately upon the queue record being committed

---

## [2026-05-11]

### Changed
- `LICENSE` — PBL v2.0 prose cleanup: remove AI-style phrasing (broken mid-sentence linebreaks in cl.8 and cl.22; "including but not limited to" → "including"; "in whole or in part" → "wholly or partly"; "without limitation" dropped; redundant "in writing" removed from bad-faith queue exception; 48h fallback statement tightened)

- `LICENSE` — PBL v2.0 forking gap audit — 6 additional fixes:
  - Fix 1 — Clause 26: added snapshot rule for no-commit forks (distribution-moment trigger), matching the Fork definition
  - Fix 2 — Clause 26b: added fallback allowing any other owner to execute the fork commit if the proposer is incapacitated or dies within the 48-hour window; does not extend the window
  - Fix 3 — Clause 26b: added bad-faith queue exception — non-proposer owners may unanimously void a malicious queue record via a joint clearsigned declaration; voiding triggers a clause 32 termination process against the proposer
  - Fix 4 — Clause 26b: clarified that governance artifact copy includes in-progress vote folders copied as-is; open votes carry no binding effect on the fork
  - Fix 5 — Clause 28: clarified that the naming restriction is bilateral once a fork is independent; each project controls permission to use its own name
  - Fix 6 — Clause 26b fork-of-fork: clarified that the original Founder's revenue floor in a direct fork is unaffected by any further forking of that direct fork; a sub-fork carries no inherited obligation to the original Founder

- `LICENSE` — PBL v2.0 forking gap audit — 6 further fixes:
  - Clause 2 + Clause 26: "derivative" and "derived version" aligned to the Fork definition; both now reference the Fork definition explicitly
  - Clause 26: independence paragraph scoped to legitimate (clause 26b) forks only; a fork that has not been elevated under clause 26b does not gain independence by merely committing files
  - Clause 26: abeyance revenue share — inherited owner's revenue share is likewise suspended during abeyance; fork must hold it in escrow; accrued escrow released to confirmed successor or distributed proportionally on redistribution
  - Clause 26b: fork-of-fork rule added — a legitimate fork is a normal independent project; forking it again follows the same rules as any project; the original Founder's carried-over floor does not cascade into grandchild forks
  - Clause 26b: lost-proposer rule — the queue record constitutes the proposer's opening ballot and YES vote; if the proposer becomes unable to act, remaining owners vote to conclusion; the vote is not voided
  - Clause 28: "majority ownership vote" replaced with standard "resolution vote" under clauses 19–22

- `LICENSE` — PBL v2.0 forking gap audit — 8 additional fixes:
  - Definitions — Fork: new definition added; covers all independent copies developed or distributed outside the original project; excludes private non-distributed copies
  - Clause 26: illegitimate forks (those carrying the inherited CONTRIBUTORS file but not elevated via clause 26b) have no independent rights; may not enter commercial agreements, accept contributions, call votes, or modify CONTRIBUTORS; any such act is void and constitutes bad-faith governance under clause 32
  - Clause 26: deceased original Founder with no successor — carried-over revenue floor passes to designated Successor-Revenue or legal heirs; fork must hold owed amounts in escrow until a valid heir is confirmed; escrow follows clause 3 mechanics
  - Clause 26: sole-owner abeyance clarified — if the fork has only one ownership holder when the 180-day abeyance window expires, the abeyance share is automatically absorbed into that owner's holding; CONTRIBUTORS updated via Administrative Notice under clause 25
  - Clause 26b: fork queue record is irrevocable — cannot be withdrawn or cancelled after committing; the fork vote must be held to conclusion
  - Clause 26b: 48-hour commit window after a passing fork vote is explicitly hard — no extension permitted for any reason
  - Clause 26b: deliberate omission of governance artifacts from the fork constitutes bad-faith governance under clause 32; accidental omissions are curable within 30 days of identification; failure to cure is treated as deliberate
  - Clause 26 + 26b: waiver conflict resolved — original Founder's carried-over revenue floor may be reduced or removed only by a resolution vote among the fork's ownership holders, even when proposed by the Founder; no unilateral waiver is effective

- `LICENSE` — PBL v2.0 forking gap fixes (8 fixes):
  - Clause 26: unlicensed forks — a fork that does not carry over the inherited CONTRIBUTORS file at creation has no valid license; any distribution constitutes copyright infringement
  - Clause 26: fork commercial obligation — original Founder's revenue floor follows clause 3 payment/suspension/termination mechanics; original Founder must be named as payee in any fork commercial agreement; audit right under clause 35 explicitly extends to forks
  - Clause 26: post-fork independence — fork and original project are fully independent after the fork's CONTRIBUTORS file is committed; actions in one project have no effect on the other; waivers are per-project
  - Clause 26: fork CONTRIBUTORS snapshot — snapshot is the last validly committed CONTRIBUTORS at the moment of the fork's initial commit; pending votes and proposed files have no effect on the fork
  - Clause 26: abeyance deadline — inherited shares in abeyance must be resolved within 180 days; redistribution vote may not be called before that window expires without unanimous written consent
  - Clause 26b: minimum ownership — 5% minimum ownership requirement under clause 8 applies to fork proposals by non-Founder owners
  - Clause 26b: fork queue and vote ordering — fork vote requires all open votes to close first; queue record freezes new votes while existing ones finish; fork vote may run alongside new votes but those votes do not carry over; failed fork vote lifts the queue immediately
  - Clause 26b: 48-hour commit deadline — CONTRIBUTORS.proposed required at vote-opening time; forker has 48 hours after vote passes to create fork repo and commit; lapsed vote subject to 30-day cooldown

---

## [2026-05-10]

### Changed
- `LICENSE` — PBL v2.0 gap audit round 2 (6 fixes):
  - Clause 19: `governance/notices/` folder and acknowledgement file structure added to governance directory tree
  - Clause 25: acknowledgement file path and naming convention defined (`<fingerprint>.ack` + `.sig`); acknowledgement file content specified
  - Clause 25: objection timing explicitly restricted to pre-deadline only; post-deadline objections not recognised
  - Clause 29: split sentence in succession notification window repaired
  - Definitions — AI-Generated Portion: cross-reference to clause 41 added for disclosure procedure
  - Definitions — Emergency Key Replacement: new entry added to match named procedure in clause 42

---

## [2026-05-07]

### Changed
- `LICENSE` — PBL v2.0 gap audit and improvements (18 fixes):
  - Clause 2: share-alike "any later version" now requires the version to be a published PBL revision by the original author
  - Clause 3: "material input" defined; supply-chain commercial use gap closed — each party in a distribution chain must independently obtain a commercial agreement
  - Clause 3: payment-default suspension-to-termination mechanics clarified with explicit written-notice requirement; removed incorrect cross-reference to clause 33
  - Clause 17: change-of-control 30-day grace period anchored to change-of-control date (not notification date); late notification forfeits the grace period
  - Clause 20: `Opened-by` field added to vote record format to support the 30-day cooldown rule
  - Clause 22: quorum required for a vote to pass; votes that expire without quorum are void
  - Clause 25: Administrative Notice silence penalty reduced — first missed notice per calendar year carries no penalty; second and subsequent trigger abstention track increment
  - Clause 26: fork revenue floor explicitly creates a payment obligation for the fork; original Founder may waive in writing
  - Clause 29: declination clarified — per-entitlement-type for separate designations; single combined designation is all-or-nothing
  - Clause 29: death triggering date defined as date remaining holders first receive written notification with death certificate
  - Clause 31(d): AI disclosure cross-reference corrected to include the AI-Generated Portion definition
  - Clause 32: termination mechanics fixed — rights are suspended pending vote, not immediately and permanently terminated; permanent termination requires vote to pass
  - Clause 35: incomplete sentence completed — non-response to audit request treated as commercial violation including suspension of rights
  - Clause 41: AI disclosure procedure specified — must be in the PR description or equivalent submission artifact
  - Clause 42: Key Rotation Window explicitly supersedes the standard Voting Window; 48-hour floor does not apply
  - Clause 44: dormant Founder's ownership excluded from snapshot for temporary Commercial Agent appointment vote
  - Definitions — Quorum: redefined as a real minimum participation threshold (≥50% ownership must have voted); void if not met
  - Definitions — Participation Score: score threshold documented as the primary trigger; individual track thresholds clarified as independent fallback triggers
  - Voting rights explicitly stated — revenue-only contributors (zero ownership) have no governance rights

---

## [2026-05-06]

### Added
- `TODO.md` — todo list for pending review items

---

## [2026-05-06]

### Added
- `README.md` — contributing section linking to CONTRIBUTING.md

### Fixed
- `README.md` — currency logo URLs updated from `divisas/` to `currencies/` (SVG repo was renamed)

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
