<p align="center">
  <img src="https://raw.githubusercontent.com/Smart-Choice-IQ/.github/main/profile/assets/banner.svg" alt="SmartChoice IQ" width="100%">
</p>

<p align="center">
  <a href="https://github.com/orgs/Smart-Choice-IQ/repositories"><img alt="Repositories" src="https://img.shields.io/badge/repositories-43-1C1F24?style=flat-square&labelColor=F7B500&color=1C1F24"></a>
  <img alt="ERPNext" src="https://img.shields.io/badge/ERPNext-v15-1C1F24?style=flat-square&logo=frappe&logoColor=F7B500">
  <img alt="Flutter" src="https://img.shields.io/badge/Flutter-stable-1C1F24?style=flat-square&logo=flutter&logoColor=F7B500">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.11-1C1F24?style=flat-square&logo=python&logoColor=F7B500">
  <img alt="License" src="https://img.shields.io/badge/code-proprietary-1C1F24?style=flat-square">
</p>

# SmartChoice IQ

**We build business systems for the Iraqi market** — ERP implementations on ERPNext/Frappe, mobile apps in Flutter, and multi-tenant SaaS products that run on our own Frappe cloud.

## Products

| Product | What it does | Stack |
|---|---|---|
| **Maidan** | Cash-van / field-sales app for ERPNext — routes, POS, pre-orders, collections, returns, visits | Flutter · GetX · ERPNext |
| **Zaboon** | Sales CRM — leads, deals, tasks, customers | Flutter · GetX |
| **Jabi** | Collections app for field cashiers | Flutter |
| **SmartResto** | Restaurant & café management, multi-tenant SaaS | Frappe |
| **Smart Education** | School management SaaS — admin, owner dashboard, parent app | Frappe Education · Flutter |
| **SmartChoice Portal** | Customer portal & control plane — plans, feature flags, support inbox | Frappe · Vue |

## How we work

<p align="center">
  <img src="https://raw.githubusercontent.com/Smart-Choice-IQ/.github/main/profile/assets/workflow.svg" alt="Branch → PR → CI → main → Release" width="100%">
</p>

- **Every repository** ships with a `README.md` (run & deploy), a `CLAUDE.md` (working rules for AI-assisted development) and a `docs/` folder.
- **Conventional Commits**, small pull requests, mandatory review from code owners, green CI before merge.
- **Releases are automatic**: bumping `version` in a `release:` PR tags the build, publishes a GitHub Release with artifacts and notifies the team.
- Details: [CONTRIBUTING.md](https://github.com/Smart-Choice-IQ/.github/blob/main/CONTRIBUTING.md) · [Security policy](https://github.com/Smart-Choice-IQ/.github/blob/main/SECURITY.md)

## Engineering standards

| Area | Standard |
|---|---|
| Flutter | GetX + Clean Architecture · design tokens only (no hard-coded colors/sizes) · `flutter analyze --fatal-infos` clean |
| Frappe | Customisations live in dedicated apps, never in core · `ruff` clean · fixtures exported · `bench run-tests` on every PR |
| Security | 2FA enforced · secret scanning with push protection · Dependabot · no real customer data in code or screenshots |
| Branches | `main` (production) · `release/x.y` · `legacy/x.y` · `feat/*` `fix/*` `hotfix/*` `chore/*` `docs/*` |

<p align="center"><sub>SmartChoice IQ · Karbala, Iraq</sub></p>
