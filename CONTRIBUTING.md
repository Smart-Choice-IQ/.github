# قواعد المساهمة — Smart-Choice-IQ

## الفروع
| الفرع | الغرض | الحماية |
|---|---|---|
| `main` | الإنتاج — ما يُنشر للعملاء/المتجر | PR + مراجعة + CI |
| `release/x.y` | تحضير إصدار كبير (مثل ميدان 2.0) | PR + CI |
| `legacy/x.y` | صيانة إصدار قديم ما زال عند العملاء | PR + CI |
| `feat/<slug>` `fix/<slug>` `chore/<slug>` `docs/<slug>` `hotfix/<slug>` | عمل يومي، يُحذف بعد الدمج | — |

- لا push مباشر على الفروع المحمية. لا `--force`. لا حذف tags.
- الـ branch يُفتح من `main` (أو من `release/x.y` إذا الشغل لإصدار قادم).
- hotfix يُفتح من `legacy/x.y` أو `main` ويُدمج في الاثنين (cherry-pick).

## الـ commits — Conventional Commits
```
feat(pos): add partial payment chips
fix(map): markers not refreshing after route change
chore(deps): bump dio to 5.9
docs(redesign): phase 3 notes
release: 2.0.0+4
```
- رفع `version:` في `pubspec.yaml` / `__version__` يصير **فقط** في PR عنوانه `release: x.y.z+n` — وهذا ما يُطلق الإصدار التلقائي.
- build number (`+n`) يزيد دائماً ولا يرجع.

## الـ PR
- صغير (≤ ~600 سطر diff)، عنوان بصيغة Conventional Commit، القالب مكتمل، لقطات للواجهات.
- Squash merge افتراضياً على `main` (تاريخ خطي). `release/*` → `main` بـ merge commit.
- المراجع من CODEOWNERS. لا يُدمج PR أحمر.

## الكود
- Flutter: GetX + Clean Architecture، لا ألوان/أبعاد ثابتة خارج الـ tokens، `flutter analyze` نظيف.
- Frappe: `ruff` نظيف، لا تعديل على core، كل تخصيص في app خاص، fixtures مُصدَّرة.
- لا بيانات حقيقية ولا أسرار في الكود (Push protection مفعّل).
- كل ريبو: `README.md` + `CLAUDE.md` + `docs/`.

## الإصدارات
- `vX.Y.Z+N` tag + GitHub Release + ملفات البناء + إشعار الفريق — تلقائياً عند دمج PR الإصدار.
- `release/*` ينتج Pre-release للاختبار.
