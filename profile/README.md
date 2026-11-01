<p align="center">
  <img src="https://raw.githubusercontent.com/Smart-Choice-IQ/.github/main/profile/assets/banner.svg" alt="SmartChoice IQ" width="100%">
</p>

<p align="center">
  <a href="https://smartchoice-iq.com"><img alt="Website" src="https://img.shields.io/badge/smartchoice--iq.com-F7B500?style=flat-square&logo=googlechrome&logoColor=1C1F24"></a>
  <img alt="ERPNext" src="https://img.shields.io/badge/ERPNext-v15-1C1F24?style=flat-square&logo=frappe&logoColor=F7B500">
  <img alt="Flutter" src="https://img.shields.io/badge/Flutter-stable-1C1F24?style=flat-square&logo=flutter&logoColor=F7B500">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.11-1C1F24?style=flat-square&logo=python&logoColor=F7B500">
  <img alt="Google Play" src="https://img.shields.io/badge/Google_Play-published-1C1F24?style=flat-square&logo=googleplay&logoColor=F7B500">
  <img alt="App Store" src="https://img.shields.io/badge/App_Store-published-1C1F24?style=flat-square&logo=apple&logoColor=F7B500">
</p>

# SmartChoice IQ

**SmartChoice IQ** is an information-technology company based in Karbala, Iraq. We design, implement and host business systems for Iraqi companies and institutions: ERP implementations on **ERPNext/Frappe**, field and back-office **mobile apps in Flutter**, and our own **multi-tenant SaaS products** running on a private Frappe cloud.

We work with distributors, retailers, restaurants, schools and universities, and we publish our apps on Google Play and the App Store under the SmartChoice IQ brand.

## What we do

| Service | Description |
|---|---|
| **ERP implementation** | ERPNext for sales, inventory, accounting, HR and manufacturing — localised for Iraqi accounting, tax and payroll practice, with Arabic-first interfaces |
| **Custom Frappe apps** | Industry modules and client-specific customisations packaged as standalone apps, never patched into core |
| **Mobile apps** | Flutter apps connected to ERPNext for field sales, collections, CRM and management dashboards |
| **Hosting & operations** | Multi-tenant Frappe hosting on our own infrastructure — one site per client, custom domains, automated backups and upgrades |
| **Training & support** | Onboarding, user guides in Arabic, and ongoing support plans |

## Products

| Product | What it does | Stack |
|---|---|---|
| **Maidan** | Cash-van / field-sales app for ERPNext — routes, POS, pre-orders, collections, returns, visits | Flutter · GetX · ERPNext |
| **Zaboon** | Sales CRM — leads, deals, tasks, customers | Flutter · GetX |
| **Jabi** | Collections app for field cashiers | Flutter |
| **SmartResto** | Restaurant & café management, multi-tenant SaaS | Frappe |
| **Smart Education** | School management SaaS — admin, owner dashboard, parent app | Frappe Education · Flutter |
| **SmartChoice Portal** | Customer portal & control plane — plans, feature flags, support inbox | Frappe · Vue |

## How we build

<p align="center">
  <img src="https://raw.githubusercontent.com/Smart-Choice-IQ/.github/main/profile/assets/workflow.svg" alt="Branch → PR → CI → main → Release" width="100%">
</p>

| Area | Standard |
|---|---|
| Process | Conventional Commits · small pull requests · mandatory code-owner review · green CI before merge · automated releases on version bump |
| Flutter | GetX + Clean Architecture · design tokens only (no hard-coded colors or sizes) · `flutter analyze --fatal-infos` clean · Arabic RTL first |
| Frappe | Customisations in dedicated apps · `ruff` clean · fixtures exported · `bench run-tests` on every PR |
| Security | 2FA enforced · secret scanning with push protection · Dependabot · no real customer data in code or screenshots |
| Documentation | Every repository ships `README.md`, `CLAUDE.md` (AI-assisted development rules) and `docs/` |

Read more: [Contributing](https://github.com/Smart-Choice-IQ/.github/blob/main/CONTRIBUTING.md) · [Security policy](https://github.com/Smart-Choice-IQ/.github/blob/main/SECURITY.md)

## Contact

Website **[smartchoice-iq.com](https://smartchoice-iq.com)** · Karbala, Iraq

<p align="center"><sub>© SmartChoice IQ — Smart Choice for Information Technology</sub></p>
