# إعدادات المنظمة — تُضبط يدوياً من واجهة GitHub

## 1. الأمان (Organization → Settings)
- [ ] Authentication security → **Require two-factor authentication**
- [ ] Member privileges → Base permissions: **Read** · Repository creation: core فقط · Repository forking: off
- [ ] Code security → Enable for all repos: **Dependabot alerts**, **Dependabot security updates**, **Secret scanning**, **Push protection**
- [ ] Actions → Allow select actions: `actions/*`, `subosito/flutter-action`, `softprops/action-gh-release` · Workflow permissions: Read (الـ workflow يرفعها حسب الحاجة)

## 2. الفرق (Organization → Teams)
| Team | الأعضاء | الصلاحية الافتراضية |
|---|---|---|
| `core` | القيادة التقنية | Admin على المنتجات، Maintain على الباقي |
| `ops` | المتدربون / الدعم | Write على ريبوهات الواجهة، Read على الباقي |
| `clients-readonly` | عملاء يطّلعون على كودهم | Read على ريبو عميلهم فقط |

## 3. Rulesets (Organization → Repository → Rulesets)
### `protected-mainlines` — target: `main`, `release/**`, `legacy/**` — all repos
- [ ] Restrict deletions · Block force pushes · Require linear history
- [ ] Require a pull request: 1 approval · Dismiss stale approvals · **Require review from Code Owners** · Require conversation resolution
- [ ] Require status checks to pass: `check` (Flutter CI) أو `lint`+`tests` (Frappe CI)
- [ ] Bypass: فريق `core` (للطوارئ فقط)

### `branch-naming` — target: all branches except default
- [ ] Restrict branch names: regex `^(main|develop|release/.+|legacy/.+|feat/.+|fix/.+|hotfix/.+|chore/.+|docs/.+|refactor/.+|dependabot/.+|copilot/.+)$`

### `tags-immutable` — target: tags `v*`
- [ ] Restrict deletions · Restrict updates · Block force pushes

## 4. لكل ريبو منتج
- [ ] General → Merge: **Squash** افتراضي (Allow merge commits لـ release/*) · Auto-delete head branches · Discussions on
- [ ] Secrets → `ANDROID_KEYSTORE_B64`, `ANDROID_KEY_PROPERTIES`, `TG_BOT_TOKEN`, `TG_CHAT_ID`
- [ ] Environments → `production` مع Required reviewers = `core`
- [ ] Topics: `flutter` / `frappe-app` · `product` / `internal` / `client-<name>`
- [ ] Labels موحّدة: `bug`, `enhancement`, `client`, `triage`, `blocked`, `good first issue`
- [ ] انسخ `CODEOWNERS` إلى `.github/CODEOWNERS` · أضف workflows من Actions → New workflow → Smart-Choice-IQ templates
- [ ] `README.md` + `CLAUDE.md` + `docs/`

## 5. Claude
- [ ] Organization → Settings → GitHub Apps → تثبيت **Claude** ومنحه الريبوهات المطلوبة (حتى يشتغل Claude من المتصفح على ريبوهات المنظمة)
