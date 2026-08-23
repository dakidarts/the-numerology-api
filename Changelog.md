# The Numerology API Changelog

## v1.0.3 - Zodiac Intelligence and Numora Studio Beta Release (August 22, 2026)

![The Numerology API v1.0.3 release banner](https://res.cloudinary.com/ds64xs2lp/image/upload/v1787480189/v1-0-3-release_lsbajc.svg)

v1.0.3 is a product-facing release across the direct API and its practitioner tooling. It adds a complete zodiac sign reference surface, makes planetary report behavior more predictable, improves a core numerology endpoint, and gives horoscope-report consumers explicit control over on-demand translation providers. It also introduces **Numora Studio v0.1.0-beta** for macOS, Windows, and Linux.

### New

- Added five dedicated zodiac reference families under `/api/v1/horoscope/sign/`: Sun, Moon, Rising/Ascendant, Modality, and Element.
- Added full birth-chart SVG wheel customization, including presets, themes, custom palettes, panel layout, visibility controls, typography, planet colors, split output, transparent backgrounds, and compression options.
- Added on-demand translation routing for horoscope reports through self-hosted LibreTranslate, Google Translate, and DeepL BYOK.
- Added translation-provider observability through `_api_metadata_.translation_provider` for translated responses.
- Released Numora Studio v0.1.0-beta for macOS, Windows, and Linux, using the dedicated `tnsr_` Studio channel.
- Added the v1.0.3 release surface across the API website, dashboard, documentation, and localized announcement content.

The five new zodiac families are:

| Family | Route | Purpose |
| --- | --- | --- |
| Sun sign | `/api/v1/horoscope/sign/sun` | Identity, vitality, purpose, compatibility, and sign facts |
| Moon sign | `/api/v1/horoscope/sign/moon` | Emotional, instinctive, intuitive, and inner-world readings |
| Rising sign | `/api/v1/horoscope/sign/ascendant` | Public persona, first impressions, outer expression, and direction |
| Modality | `/api/v1/horoscope/sign/modality` | Cardinal, fixed, and mutable sign expressions |
| Element | `/api/v1/horoscope/sign/element` | Fire, earth, air, and water elemental expressions |

All five families return structured sign facts, symbols, archetypes, summaries, detailed meanings, and the enterprise usage wrapper through the shared response pipeline. They are available through the documented `GET` and `POST` contracts.

### Improvements

- Standardized planetary report requests around the `general` planet option and made it the default where a planetary selection is required.
- Corrected Birth Day Number request validation and meaning resolution while preserving GET and POST parity.
- Refined Studio plan presentation, checkout hand-offs, API-key discovery, and desktop authorization states for the API-and-desktop workflow.
- Updated tenant-facing Studio usage views to show calculated percentages without disclosing internal token quantities.
- Preserved the existing direct API and PayPal payment paths while extending the platform with the Studio billing surfaces.
- Added the Numora Studio product links for the desktop repository and the public Studio page:
  - https://github.com/dakidarts/numora-studio-desktop
  - https://numerologyapi.com/studio

### Fixes

- Removed duplicate authorization entries and corrected consent success and failure state presentation.
- Standardized the runtime FastAPI/OpenAPI version and shared response metadata to `1.0.3`.
- Improved localized release and dashboard copy so the v1.0.3 announcement remains consistent across supported language surfaces.

### Deprecated

- No production API endpoint was deprecated in v1.0.3.

## v1.0.1 - Full Multilingual Systems Release (June 8, 2026)

![The Numerology API v1.0.1 release banner](https://res.cloudinary.com/ds64xs2lp/image/upload/v1780938449/v1-0-1-release_fhre9c.svg)

v1.0.1 expands The Numerology API with full multilingual support for supported numerology responses, production-ready multi-system numerology through `num_sys`, and 10 new direct API endpoint families.

### New

- Added full 8-language support for supported numerology/helper responses: `en`, `fr`, `es`, `de`, `pt`, `ja`, `hi`, `ar`.
- Added production-ready numerology-system selection for supported name-based calculations: `pythagorean`, `chaldean`, and `vedic`.
- Added 10 new direct API endpoint families:
  - `GET/POST /api/v1/career-path-numerology`
  - `GET/POST /api/v1/wealth-code-reading`
  - `GET/POST /api/v1/home-address-numerology`
  - `GET/POST /api/v1/baby-name-forecast`
  - `GET/POST /api/v1/team-dynamics-numerology`
  - `GET/POST /api/v1/domain-name-numerology`
  - `GET/POST /api/v1/product-name-numerology`
  - `GET/POST /api/v1/decision-crossroads-reading`
  - `GET/POST /api/v1/launch-timing-numerology`
  - `GET/POST /api/v1/personal-archetype-stack`
- Added localized v1.0.1 release/docs coverage for all 8 supported languages.
- Updated platform messaging to reflect **210+ total endpoints** and **130+ horoscope-focused routes**.

### Fixes

- Validated the new multilingual JSON meaning bundles for structure, placeholders, URL/API-token parity, and leakage safety.
- Hardened Vedic numerology as an explicit supported system with separate mapping ownership and Latin diacritic normalization.
- Aligned Chaldean and Vedic missing-value handling so `9` is not incorrectly reported as a missing alphabet value.
- Kept public routes clean under `/api/v1/*` and removed the public-facing `extended` route prefix from v1.0.1 endpoint URLs.
- Refreshed dashboard/internal docs discovery so v1.0.1 endpoints appear as combined `GET,POST` catalog entries.
- Refreshed website language switching, localized sitemap entries, and release messaging for v1.0.1.

### Deprecated

- No production endpoint was deprecated in v1.0.1.

## v1.0.0 - Stellar Intelligence Release (April 12, 2026)

### New

- Added 23 extended numerology endpoint families across timing, identity intelligence, spiritual analysis, and relationship dynamics.
- Added 53+ new horoscope/report surfaces across periods, sections, astrology reports, transit, aspect, house, planet, and compatibility areas.
- Expanded the platform to 203+ endpoints at release time, including 130+ horoscope-focused routes.
- Added direct API dashboard, credit, and operational surfaces for production usage.

### Fixes

- Standardized docs and smoke-test coverage across the direct API surface.
- Hardened migration-safe production behavior for dashboard and backend rollout.

### Deprecated

- No production endpoint was deprecated in v1.0.0.

## v0.0.2 - Celestial Expansion (December 13, 2023)

### New

42. **Zodiac Sign Birthday:** Discover the unique personality traits associated with each zodiac sign based on birthdays.
43. **Compatibility Career:** Explore astrological insights into career compatibility between individuals.
44. **Compatibility Friendship:** Gain insights into the dynamics of friendship compatibility based on astrological signs.
45. **Compatibility Love:** Delve into love compatibility insights, providing a deeper understanding of romantic relationships.
46. **Astrology Aspects:** Explore the various aspects and angles between celestial bodies to understand their influence on an individual's life.
47. **Astrology Houses:** Uncover the significance of astrological houses and their impact on different aspects of life.
48. **Astrology Returns:** Explore significant astrological returns, such as the Solar Return and Lunar Return, to gain insights into specific periods of life.
49. **Astrology Terms:** Familiarize yourself with essential astrology terms, creating a foundation for deeper astrological understanding.
50. **Planets Horoscope:** Gain insights into the influence of individual planets on a person's horoscope and life path.
51. **Planets in Houses:** Explore the significance of planets positioned in different astrological houses and their impact on an individual's life.
52. **Mercury Retrograde Effect:** Understand the effects of Mercury retrograde on communication, technology, and daily life.
53. **Saturn Returns Effect:** Explore the transformative effects of Saturn returns on an individual's life path and personal growth.

## v0.0.1 - Cosmic Inception

### Initial Features

1. **Attitude/Sun Number:** Discover the essence of one's personality.
2. **Balance Number:** Uncover the equilibrium in life.
3. **Challenge Number:** Navigate life challenges with precision.
4. **Karmic Debt Number:** Understand and address karmic debts.
5. **Karmic Lesson Numbers:** Learn the lessons embedded in life experiences.
6. **Life Period Cycle Numbers:** Gain insights into life cycles.
7. **Lucky Numbers:** Identify numbers with positive vibes.
8. **Personality Number:** Decode the characteristics defining an individual.
9. **Personal Year Number:** Navigate through yearly influences.
10. **Rational Thought Number:** Explore the intellect's influence.
11. **Soul Expression/Destiny Number:** Reveal the soul's purpose.
12. **Soul Urge Number:** Understand inner desires.
13. **Subconscious Self Number:** Delve into the hidden realms of the psyche.
14. **Analyze a person's phone number:** Uncover numeric vibrations.
15. **Determine Life Path:** Calculate life's journey based on birthdate.
16. **Daily Horoscope (Yesterday, Today, Tomorrow):** Receive personalized daily insights.
17. **Weekly Horoscope:** Plan your week with astrological guidance.
18. **Monthly Horoscope:** Navigate the month ahead with foresight.
19. **Yearly Personal Horoscope:** Gain a holistic view of the year's events.
20. **Love Daily Horoscope:** Explore love insights for yesterday, today, and tomorrow.
21. **Love Weekly Horoscope (Couples, Singles):** Relationship guidance for the week.
22. **Love Monthly Horoscope (Couples, Singles):** Love insights for the month.
23. **Love Yearly Couples Horoscope:** Explore relationship dynamics annually.
24. **Love Yearly Singles Horoscope:** Insights tailored for singles seeking love.
25. **Career Daily Horoscope:** Professional insights for yesterday, today, and tomorrow.
26. **Career Weekly Horoscope:** Plan your workweek with career-focused guidance.
27. **Career Monthly Horoscope:** Navigate your career path for the month.
28. **Career Yearly Horoscope:** Plan your financial and professional trajectory.
29. **Health Daily Horoscope:** Well-being insights for yesterday, today, and tomorrow.
30. **Health Weekly Horoscope:** Plan your week with health-focused guidance.
31. **Health Monthly Horoscope:** Wellness insights for the month.
32. **Planetary Daily Horoscope:** Planetary insights for yesterday, today, and tomorrow.
33. **Planetary Weekly/Monthly Horoscope:** Explore weekly and monthly planetary influences.
34. **Zodiac Sign Personality:** Uncover the unique traits and characteristics of each zodiac sign.
35. **Zodiac Sign Friendship:** Explore the dynamics of friendships based on zodiac signs.
36. **Zodiac Sign Love:** Delve into the romantic aspects of zodiac signs.
37. **Zodiac Sign Lifestyle:** Gain a glimpse into the lifestyle preferences associated with each zodiac sign.
38. **Zodiac Sign Health:** Understand the potential health tendencies and wellness considerations linked to specific zodiac signs.
39. **Zodiac Sign Spirituality:** Explore the spiritual inclinations and tendencies associated with each zodiac sign.
40. **Zodiac Sign Career & Money:** Navigate the professional and financial aspects linked to zodiac signs.
41. **Zodiac Sign Parent & Child:** Explore the dynamics of parenting and child relationships influenced by zodiac signs.
