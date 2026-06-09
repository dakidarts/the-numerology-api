# The Numerology API

<p align="center">
  <img src="https://res.cloudinary.com/ds64xs2lp/image/upload/v1758341353/cover_dne2nf.jpg" alt="The Numerology API Cover" width="100%" />
</p>

<p align="center">
  <a href="https://docs.numerologyapi.com/">
    <img src="https://img.shields.io/badge/docs-live-0ea5e9?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Docs Live" />
  </a>
  <a href="https://dashboard.numerologyapi.com/">
    <img src="https://img.shields.io/badge/dashboard-open-111827?style=for-the-badge&logo=speedtest&logoColor=white" alt="Dashboard" />
  </a>
  <a href="https://numerologyapi.com/">
    <img src="https://img.shields.io/badge/platform-numerologyapi.com-14b8c9?style=for-the-badge&logo=googlecloud&logoColor=white" alt="Platform" />
  </a>
  <a href="https://rapidapi.com/dakidarts-dakidarts-default/api/the-numerology-api">
    <img src="https://img.shields.io/badge/rapidapi-marketplace-7c3aed?style=for-the-badge&logo=rapid&logoColor=white" alt="RapidAPI" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-v1.0.1-22c55e?style=flat-square" alt="Version v1.0.1" />
  <img src="https://img.shields.io/badge/docs-210%2B%20endpoint%20pages-0f766e?style=flat-square" alt="201+ endpoint pages" />
  <img src="https://img.shields.io/badge/languages-en%20%7C%20es%20%7C%20de%20%7C%20fr%20%7C%20pt%20%7C%20ar%20%7C%20hi%20%7C%20ja-1d4ed8?style=flat-square" alt="Languages" />
  <img src="https://img.shields.io/badge/engine-Swiss%20Ephemeris%20powered-0f172a?style=flat-square" alt="Swiss Ephemeris powered engine" />
</p>

> The Numerology API by Dakidarts is an enterprise-grade numerology, horoscope, astrology, and divination API for production apps, SaaS products, bots, dashboards, and spiritual intelligence experiences.
>
> The current platform exposes **210+ API endpoints**, including **130+ horoscope routes**, direct API key access, credit-based billing, localized response support, and multi-system numerology across **Pythagorean, Chaldean, and Vedic** calculations.

---

<p align="center">
  <img src="https://res.cloudinary.com/ds64xs2lp/image/upload/v1780938449/v1-0-1-release_fhre9c.svg" alt="v1.0.1 - Full Multilingual Systems Release" width="100%" />
</p>

## Latest Release

**v1.0.1 - Full Multilingual Systems Release**

v1.0.1 expands the direct API platform with full multilingual support for supported numerology responses, hardened numerology-system selection through `num_sys`, and 10 new production-ready endpoint families.

Highlights:

- **8 supported response languages:** `en`, `fr`, `es`, `de`, `pt`, `ja`, `hi`, `ar`
- **Multi-system numerology:** `pythagorean`, `chaldean`, `vedic`
- **10 new direct API endpoint families** for career, wealth, addresses, baby names, teams, domains, products, decisions, launch timing, and archetype stacks
- **Production validation:** localized JSON meanings, endpoint contracts, docs, and dashboard discovery refreshed for v1.0.1

Read the full release notes: [v1.0.1 changelog](https://docs.numerologyapi.com/changelog/changelog-v1-0-1/)

<p align="center">
  <a href="https://dashboard.numerologyapi.com/credits">
  <img src="https://res.cloudinary.com/ds64xs2lp/image/upload/v1780992687/numerology-api-banner_l73pov.png" alt="v1.0.1 Release Promo" width="100%" />
  </a>
</p>

## Core Capabilities

- **Numerology Intelligence:** Life path, destiny/expression, soul urge, personality, balance, karmic lessons, cycles, bridge numbers, name readings, compatibility, timing, and extended spiritual analysis.
- **Multi-System Name Numerology:** Pythagorean by default, with optional Chaldean and Vedic systems via `num_sys`.
- **Horoscope and Astrology:** Daily, weekly, monthly, yearly, planetary, zodiac, compatibility, astrology report, transit, aspect, house, and chart-oriented endpoints.
- **Business and Product Readings:** Business names, brand comparisons, product names, domain names, launch timing, decision analysis, and wealth/career readings.
- **Relationship and Family Readings:** Relationship composites, healing readings, parent-child numerology, team dynamics, and soul connection indicators.
- **Multilingual Output:** Supported numerology/helper responses can use `lang=en|fr|es|de|pt|ja|hi|ar`.
- **Production Operations:** API keys, dashboard access, credits, usage visibility, internal docs, and direct-host deployment at `api.numerologyapi.com`.

## Example Request

```bash
curl -X GET "https://api.numerologyapi.com/api/v1/career-path-numerology?full_name=Ada%20Lovelace&dob=1815-12-10&current_role=Mathematician&num_sys=chaldean&lang=fr" \
  -H "X-API-Key: YOUR_API_KEY"
```

POST requests also support `lang` in the query string and `num_sys` in the JSON body where the endpoint supports numerology systems.

## v1.0.1 Endpoint Families

The v1.0.1 release adds these direct API endpoint families:

| Endpoint | Methods | Purpose |
| --- | --- | --- |
| `/api/v1/career-path-numerology` | GET, POST | Career strengths, work style, and professional alignment |
| `/api/v1/wealth-code-reading` | GET, POST | Money pattern, earning style, and prosperity lessons |
| `/api/v1/home-address-numerology` | GET, POST | Home or location vibration analysis |
| `/api/v1/baby-name-forecast` | GET, POST | Baby-name candidate comparison and family harmony |
| `/api/v1/team-dynamics-numerology` | GET, POST | Team mission, member balance, and collaboration dynamics |
| `/api/v1/domain-name-numerology` | GET, POST | Domain-name vibration and brand-fit insights |
| `/api/v1/product-name-numerology` | GET, POST | Product, app, offer, or feature-name alignment |
| `/api/v1/decision-crossroads-reading` | GET, POST | Option comparison for major decisions |
| `/api/v1/launch-timing-numerology` | GET, POST | Date scoring for launches and releases |
| `/api/v1/personal-archetype-stack` | GET, POST | Combined archetype profile from name and birth data |

## Documentation

- Public docs: [docs.numerologyapi.com](https://docs.numerologyapi.com/)
- v1.0.1 release notes: [Full Multilingual Systems Release](https://docs.numerologyapi.com/changelog/changelog-v1-0-1/)
- Dashboard/signup: [dashboard.numerologyapi.com](https://dashboard.numerologyapi.com/signup)
- Website: [numerologyapi.com](https://numerologyapi.com/)

---

## Access channels

### Direct platform access
For the newest and most advanced platform capabilities, use:

- **Base URL:** `https://api.numerologyapi.com`
- **Auth:** `X-API-Key: YOUR_API_KEY`
- or `Authorization: Bearer YOUR_API_KEY`

### RapidAPI
Marketplace access remains available for supported public surfaces on RapidAPI:

- https://rapidapi.com/dakidarts-dakidarts-default/api/the-numerology-api

> Some newer and extended releases are **direct-platform only** and are not fully mirrored through RapidAPI.

---

## Example use cases

The Numerology API is built for products such as:

- mobile numerology apps
- astrology and horoscope apps
- dashboard products
- personalized PDF/report generators
- compatibility tools
- spiritual coaching software
- Telegram and WhatsApp bots
- browser extensions
- WordPress integrations
- content automation and SEO engines
- SaaS products that need symbolic or timing-based intelligence

---

## Ecosystem

### Documentation site
A dedicated docs platform with structured navigation, examples, changelogs, and release pages:

- https://docs.numerologyapi.com/

### Numerology dashboard
Manage access, keys, credits, and usage:

- https://dashboard.numerologyapi.com/

### Numerology bot
Official bot experience powered by the platform:

- https://numerologybot.com
- https://t.me/NumerologyAstroBot

### WordPress plugin
Free plugin for bringing numerology insights into WordPress sites:

- https://hub.dakidarts.com/getting-started-with-dakidarts-numerology-wordpress-plugin/

### Firefox extension
Numerology Report Generator Pro:

- GitHub: https://github.com/dakidarts/numerology-report-generator-pro
- Firefox Add-ons: https://addons.mozilla.org/en-US/firefox/addon/numerology-report-generator/

---

## Open-source astrology engine (Python library + CLI)

If you want a lightweight, open-source astrology stack outside the full hosted platform, use **OpAstro**.

**OpAstro** is our open-source astrology engine for Python developers and indie astrologers:

- Python library + CLI interface
- lightweight sibling of our main production horoscope engine
- built for local workflows, scripting, and indie product integration
- practical for developers who want direct control and self-managed usage

- **Repo:** https://github.com/dakidarts/opastro
- **Site:** https://opastro.com/

> If OpAstro helps your work, please star the repo.
> GitHub stars help the algorithm recommend the project to more builders.

---

## Authority and release discipline

This platform has evolved through continuous releases from early public numerology tooling into a broader intelligence platform with:

- 203+ documented endpoint/reference pages in the current release docs
- direct-platform and marketplace distribution
- versioned changelogs and release documentation
- enterprise-style metadata wrappers
- multilingual validation across supported surfaces
- an internal horoscope engine replacing dependence on legacy third-party flows

v1.0.0 marks the transition from “feature collection” to **structured platform architecture**.

---

## Repository purpose

This GitHub repository serves as the public-facing home for:

- project identity and platform overview
- release visibility
- ecosystem links
- documentation entry points
- product credibility and technical positioning

If you are looking to integrate the API, start with the docs and dashboard rather than the repository itself.

---

## Getting started

### 1) Open the docs
Start here:

- https://docs.numerologyapi.com/

### 2) Create or access your account
Open the dashboard:

- https://dashboard.numerologyapi.com/

### 3) Pick your access path
Choose between:

- direct platform access for the newest and extended surfaces
- RapidAPI for supported marketplace surfaces

### 4) Test endpoints
Use the documentation examples and reference pages to begin integrating.

---

## Selected feature timeline

### Early platform foundation
The platform started with core numerology, zodiac sign intelligence, and major horoscope sections.

### Birth charts and visual astrology
Added:

- `/birth-chart`
- `/birth-chart/svg`

### Tarot surfaces
Added tarot reading endpoints for multi-card and power-card use cases.

### Advanced numerology releases
Expanded into:

- hidden passion positions
- mirror numbers
- essence cycles
- bridge numbers
- compatibility systems
- angel number synchronicities
- personal hour
- lifecycle and timing intelligence

### v0.1.1
Expanded themed, human-centered response quality and companion ecosystem tooling.

### v1.0.0
Unified release for major numerology and horoscope expansion, documentation maturity, route normalization, and in-house engine authority.

---

## Brand and philosophy

The Numerology API is built at the intersection of:

- symbolic intelligence
- developer usability
- structured automation
- spiritual tooling
- production-grade delivery

It is designed to help builders create products that are not only functional, but meaningful.

> “As within, so without. As in the code, so in the cosmos.”

---

## Stay connected

- **Website:** https://numerologyapi.com/
- **Docs:** https://docs.numerologyapi.com/
- **Dashboard:** https://dashboard.numerologyapi.com/
- **RapidAPI:** https://rapidapi.com/dakidarts-dakidarts-default/api/the-numerology-api
- **X:** https://x.com/dakidarts/
- **GitHub:** https://github.com/dakidarts/the-numerology-api

---

## License and contribution

This repository is primarily a public project and platform-facing repository.

For platform usage, integration, and endpoint access, use the official docs and dashboard.  
For collaboration or partnership opportunities, reach out through Dakidarts channels.

---

<p align="center">
  <strong>Build with numbers. Ship with clarity. Scale with structured cosmic intelligence.</strong>
</p>
