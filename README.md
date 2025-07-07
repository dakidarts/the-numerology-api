# The Numerology API

![The Numerology API Logo](https://res.cloudinary.com/ds64xs2lp/image/upload/v1731447994/numerologyAPIDevTo_trjxbj.jpg)

Welcome to the official repository for The Numerology API—a powerful tool that combines the ancient wisdom of numerology with the celestial insights of astrology. Whether you're a developer integrating cosmic features into your applications or an enthusiast exploring the mysteries of life, this API is your key to unlocking a universe of knowledge.

> “As within, so without. As in the code, so in the cosmos.” — DWS Numerology API

## Key Features

- 🌌 **Numerological Insights:** Explore personality traits, life challenges, and cycles using Pythagorean numerology methods.
- 🌠 **Horoscope Revelations:** Access daily, weekly, monthly, and yearly horoscopes for love, career, health, and planetary influences.
- 🌟 **Zodiac Wisdom:** Uncover the unique traits of each zodiac sign, from personality and love compatibility to lifestyle choices.

## Getting Started

1. **API Integration:** Explore the comprehensive [documentation](https://dakidarts.com/api/the-numerology-api/) to seamlessly integrate Astro-Numerology features into your applications. You can also [view and test the API on RapidAPI](https://rapidapi.com/kidddevs/api/the-numerology-api).
2. **Contribute:** Join the cosmic journey! Contribute to the development, share insights, and enhance the API for the community.

## Features (v0.0.1)

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

## Added Features (v0.0.2)

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

## New Features (v0.0.3)

**Gematria Calculator:** Added a new endpoint /gematria that computes Gematria values using multiple systems, including:

Ordinal Gematria
Reverse Ordinal Gematria
Pythagorean Gematria
Standard Hebrew Gematria
Hidden Meaning Interpretation: Returns possible symbolic or mystical meanings for certain numerical values.

## v0.0.4 – Cosmic Charts & Customization (April 2025)

### New Features:

#### Birth Chart JSON Endpoint  
**`/birth-chart`**: Returns a full natal chart as structured JSON, including astrological positions, houses, and planetary aspects.

#### Birth Chart SVG Endpoint  
**`/birth-chart/svg`**: Generates and returns a high-quality SVG natal chart image.

- **Supported themes**: `light`, `dark`, `dark-high-contrast`, `classic`  
- **Supported languages**: `EN`, `FR`, `PT`, `IT`, `CN`, `ES`, `RU`, `TR`, `DE`, `HI`

**Note**: This endpoint returns an SVG image `(Content-Type: image/svg+xml)`. RapidAPI’s test console may not display it correctly. Please test the endpoint using a browser, Postman, or in your frontend app. Treat the response as text, not JSON.

![The Numerology API Birth Chart Report](https://res.cloudinary.com/ds64xs2lp/image/upload/v1743891562/birth-chart-report-classic_ti0gjr.jpg)

![The Numerology API Birth Chart Report](https://res.cloudinary.com/ds64xs2lp/image/upload/v1743891566/birth-chart-report-dark_azr2sm.jpg)

### 2025 Support for Year Horoscope  
The `/horoscope/yearly/*` endpoints now includes accurate horoscope calculations for **2025**.  
*(2026 support coming soon!)*

Improvements:

API Performance Optimization: Enhanced query handling and response times for all endpoints.
Better Error Handling: More detailed error messages for invalid inputs.

## 🔮 v0.0.5 – Tarot Readings Are Here! (May 2025)

We're excited to announce the **v0.0.5** release of the **Numerology API**, now enriched with mystical new endpoints that allow users to draw Tarot cards programmatically. Whether you're building a spiritual bot, daily horoscope app, or just love the magic of the cards, this update is for you!

![The Numerology API Tarot Readings](https://res.cloudinary.com/ds64xs2lp/image/upload/v1746950049/Tarot-Reading_waanny.png)

### ✨ What's New

### `/tarot/reading` – Three-Card Tarot Spread  
Dive deep into your **past, present, and future** with a classic 3-card Tarot pull. Each card comes with its upright or reversed meaning and a corresponding image.

**Optional parameter:**
- `mode=random` (default) – Shuffle fresh cards every request  
- `mode=daily` – Get a consistent reading per day

### `/tarot/power` – Single-Card Power Tarot  
A quick yet powerful daily insight. Pull just **one Tarot card** to reveal guidance or affirmation for the moment.  
Same `mode` parameter applies.

## 💥 v0.0.6 – Divine Expansion! (July 7, 2025)

### ✨ What’s New in v0.0.6

We've added **9 transformational new endpoints**, expanding into **affirmations, ancestral decoding, vibrational time tracking**, and more — expanding the spiritual toolkit from 71 to **80 endpoints**!

### 🔢 New Endpoints

| Endpoint | Description |
|----------|-------------|
| `/personal-day` | Returns personal day number & meaning based on DOB + date |
| `/personal-month` | Returns personal month number & meaning |
| `/lucky-days-calendar` | Generates a 9–10 week lucky day calendar |
| `/date-meaning` | Reduces any date (YYYY-MM-DD) into a numerological meaning |
| `/email-numerology` | Decodes numerology energy from an email address |
| `/cornerstone-letter` | Gets the first letter of a name and its cornerstone meaning |
| `/capstone-letter` | Gets the last letter of a first name and its capstone meaning |
| `/ancestor-reading` | Calculates ancestral number & spiritual legacy from family name |
| `/personal-day-affirmations` | Stoic-style daily affirmations based on personal day number |

Each endpoint supports **GET** and **POST** and includes robust **error handling**, `status` codes, and spiritual insights for devs, creators, and seekers.

### 💸 Updated Pricing Plans

We’ve **slashed pricing** and boosted request limits to support more developers, apps, and spiritual platforms.

| Plan      | Old Price → New Price | Old Requests → New Requests |
|-----------|------------------------|------------------------------|
| **Pro**   | `$9.99` → `$9.17`      | `100,000` → `130,000` req/month |
| **Ultra** | `$69.99` → `$63.17`    | `350,000` → `550,000` req/month |
| **Mega**  | `$399.99` → `$369.17`  | `1,000,000` → `2,000,000` req/month |

👉 **Free Plan** still available with up to `100 requests/month`.

## Stay Connected

- 🌐 **Official Website:** [Visit Dakidarts](https://dakidarts.com/api/the-numerology-api/)
- 🐦 **X (Twitter):** [@dakidarts](https://x.com/dakidarts/) - Stay updated with the latest developments and announcements.

Embrace the magic of numbers, stars, and cosmic revelations—start your journey with the Astro-Numerology API today!

🚀 *Empower your applications with cosmic insights!* 🚀
