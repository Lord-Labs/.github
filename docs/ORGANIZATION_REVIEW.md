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
| Community conversation | No organization discussion hub | Enable Discussions on `.github` and connect it to the organization |
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

Verification completed: private vulnerability reporting, vulnerability alerts, automated security updates, secret-scanning user alerts and push protection were enabled and read back on all six reviewed repositories. There were zero open secret-scanning alerts returned at verification time; this is not a guarantee that no unsupported secret exists.

Local validation: organization YAML and manifest paths parsed successfully; original wordmarks match the supplied website assets; NetScope repository checks passed (56 Markdown links); LORD Labs website passed 21 tests and build; ZipZap website passed 5 tests and build. All three repository changes were merged through PRs [lordlabs.tech#1](https://github.com/Lord-Labs/lordlabs.tech/pull/1), [zipzap-website#5](https://github.com/Lord-Labs/zipzap-website/pull/5), and [NetScope#36](https://github.com/Lord-Labs/NetScope/pull/36). NetScope's hosted `web-api` and `windows-host` jobs both passed before merge. No unrelated product or dependency PR was merged.

GitHub's project item listing did not agree with the issue-side project associations during verification. Re-adding the associations in small API batches succeeded, but the project-wide listing still returned zero; UI additions also disappeared from the view after reload. This is an unresolved GitHub listing problem, not a verified working board. The profile therefore links directly to the [roadmap index](ROADMAP.md), which preserves all 42 source issue links. Do not interpret an empty project view as an empty backlog.

The initial review covered the five existing public product/website repositories plus the new shared `.github` repository. Repositories created concurrently with this review are outside that verified snapshot.
