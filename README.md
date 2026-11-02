# `.github` — organization defaults for Smart-Choice-IQ

Everything in this repository is applied automatically to every repository in the organization that does not define its own copy.

| Path | Effect |
|---|---|
| `profile/README.md` | Public organization profile page |
| `CODEOWNERS` | Mandatory reviewers (enforced through rulesets) — **copy into each repo's `.github/`** |
| `PULL_REQUEST_TEMPLATE.md` | Template for every pull request |
| `ISSUE_TEMPLATE/` | Bug report · Feature request · Client request |
| `CONTRIBUTING.md` · `SECURITY.md` | Contribution rules and vulnerability disclosure |
| `workflow-templates/` | CI and release workflows offered under *Actions → New workflow → By Smart-Choice-IQ* |
| `docs/BRAND.md` | Colors, typography and logo assets for GitHub surfaces |
| `docs/GOVERNANCE.md` | Checklist of settings that must be configured in the GitHub UI (2FA, teams, rulesets, secrets) |

## Applying the standard to a repository

1. Copy `CODEOWNERS` into `.github/CODEOWNERS`.
2. *Actions → New workflow* → pick **Flutter CI** or **Frappe CI**, and **Release on version bump**.
3. Add the secrets listed in `docs/GOVERNANCE.md` §4.
4. Add `README.md`, `CLAUDE.md` and `docs/`.
5. Confirm the organization rulesets show as *Active* under *Settings → Rules*.
