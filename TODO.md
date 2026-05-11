# TODO

## Public vote approval requirement

Currently, votes default to secret (commit-reveal) and owners can opt out by setting `Secret: no` in the vote record. The open question is whether that opt-out should be unilateral or should require prior approval from the other owners.

The concern is that a public vote exposes how each owner votes in real time, which creates conditions for pressure, retaliation, or coordinated influence before the window closes. Allowing any single owner to impose a public ballot on everyone else undermines the protection that secret voting is meant to provide.

The consent mechanism should be lightweight: each owner who is willing simply commits a signed ok to the repository before the vote opens. No formal ballot, no quorum math — just an explicit opt-in from each owner who chooses to respond.

The complication is that not every owner will necessarily respond. Some may be inactive, on a declared absence, or simply unresponsive. Requiring consent from every owner before a public vote can open would give a silent or absent owner an effective veto by doing nothing, which is too strong. The rule needs to account for non-response.

Things to work out before implementing:

- What counts as a valid ok — a clearsigned statement committed to the repo is the natural fit given the rest of the governance model.
- How long the consent window stays open before the proposer can proceed without hearing from everyone.
- Whether an owner who did not respond during the consent window can object after the vote opens, or whether silence during the window is treated as acceptance.
- How declared absences interact with the window — an excused owner probably should not be able to block a public vote by being absent.
- Where the signed consent statements live in the repo layout (alongside the `.vote` file, or in a separate pre-open folder).
- Whether there are categories of vote (e.g. purely procedural ones with no ownership consequences) that should be exempt from the requirement entirely.
- How this interacts with urgent votes, where the proposer can already bypass the 30-day cooldown — should urgency also be able to waive the consent requirement?
