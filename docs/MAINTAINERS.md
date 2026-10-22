# Maintainer guide

## Repository directory

| Repository | Role | Main checks | Dependency updates |
| --- | --- | --- | --- |
| [ZipZap](https://github.com/Lord-Labs/ZipZap) | Windows application and browser handoff | Follow its contribution guide; hosted repository checks remain manual by prior owner preference | Existing npm, Cargo, GitHub Actions config |
| [lor](https://github.com/Lord-Labs/lor) | Video meetings | Existing CI; live two-person media E2E is intentionally skipped and must not be claimed as tested | Existing npm and GitHub Actions config |
| [NetScope](https://github.com/Lord-Labs/NetScope) | Household accounting foundation | Existing Foundation checks; hardware measurement gates remain separate | npm, Cargo host, GitHub Actions |
| [lordlabs.tech](https://github.com/Lord-Labs/lordlabs.tech) | Organization website and journal | Existing website tests and build | GitHub Actions; currently no npm dependencies |
| [zipzap-website](https://github.com/Lord-Labs/zipzap-website) | ZipZap landing page | Local `npm run check` and build; hosted CI remains off by prior preference | Currently no dependencies or Actions to update |
| [.github](https://github.com/Lord-Labs/.github) | Profile and community defaults | Review Markdown, links, and issue forms | No executable dependencies |

## Starting a repository

1. Choose public/private visibility deliberately and add the correct project license. Do not apply a blanket organization license.
2. Set a clear description, useful topics, and a real homepage/documentation URL. Use `main` as the default branch.
3. Use the shared community defaults unless the project needs a more specific policy. CODEOWNERS, workflows, Dependabot and licenses require local files; they are not inherited.
4. Enable vulnerability alerts, applicable security updates, secret scanning, push protection, and private vulnerability reporting. Review alerts privately; never put a secret value into an issue or PR.
5. Use pull requests for main, block force pushes and deletion, resolve review conversations, and delete merged feature branches. The sole maintainer can merge after verification without requiring approval from themselves. Preserve existing stricter protections.
6. Require only checks that run reliably for the relevant PR. Never require a manual workflow, a deployment requiring secrets, or a deliberately disabled E2E suite as evidence of passing tests.
7. Add real open work to the shared project board. Keep product scope, acceptance criteria, dependencies and priorities in the source issue.

## Ongoing maintenance

- Triage incoming issues, confirm reproduction and put the work in the correct repository. Apply existing project labels rather than replacing project taxonomies. Do not label work as beginner-friendly without checking scope and dependencies.
- Use Todo for unstarted work, In Progress only with real implementation evidence, and Done only when the source issue is complete. An open PR is evidence of activity, not completion. Dependency updates remain in their repository PR list.
- Review dependency updates against the project's checks; do not bulk-merge unrelated updates or advertise unverified releases.
- Review access and security settings when adding collaborators. The organization currently has one owner; do not invent teams or grant access just to fill an empty section.
- Before requiring organization-wide 2FA, verify the owner's recovery methods and member readiness. Domain verification needs control of DNS. Sponsorship needs a real funding destination. These require owner-provided setup information.
- Update the profile and this directory when projects change. Preserve original product identities and distinguish released software from foundation work.
