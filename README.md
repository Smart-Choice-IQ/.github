# `.github` — الملفات الافتراضية لمنظمة Smart-Choice-IQ

كل ما في هذا الريبو يُطبَّق تلقائياً على كل ريبوهات المنظمة التي لا تملك نسختها الخاصة:

| الملف | الأثر |
|---|---|
| `profile/README.md` | صفحة المنظمة العامة |
| `CODEOWNERS` | المراجعون الإلزاميون (يُفعَّل بالـ Rulesets) |
| `PULL_REQUEST_TEMPLATE.md` | قالب كل PR |
| `ISSUE_TEMPLATE/` | قوالب bug / feature / client-request |
| `CONTRIBUTING.md`, `SECURITY.md` | قواعد المساهمة والإبلاغ الأمني |
| `workflow-templates/` | قوالب CI/Release تظهر في تبويب Actions → New workflow لكل ريبو |
| `docs/GOVERNANCE.md` | قائمة الإعدادات التي تُضبط يدوياً من واجهة GitHub (Rulesets, Teams, 2FA) |

> **ملاحظة:** `CODEOWNERS` من هذا الريبو لا يُورَّث تلقائياً — انسخه إلى `.github/CODEOWNERS` داخل كل ريبو (أو استخدم Ruleset "Require code owner review" مع نسخة محلية).
