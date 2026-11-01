# Organization governance — settings configured in the GitHub UI

## 1. Security (Organization → Settings)
- [ ] Authentication security → **Require two-factor authentication**
- [ ] Member privileges → Base permissions **Read** · Repository creation: owners only · Forking: off
- [ ] Code security → enable for all repositories: **Dependabot alerts**, **Dependabot security updates**, **Secret scanning**, **Push protection**
- [ ] Actions → Allow select actions: `actions/*`, `subosito/flutter-action`, `softprops/action-gh-release` · Workflow permissions: Read (workflows request more when needed)
- [ ] Add a **second owner** (backup account or trusted lead) — a single owner is a lock-out risk
- [ ] Billing → seats: make sure seats ≥ members before inviting trainees

## 2. Teams (Organization → Teams)
| Team | Members | Default access |
|---|---|---|
| `core` | Technical leadership | Admin on products, Maintain elsewhere |
| `ops` | Trainees / support | Write on UI repositories, Read elsewhere |
| `clients-readonly` | Clients reviewing their own code | Read on their repository only |

## 3. Rulesets (Organization → Repository → Rulesets)

### `protected-mainlines` — targets `main`, `release/**`, `legacy/**` — all repositories
- [ ] Restrict deletions · Block force pushes · Require linear history
- [ ] Require a pull request: 1 approval · Dismiss stale approvals · **Require review from Code Owners** · Require conversation resolution
- [ ] Require status checks: `check` (Flutter CI) or `lint` + `tests` (Frappe CI)
- [ ] Bypass list: team `core` (emergencies only)

### `branch-naming` — targets all branches except default
- [ ] Restrict branch names, regex:
  `^(main|develop|release/.+|legacy/.+|feat/.+|fix/.+|hotfix/.+|chore/.+|docs/.+|refactor/.+|dependabot/.+|copilot/.+)$`

### `tags-immutable` — targets tags `v*`
- [ ] Restrict deletions · Restrict updates · Block force pushes

## 4. Per product repository
- [ ] General → Merge: **Squash** default (allow merge commits for `release/*`) · Auto-delete head branches · Discussions on
- [ ] Secrets → `ANDROID_KEYSTORE_B64`, `ANDROID_KEY_PROPERTIES`, `TG_BOT_TOKEN`, `TG_CHAT_ID`
- [ ] Environments → `production` with required reviewers = `core`
- [ ] Topics: `flutter` / `frappe-app` · `product` / `internal` / `client-<name>`
- [ ] Labels: `bug`, `enhancement`, `client`, `triage`, `blocked`, `good first issue`
- [ ] Copy `CODEOWNERS` to `.github/CODEOWNERS` · add workflows from *Actions → New workflow → By Smart-Choice-IQ*
- [ ] `README.md` + `CLAUDE.md` + `docs/`

## 5. AI tooling
- [ ] Organization → Settings → GitHub Apps → install **Claude** and grant the required repositories (enables Claude to work on organization repositories directly)
