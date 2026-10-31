# Agorail Labs governance

**Current model:** Founder-maintained, publicly reviewed open-source projects.

Agorail Labs is an independent initiative. Its initial founding maintainer is [@arjun2075](https://github.com/arjun2075). Additional maintainers or organizational governance roles should be announced explicitly; a review, comment, or outside contribution does not create such a role.

## Decisions

Each project governs its own technical scope and versioned releases.

- **Routine maintenance:** Maintainers review focused bug fixes, tests, and documentation changes against the project's recorded requirements.
- **Normative or safety-affecting changes:** Proposals should identify affected guarantees, negative tests, compatibility impact, and unresolved risks. The decision and rationale should be documented in an issue, pull request, or versioned decision record before publication.
- **Production claims:** Release readiness, live-provider verification, and operational safety require separate evidence; a passing simulator suite or independent reviewer comment alone cannot establish them.
- **Security matters:** Confidential disclosures follow the relevant project's security policy rather than public issue triage.

Decisions are not assumed ratified merely because they appear in drafts or discussion threads. Maintainers should preserve unresolved issues and rejected alternatives where they materially clarify the safety model.

## Maintainer participation

New maintainers may be invited following sustained, technically sound contributions and agreement on scope, review responsibilities, and access. No invitation, paid arrangement, or co-maintainer appointment is implied by this document.

## Independence

Projects may reference UCP, ACP, or commercial providers for research and compatibility analysis. No such reference creates standards-body affiliation, vendor backing, or authority to speak on another organization's behalf.

For contribution procedures see [CONTRIBUTING.md](CONTRIBUTING.md); for project-specific boundaries see [PROJECTS.md](PROJECTS.md).
