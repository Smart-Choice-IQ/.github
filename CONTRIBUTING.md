# Contributing — Smart-Choice-IQ

## Branches

| Branch | Purpose | Protection |
|---|---|---|
| `main` | Production — what customers / the stores receive | PR + review + CI |
| `release/x.y` | Preparing a major release (e.g. Maidan 2.0) | PR + CI |
| `legacy/x.y` | Maintenance of an older version still in the field | PR + CI |
| `feat/<slug>` `fix/<slug>` `chore/<slug>` `docs/<slug>` `hotfix/<slug>` | Day-to-day work, deleted after merge | — |

- No direct pushes to protected branches. No `--force`. Tags are never deleted.
- Branch from `main` (or from `release/x.y` when the work targets an upcoming release).
- A hotfix branches from `legacy/x.y` or `main` and is merged into both (cherry-pick).

## Commits — Conventional Commits

```
feat(pos): add partial payment chips
fix(map): markers not refreshing after route change
chore(deps): bump dio to 5.9
docs(redesign): phase 3 notes
release: 2.0.0+4
```

- Bumping `version:` in `pubspec.yaml` (or `__version__` in a Frappe app) happens **only** in a PR titled `release: x.y.z+n` — that is what triggers the automated release.
- The build number (`+n`) always increases and never goes back.

## Pull requests

- Keep them small (≲ 600 lines of diff), Conventional-Commit title, template fully filled, screenshots for UI.
- `main` uses **squash merge** (linear history). `release/*` → `main` uses a merge commit.
- Reviewers come from `CODEOWNERS`. A red PR is never merged.

## Code

- **Flutter:** GetX + Clean Architecture; colors and sizes come from design tokens only; `flutter analyze --fatal-infos` is clean.
- **Frappe:** `ruff` is clean; no edits to core; every customisation lives in its own app; fixtures are exported.
- No real data and no secrets in the repository (push protection is enabled).
- Every repository contains `README.md`, `CLAUDE.md` and `docs/`.

## Releases

- `vX.Y.Z+N` tag + GitHub Release + build artifacts + team notification — automatically when a release PR is merged.
- Releases cut from `release/*` are marked **Pre-release** for testing.
