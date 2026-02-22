# gras-lab/.github

This repository contains organization-wide defaults for all repositories under [gras-lab](https://github.com/gras-lab).

GitHub automatically applies these files to any repository in the organization that does not define its own.

## Contents

| File | Purpose |
|---|---|
| `profile/README.md` | Public profile shown on the [organization page](https://github.com/gras-lab) |
| `.github/ISSUE_TEMPLATE/bug_report.md` | Default bug report template for all repos |
| `.github/ISSUE_TEMPLATE/feature_request.md` | Default feature request template for all repos |
| `.github/PULL_REQUEST_TEMPLATE.md` | Default pull request template for all repos |
| `CONTRIBUTING.md` | Contribution guidelines (branch strategy, commit conventions, PR rules) |
| `CODE_OF_CONDUCT.md` | Community standards and enforcement policy |
| `SECURITY.md` | Vulnerability reporting process and response timeline |

## How defaults work

Files placed here apply org-wide. A repository can override any of them by creating its own copy at the same path inside its own `.github/` folder. The repository-level file always takes precedence.

## Resources

- [GitHub documentation: Default community health files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
