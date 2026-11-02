<p align="center">
  <img src="https://raw.githubusercontent.com/Smart-Choice-IQ/.github/main/profile/assets/banner.svg" alt="Smart Choice Company for Technical Solutions — Smart Solutions. Beyond Limits." width="100%">
</p>

<p align="center">
  <a href="https://smartchoice-iq.com"><img alt="Website" src="https://img.shields.io/badge/smartchoice--iq.com-2B780C?style=flat-square&logo=googlechrome&logoColor=FFFFFF"></a>
  <img alt="ERPNext" src="https://img.shields.io/badge/ERPNext-v15-141D00?style=flat-square&logo=frappe&logoColor=FFFFFF&labelColor=2B780C">
  <img alt="Flutter" src="https://img.shields.io/badge/Flutter-stable-141D00?style=flat-square&logo=flutter&logoColor=FFFFFF&labelColor=2B780C">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.11-141D00?style=flat-square&logo=python&logoColor=FFFFFF&labelColor=2B780C">
  <img alt="Google Play" src="https://img.shields.io/badge/Google_Play-published-141D00?style=flat-square&logo=googleplay&logoColor=FFFFFF&labelColor=2B780C">
  <img alt="App Store" src="https://img.shields.io/badge/App_Store-published-141D00?style=flat-square&logo=apple&logoColor=FFFFFF&labelColor=2B780C">
</p>

# Smart Choice

**Smart Choice Company for Technical Solutions**, also known as SmartChoice IQ, is an information-technology company based in Karbala, Iraq. We design, implement and host business systems for Iraqi companies and institutions: ERP implementations on **ERPNext/Frappe**, field and back-office **mobile apps in Flutter**, and our own **multi-tenant SaaS products** running on a private Frappe cloud.

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

Website **[smartchoice-iq.com](https://smartchoice-iq.com)** · Email [info@smartchoice-iq.com](mailto:info@smartchoice-iq.com) · [Facebook](https://facebook.com/smartchoice.iq) · Karbala, Iraq

<p align="center"><sub>© Smart Choice Company for Technical Solutions — Smart Solutions. Beyond Limits.</sub></p>
