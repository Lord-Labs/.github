# Organization review — 2026-10-22

Scope: all five existing public repositories, their community files, repository settings, branch protection, dependency maintenance, open issues, organization profile, pinned projects, and shared planning. This is a repository-management review, not a source-code security audit or release certification.

## Findings and changes

| Area | Finding | Action |
| --- | --- | --- |
| Organization profile | No profile README or pinned projects | Bilingual project directory, original wordmark, contribution/support links; pin the three products and organization website |
| Shared community files | No public `.github` repository | Shared contribution, conduct, support, security, governance, issue forms, and PR template |
| Website ownership | Both websites lacked CODEOWNERS | Name the existing organization maintainer locally |
| Website contribution guidance | ZipZap website had only a README | Add a focused guide with actual Node 24 commands and existing hosted-CI preference |
| Dependency configuration | NetScope had no Dependabot; organization site Actions had no update config | Add scoped configurations; preserve existing LOR./ZipZap exceptions and limits |
| Security features | Secret-scanning user alerts/push protection disabled across the original repositories; some security updates/reporting disabled | Enable available free repository protections and verify returned settings |
| Merge hygiene | Websites kept merged branches and allowed multiple merge styles | Use existing application convention: squash merge and delete merged feature branches |
| Branch protection | LOR./ZipZap already protected; NetScope and websites not protected | Preserve existing application rules; add PR, conversation, force-push/deletion protection to unprotected main branches |
| Shared planning | No organization project board | Create a board from existing open issues; link active work without inventing completion or changing project dependency gates |
| Discoverability | NetScope/ZipZap website lacked topics | Add factual stack/product topics and NetScope documentation homepage |

## Decisions requiring owner information

- **Organization 2FA policy:** not required at review time. Verify the owner's recovery methods before enforcing a membership policy. No authentication or membership changes are part of this review.
- **Verified domain:** `lordlabs.tech` is not verified on the organization. DNS ownership proof is needed; adding a website link is not domain verification.
- **Backup owner / teams:** the organization has one owner. A trusted second owner requires a real person and an access decision. No empty teams, invitations, or fabricated roles are added.
- **Funding:** no verified sponsorship destination was provided, so no FUNDING file or donation link is fabricated.

## Verification and limits

Check the live repository settings after applying changes. Community defaults can take time to appear in GitHub's cached health percentage; YAML issue forms may not be counted as the older Markdown `issue_template` field. Existing project-specific files take precedence.

The original LOR. branch protection includes the deliberately skipped two-person E2E context. This review preserves its existing protection; skipped E2E is not evidence that live media was tested. See its existing reproducibility issue [lor#221](https://github.com/Lord-Labs/lor/issues/221).

Product code, release binaries, deployments, open dependency PRs, and hardware validation are outside this organization-management change. No repository is renamed, archived, deleted, or made more public. The new profile repository contains public community resources only; the shared roadmap contains existing public issue references.
