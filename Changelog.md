# The Numerology API Changelog

## Numerology Expansion + Horoscope Expansion v1.0.0 Unified Changelog

![Full Horoscope Engine Architecture](https://res.cloudinary.com/ds64xs2lp/image/upload/q_auto/f_auto/v1775911991/v1-0-0-release_gdkp0h.svg)

**Release date:** 2026-04-12  
**Version:** v1.0.0  
**Scope:** Full platform release covering **The Numerology API**, **Horoscope Expansion**: including extended endpoint rollout, engine-backed horoscope report migration, request/response normalization, documentation parity, multilingual validation, and production integration guidance.

---

### Overview

v1.0.0 is a major production release across the Dakidarts API platform. It brings together two large tracks of work into one coordinated rollout:

1. **Numerology Expansion**
   - Adds the complete extended numerology surface.
   - Expands timing/cycle coverage with personal week and universal day/week/month/year.
   - Introduces deeper spiritual, relationship, identity, and shadow-analysis endpoints.
   - Completes documentation parity, response examples, and multilingual smoke validation.

2. **Horoscope Expansion**
   - Completes the major migration of horoscope report generation to the in-house Swiss Ephemeris engine.
   - Canonicalizes engine-backed report routes under `/api/v1/horoscope/reports/*`.
   - Adds broad section coverage across daily, weekly, monthly, and yearly periods.
   - Introduces periodized planetary, aspects, transit, and house report suites.
   - Tightens payload consistency, personalization behavior, compatibility aliases, and docs parity.

This changelog is intended to serve as the single source of truth for integrators, internal rollout review, support, migration planning, and customer-facing release communication.

### Platform-Wide Highlights

#### What v1.0.0 delivers across the platform

- Major **v1.0.0 production release** for both Numerology API and Horoscope API.
- Broad expansion of **endpoint surface area** across numerology and horoscope products.
- Completion of **engine-backed horoscope computation migration** for major report flows.
- Completion of the **Extended Numerology** release track.
- Improved **POST-first structured request patterns** for upgraded horoscope routes.
- Broader support for **rich response payloads**, enterprise wrappers, and metadata consistency.
- Stronger **documentation parity** across public docs and example payloads.
- Successful **multilingual smoke validation** for numerology extended endpoints.
- Improved **route clarity**, **compatibility handling**, and **migration guidance** for production clients.
- Expanded support for **personalized calculations** where birth vectors and advanced request fields are provided.
- Improved operational clarity around timezone, zodiac system, ayanamsa, house systems, and node behavior in horoscope request flows.

### Release Composition Summary

#### Numerology Expansion
- New endpoint families added: **23**
- Combined operations added (`GET`/`POST`): **41**
- Validation/smoke requests executed: **205**
- Documented multilingual smoke success: **100.0%**
- Extended release model: **additive**, with no formal deprecations in the new extended suite

#### Horoscope Expansion
- Major report surfaces migrated to the in-house engine
- New report suites added across:
  - planetary
  - aspects
  - transits
  - house
  - planet-house
- Canonical report namespace established under:
  - `/api/v1/horoscope/reports/*`
- Multiple legacy routes retained as hidden compatibility aliases while public docs move forward with canonical paths

## Part I — Numerology API v1.0.0

### Numerology Expansion Highlights

- Added the full **Extended Numerology** surface documented under the extended documentation section.
- Added and completed **Personal Week** with full GET/POST parity and rich response payload support.
- Added and completed **Universal Cycle extensions**:
  - Universal Day
  - Universal Week
  - Universal Month
  - Universal Year
- Standardized extended endpoint docs with complete parameter tables, options, response examples, and related endpoint linking.
- Confirmed multilingual smoke coverage across `en`, `es`, `de`, `fr`, `pt` at **100% success** for extended operations.
- Clarified access model: extended endpoints are **direct-platform only** and are **not currently supported via RapidAPI gateway**.

### Numerology Expansion — New Endpoints Added

This release adds **23 extended endpoint families** and **41 operations** (`GET`/`POST` combined).

#### A) Cycles and Timing Endpoints

| Endpoint | Methods | Path |
|---|---|---|
| Personal Week | `GET`, `POST` | `/api/v1/personal-week` |
| Universal Year | `GET`, `POST` | `/api/v1/universal-year` |
| Universal Month | `GET`, `POST` | `/api/v1/universal-month` |
| Universal Week | `GET`, `POST` | `/api/v1/universal-week` |
| Universal Day | `GET`, `POST` | `/api/v1/universal-day` |
| Monthly Energy Heatmap | `GET`, `POST` | `/api/v1/monthly-energy-heatmap` |
| Caution Dates Calendar | `GET`, `POST` | `/api/v1/caution-dates-calendar` |

#### B) Identity and Name Intelligence Endpoints

| Endpoint | Methods | Path |
|---|---|---|
| Username Numerology | `GET`, `POST` | `/api/v1/username-numerology` |
| Business Name Numerology | `GET`, `POST` | `/api/v1/business-name-numerology` |
| Brand Name Compare | `POST` | `/api/v1/brand-name-compare` |
| Name Change Impact | `GET`, `POST` | `/api/v1/name-change-impact` |
| Date Alignment Check | `GET`, `POST` | `/api/v1/date-alignment-check` |

#### C) Spiritual and Shadow Analysis Endpoints

| Endpoint | Methods | Path |
|---|---|---|
| Aura Frequency Reading | `GET`, `POST` | `/api/v1/aura-frequency-reading` |
| Chakra Numerology | `GET`, `POST` | `/api/v1/chakra-numerology` |
| Past Life Patterns | `GET`, `POST` | `/api/v1/past-life-patterns` |
| Shadow Work Number | `GET`, `POST` | `/api/v1/shadow-work-number` |
| Soul Contract Reading | `GET`, `POST` | `/api/v1/soul-contract-reading` |
| Soul Connection Indicator | `POST` | `/api/v1/soul-connection-indicator` |
| Spiritual Gifts Reading | `GET`, `POST` | `/api/v1/spiritual-gifts-reading` |
| Sacred Balance Reading | `GET`, `POST` | `/api/v1/sacred-balance-reading` |

#### D) Relationship Dynamics Endpoints

| Endpoint | Methods | Path |
|---|---|---|
| Relationship Composite | `POST` | `/api/v1/relationship-composite` |
| Relationship Healing Reading | `POST` | `/api/v1/relationship-healing-reading` |
| Parent Child Numerology | `POST` | `/api/v1/parent-child-numerology` |

### Numerology API — Updated and Fixed Endpoints

#### A) Newly Completed Core Extended Surfaces

The following newly introduced surfaces were completed end-to-end in this release cycle with request validation and rich meaning output:

- `GET /api/v1/personal-week`
- `POST /api/v1/personal-week`
- `GET /api/v1/universal-year`
- `POST /api/v1/universal-year`
- `GET /api/v1/universal-month`
- `POST /api/v1/universal-month`
- `GET /api/v1/universal-week`
- `POST /api/v1/universal-week`
- `GET /api/v1/universal-day`
- `POST /api/v1/universal-day`

#### B) Stability Fixes Applied During Smoke Validation

Five operations that initially produced `422` under generated smoke inputs were stabilized for production-like test input coverage and now return successful responses under multilingual smoke:

- `POST /api/v1/brand-name-compare`
- `GET /api/v1/caution-dates-calendar`
- `POST /api/v1/caution-dates-calendar`
- `GET /api/v1/monthly-energy-heatmap`
- `POST /api/v1/monthly-energy-heatmap`

#### C) Practical Validation Rules Reinforced

The following constraints were tightened and clarified during validation and documentation work:

- Brand compare requires at least **two entries** in `names[]`.
- Calendar and heatmap month inputs use the `YYYY-MM` format.
- Caution dates `top_n` remains bounded to the range **`1..31`**.
- Client payloads benefit from prevalidation before submission to reduce avoidable `422` or format-level errors.

#### D) Documentation and OpenAPI Parity Fixes

All extended docs were normalized for integration parity:

- complete parameter tables per method
- parameter option details
- patterns, ranges, defaults, and nested object fields
- rich response example sections based on smoke-generated payloads
- standardized access and availability notes
- dashboard CTA, note sections, and related endpoint footers

### Numerology API — QA Verification Snapshot

Validation artifacts for the extended numerology suite:

- Summary files: **23**
- Operations tested: **41**
- Total requests executed: **205**
- Overall success rate: **100.0%**
- Language success:
  - `en` — 100%
  - `es` — 100%
  - `de` — 100%
  - `fr` — 100%
  - `pt` — 100%

This release closes the extended numerology launch cycle with production-ready validation confidence across the documented language set.


### Numerology API — Deprecations

For the **Numerology Extended v1.0.0** release, no endpoint in the extended surface is formally deprecated.

| Endpoint | Status in v1.0.0 | Replacement | Notes |
|---|---|---|---|
| None | Not applicable | Not applicable | Extended suite is additive in this release. |


### Numerology API — Breaking Changes

No breaking path removals are introduced for the extended numerology surface in this release.

That said, integrators should note the following rollout-level expectations:

- Extended endpoints are **not available through RapidAPI** at this time.
- Clients integrating extended endpoints should target the direct platform host.
- Some new endpoints are `POST`-only by design and should not be assumed to have `GET` parity.

### Numerology API — Migration Notes

#### 1) Access Channel Migration

Extended endpoints are available via direct platform access:

- Base URL: `https://api.numerologyapi.com`
- Authentication:
  - `X-API-Key: YOUR_API_KEY`
  - or `Authorization: Bearer YOUR_API_KEY`

Extended endpoints are currently **not supported via RapidAPI gateway**.

#### 2) GET vs POST Usage Guidance

Most extended endpoints support both `GET` and `POST` with equivalent output intent.

Use:

- `GET` for simple query-based calls
- `POST` for stronger payload structure, nested objects, and SDK/backend consistency

Post-only endpoints in this release include:

- `/api/v1/brand-name-compare`
- `/api/v1/relationship-composite`
- `/api/v1/relationship-healing-reading`
- `/api/v1/parent-child-numerology`
- `/api/v1/soul-connection-indicator`

#### 3) Client-Side Input Validation Rules

Recommended client-side prevalidation:

- `dob` and `target_date`: `YYYY-MM-DD`
- `month`: `YYYY-MM`
- `timezone_offset`: valid IANA timezone string
- `top_n`: integer in range `1..31`
- `names[]`: minimum of 2 entries for brand compare
- `context` for date alignment: max length `80`, normalized aliases accepted

#### 4) Nested Request Body Patterns

For relationship and compatibility endpoints, use explicit nested objects such as:

- `person_a`
- `person_b`
- `parent`
- `child`

Each object should include required fields such as:

- `full_name`
- `dob`

#### 5) Language and Metadata Handling

Extended numerology endpoints support multilingual response rendering via `lang`.

Supported language set for smoke-verified coverage:

- `en`
- `es`
- `de`
- `fr`
- `pt`

Responses may include enterprise-style metadata wrappers:

- `_enterprise`
- `_api_metadata_`

Clients should preserve and parse these fields where useful for platform analytics, plan information, or endpoint metadata.

#### 6) Newly Added Cycle Coverage

Clients previously using only personal day/month/year flows can now extend schedule logic to cover:

- weekly personal cycles via `/api/v1/personal-week`
- collective timing surfaces via:
  - `/api/v1/universal-day`
  - `/api/v1/universal-week`
  - `/api/v1/universal-month`
  - `/api/v1/universal-year`

#### 7) Documentation Source of Truth

The full endpoint-level integration pages for this release are maintained under the extended documentation section, including index and per-endpoint pages.

### Numerology API — Recommended Upgrade Checklist

- Move extended calls to direct API access at `https://api.numerologyapi.com`.
- Ensure request validators enforce date, month, and timezone formats.
- Add fallback handling for multilingual `lang` values where needed.
- Update clients to parse `_enterprise` and `_api_metadata_` consistently.
- For nested endpoints, align SDK request models to required object keys.
- Validate against smoke fixtures before promoting to production.
- Confirm all extended calls are routed outside RapidAPI-based client assumptions.

### Numerology API — Release Notes Summary

Numerology API v1.0.0 introduces the complete extended numerology surface with weekly and universal cycle expansion, advanced relationship and spiritual analyses, richer request/response contracts, and fully synchronized documentation plus smoke-test parity.

## Part II — Horoscope Expansion v1.0.0

### Horoscope Expansion Highlights

- Completed migration of major horoscope report flows to the in-house Swiss Ephemeris engine.
- Standardized upgraded report endpoints around **POST-first request bodies**.
- Added broad **section-first coverage** across daily, weekly, monthly, and yearly periods.
- Restructured **planetary report endpoints** by period and section/overview parity.
- Renamed the planets glossary endpoint to reflect its **informational** behavior rather than report behavior.
- Expanded natal birth chart request parity and tightened response-shape validation.
- Normalized upgraded endpoint responses to engine payload plus enterprise metadata wrappers.
- Updated public docs examples with smoke-backed JSON parity.

### Horoscope Expansion — New Endpoints Added

#### A) New Helper and Canonical Surfaces

- `GET /api/v1/horoscope/timezones`

#### B) Planetary Report Suite (Periodized Surface)

Sections (non-general):

- `POST /api/v1/horoscope/reports/planetary/daily`
- `POST /api/v1/horoscope/reports/planetary/weekly`
- `POST /api/v1/horoscope/reports/planetary/monthly`
- `POST /api/v1/horoscope/reports/planetary/yearly`

Overview (general-only):

- `POST /api/v1/horoscope/reports/planetary/daily/overview`
- `POST /api/v1/horoscope/reports/planetary/weekly/overview`
- `POST /api/v1/horoscope/reports/planetary/monthly/overview`
- `POST /api/v1/horoscope/reports/planetary/yearly/overview`

Expanded planetary section coverage across periods includes engine-supported sections such as:

- `communication`
- `friendship`
- `lifestyle`
- `career`
- `health`
- `money`
- `love_singles`
- `love_couples`

#### C) Aspect Report Suite (Periodized Surface)

Sections (non-general):

- `POST /api/v1/horoscope/reports/aspects/daily`
- `POST /api/v1/horoscope/reports/aspects/weekly`
- `POST /api/v1/horoscope/reports/aspects/monthly`
- `POST /api/v1/horoscope/reports/aspects/yearly`

Overview (general-only):

- `POST /api/v1/horoscope/reports/aspects/daily/overview`
- `POST /api/v1/horoscope/reports/aspects/weekly/overview`
- `POST /api/v1/horoscope/reports/aspects/monthly/overview`
- `POST /api/v1/horoscope/reports/aspects/yearly/overview`

`aspects/*` supports:

- public mode
- personalized mode
- optional deterministic `aspect` override
- the same section model used across upgraded horoscope routes

#### D) Transit Report Suite (Periodized Surface)

Sections (non-general):

- `POST /api/v1/horoscope/reports/transits/daily`
- `POST /api/v1/horoscope/reports/transits/weekly`
- `POST /api/v1/horoscope/reports/transits/monthly`
- `POST /api/v1/horoscope/reports/transits/yearly`

Overview (general-only):

- `POST /api/v1/horoscope/reports/transits/daily/overview`
- `POST /api/v1/horoscope/reports/transits/weekly/overview`
- `POST /api/v1/horoscope/reports/transits/monthly/overview`
- `POST /api/v1/horoscope/reports/transits/yearly/overview`

`transits/*` supports:

- public mode
- personalized mode
- optional deterministic `transit` override
- the same section model used across upgraded horoscope routes

#### E) House Report Suite (Personalized-Only, Periodized Surface)

House reports (non-general sections):

- `POST /api/v1/horoscope/reports/house/daily`
- `POST /api/v1/horoscope/reports/house/weekly`
- `POST /api/v1/horoscope/reports/house/monthly`
- `POST /api/v1/horoscope/reports/house/yearly`

House overviews (general-only):

- `POST /api/v1/horoscope/reports/house/daily/overview`
- `POST /api/v1/horoscope/reports/house/weekly/overview`
- `POST /api/v1/horoscope/reports/house/monthly/overview`
- `POST /api/v1/horoscope/reports/house/yearly/overview`

Planet-house reports (non-general sections):

- `POST /api/v1/horoscope/reports/planet/house/daily`
- `POST /api/v1/horoscope/reports/planet/house/weekly`
- `POST /api/v1/horoscope/reports/planet/house/monthly`
- `POST /api/v1/horoscope/reports/planet/house/yearly`

Planet-house overviews (general-only):

- `POST /api/v1/horoscope/reports/planet/house/daily/overview`
- `POST /api/v1/horoscope/reports/planet/house/weekly/overview`
- `POST /api/v1/horoscope/reports/planet/house/monthly/overview`
- `POST /api/v1/horoscope/reports/planet/house/yearly/overview`

Both route families are **personalized-only** and are backed by engine endpoints such as:

- `/house-horoscope`
- `/planet-house-horoscope`

#### F) Report Namespace Canonicalization

Canonical live-report paths now use the `/api/v1/horoscope/reports/*` namespace across upgraded engine-backed horoscope surfaces.

Legacy non-report paths remain registered as hidden compatibility aliases.

#### G) Newly Added Horoscope Section Route Families Across Periods

##### Communication

- `POST /api/v1/horoscope/reports/communication/daily/today`
- `POST /api/v1/horoscope/reports/communication/daily/tomorrow`
- `POST /api/v1/horoscope/reports/communication/daily/yesterday`
- `POST /api/v1/horoscope/reports/communication/weekly`
- `POST /api/v1/horoscope/reports/communication/monthly`
- `POST /api/v1/horoscope/reports/communication/yearly`

##### Friendship

- `POST /api/v1/horoscope/reports/friendship/daily/today`
- `POST /api/v1/horoscope/reports/friendship/daily/tomorrow`
- `POST /api/v1/horoscope/reports/friendship/daily/yesterday`
- `POST /api/v1/horoscope/reports/friendship/weekly`
- `POST /api/v1/horoscope/reports/friendship/monthly`
- `POST /api/v1/horoscope/reports/friendship/yearly`

##### Lifestyle

- `POST /api/v1/horoscope/reports/lifestyle/daily/today`
- `POST /api/v1/horoscope/reports/lifestyle/daily/tomorrow`
- `POST /api/v1/horoscope/reports/lifestyle/daily/yesterday`
- `POST /api/v1/horoscope/reports/lifestyle/weekly`
- `POST /api/v1/horoscope/reports/lifestyle/monthly`
- `POST /api/v1/horoscope/reports/lifestyle/yearly`

##### Love Split Surfaces (Singles/Couples)

- `POST /api/v1/horoscope/reports/love_singles/daily/today`
- `POST /api/v1/horoscope/reports/love_singles/daily/tomorrow`
- `POST /api/v1/horoscope/reports/love_singles/daily/yesterday`
- `POST /api/v1/horoscope/reports/love_singles/weekly`
- `POST /api/v1/horoscope/reports/love_singles/monthly`
- `POST /api/v1/horoscope/reports/love_couples/daily/today`
- `POST /api/v1/horoscope/reports/love_couples/daily/tomorrow`
- `POST /api/v1/horoscope/reports/love_couples/daily/yesterday`
- `POST /api/v1/horoscope/reports/love_couples/weekly`
- `POST /api/v1/horoscope/reports/love_couples/monthly`

##### Yearly Section Additions

- `POST /api/v1/horoscope/reports/health/yearly`
- `POST /api/v1/horoscope/reports/money/yearly`

#### H) Renamed Informational Planets Surface

- `GET /api/v1/horoscope/planets-info`
- `POST /api/v1/horoscope/planets-info`

This replaces the prior `/horoscope/planets` naming for the informational glossary-style behavior.

### Horoscope Expansion — Updated and Fixed Endpoints

#### A) Engine Migration and Behavior Updates

The following existing route families were upgraded to in-house engine-backed behavior:

##### Main report routes
- `POST /api/v1/horoscope/reports/today`
- `POST /api/v1/horoscope/reports/yesterday`
- `POST /api/v1/horoscope/reports/tomorrow`
- `POST /api/v1/horoscope/reports/weekly`
- `POST /api/v1/horoscope/reports/monthly`
- `POST /api/v1/horoscope/reports/yearly`

##### Existing category routes upgraded from legacy horoscope.com-backed behavior
- career
- health
- love
- money

##### Existing and legacy families restructured and upgraded
- legacy love routes split into `love_singles` and `love_couples`
- combined `yearly/career_money` behavior replaced by dedicated yearly career and yearly money routes
- planetary legacy report and overview routes moved to periodized routes

#### B) Zodiac Sign Description Route Clarification

The following surfaces remain descriptive sign endpoints rather than live-report endpoints:

- `/api/v1/horoscope/sign/personality`
- `/api/v1/horoscope/sign/communication`
- `/api/v1/horoscope/sign/friendship`
- `/api/v1/horoscope/sign/love`
- `/api/v1/horoscope/sign/lifestyle`
- `/api/v1/horoscope/sign/health`
- `/api/v1/horoscope/sign/career`
- `/api/v1/horoscope/sign/money`
- `/api/v1/horoscope/sign/parent_child`
- `/api/v1/horoscope/sign/spirituality`
- `/api/v1/horoscope/sign/shadow`

#### C) Birthday Horoscope Parity Update

`POST /api/v1/horoscope/reports/birthday` now exposes engine-native request keys while retaining compatibility keys.

Canonical upgraded surface:

- `POST /api/v1/horoscope/reports/birthday`

Hidden compatibility aliases retained:

- `/api/v1/horoscope/birthday`
- `/api/v1/horoscope/sign/birthday`

Engine-native request keys exposed:

- `sign`
- `target_date`
- `birth`
- `sections`
- `zodiac_system`
- `ayanamsa`
- `house_system`
- `node_type`
- `tenant_id`

Compatibility keys retained:

- `dob`
- `timezone`
- `year`
- `birth_time`
- `birth_latitude`
- `birth_longitude`
- `birth_timezone`

#### D) Natal Birth Chart Parity Update

These surfaces existed prior to v1.0.0 and are now upgraded for fuller engine parity:

- `POST /api/v1/birth-chart`
- `POST /api/v1/birth-chart/svg`

Improvements include:

- fuller gateway-to-engine request option support
- wheel configuration field parity
- stricter response-shape guards

#### E) Response Contract Normalization

Upgraded horoscope engine-backed endpoints return:

- raw engine response payload
- `_enterprise`
- `_api_metadata_`

#### F) Timezone and Relative-Day Handling

Daily endpoints using `today`, `yesterday`, and `tomorrow` now apply timezone-aware target-date resolution via IANA timezone input.

#### G) Personalization Support Clarification

Where supported, personalized reports are activated by providing birth-vector fields such as:

- `birth_time`
- `birth_latitude`
- `birth_longitude`
- `birth_timezone`

If omitted, routes remain usable in generalized sign-based mode.

### Horoscope Expansion — Deprecated, Hidden, and Removed Endpoints

| Endpoint | Status in v1.0.0 | Replacement | Notes |
|---|---|---|---|
| Legacy planetary aggregate report route | Removed | Period routes under `/reports/planetary/` with period-specific paths plus matching `/overview` routes | Aggregate entrypoint removed after periodized parity completion. |
| `POST /api/v1/horoscope/planetary/overview` | Deprecated (hidden from OpenAPI) | `POST /api/v1/horoscope/reports/planetary/daily/overview`, `POST /api/v1/horoscope/reports/planetary/weekly/overview`, `POST /api/v1/horoscope/reports/planetary/monthly/overview`, `POST /api/v1/horoscope/reports/planetary/yearly/overview` | Replaced by period-specific overview routes. |
| `POST /api/v1/horoscope/planetary/daily/sections` | Hidden alias | `POST /api/v1/horoscope/reports/planetary/daily` | Internal compatibility alias. |
| `POST /api/v1/horoscope/love_single/monthly` | Deprecated alias (hidden) | `POST /api/v1/horoscope/reports/love_singles/monthly` | Kept for compatibility. |
| `POST /api/v1/horoscope/weekly/retail` | Deprecated (hidden from OpenAPI/docs) | None | Weekly retail surface retired from public docs. |
| Legacy flexible aggregate horoscope route | Removed | Section-specific report routes and period overview routes | Aggregate entrypoint removed after full endpoint split. |
| `POST /api/v1/horoscope/yearly/career_money` | Removed | `POST /api/v1/horoscope/reports/career/yearly` and `POST /api/v1/horoscope/reports/money/yearly` | Combined endpoint split into dedicated routes. |
| `POST /api/v1/horoscope/love/{today,tomorrow,yesterday}` | Removed active registration | `POST /api/v1/horoscope/reports/love_singles/daily/{today,tomorrow,yesterday}` or `POST /api/v1/horoscope/reports/love_couples/daily/{today,tomorrow,yesterday}` | Daily love is now split by relationship context. |
| `GET /api/v1/horoscope/planets` and `POST /api/v1/horoscope/planets` | Renamed/removed | `GET /api/v1/horoscope/planets-info` and `POST /api/v1/horoscope/planets-info` | Informational endpoint rename for clarity. |


### Horoscope Expansion — Breaking Changes

- Route rename: `/api/v1/horoscope/planets` → `/api/v1/horoscope/planets-info`
- Canonical namespace for live engine-backed horoscope reports is now `/api/v1/horoscope/reports/*`
- Combined daily love routes replaced by explicit singles and couples paths
- Combined yearly `career_money` route removed in favor of dedicated yearly routes
- Planetary generic report and overview endpoints deprecated in favor of period-structured routes
- Upgraded engine-backed routes standardized around POST-first request bodies

### Horoscope Expansion — Compatibility Notes

- Legacy `/api/v1/horoscope/report/*` routes remain available as hidden backward-compatible aliases
- Public docs and OpenAPI now present only the canonical `/api/v1/horoscope/reports/*` namespace
- New integrations should adopt `/reports/*` paths immediately

### Horoscope Expansion — Migration Notes

#### 1) Endpoint Path Migration Map

- `GET/POST /api/v1/horoscope/planets` → `GET/POST /api/v1/horoscope/planets-info`
- `POST /api/v1/horoscope/report/{surface}` → `POST /api/v1/horoscope/reports/{surface}`
- `POST /api/v1/horoscope/{surface}` → `POST /api/v1/horoscope/reports/{surface}`
- `POST /api/v1/horoscope/planetary/overview` → `POST /api/v1/horoscope/reports/planetary/{period}/overview`
- legacy planetary aggregate route → `POST /api/v1/horoscope/reports/planetary/{period}` or overview equivalent
- legacy flexible aggregate horoscope route → section-specific routes or overview routes
- `POST /api/v1/horoscope/yearly/career_money` → split into yearly career and yearly money routes
- legacy love daily routes → split into `love_singles` or `love_couples` daily routes

#### 2) Request Payload Migration

For upgraded engine-backed routes, use structured POST bodies with fields such as:

- `dob`
- `timezone`
- period selectors such as `day`, `target_date`, or `year`
- optional engine options:
  - `zodiac_system`
  - `ayanamsa`
  - `house_system`
  - `node_type`
  - `tenant_id`
- optional personalization fields:
  - `birth_time`
  - `birth_latitude`
  - `birth_longitude`
  - `birth_timezone`

#### 3) Planetary Route Migration Rules

- use `sections` only on non-overview planetary period routes
- `general` is exposed via dedicated `/overview` routes

#### 4) Response Parser Migration

Clients should parse:

- report payload fields directly from the response body
- `_enterprise`
- `_api_metadata_`

#### 5) Translation Behavior Note

The horoscope engine itself does not generate multilingual content directly, so report based endpoints currently support but `en` only.

Non-report endpoints continue to support full multilingual translation through gateway helper layers using `lang`, such as:

- `en`
- `es`
- `de`
- `fr`
- `pt`


### Horoscope Expansion — Documentation and QA Parity Completed

- Public docs updated for upgraded horoscope routes
- Legacy planetary docs replaced by period-specific planetary docs
- Career and money docs split where combined routes were removed
- Smoke-backed example JSON synchronized with endpoint responses for upgraded docs


### Horoscope Expansion — Recommended Client Upgrade Checklist

- Update all renamed and deprecated paths using the migration map
- Switch any legacy GET consumers of upgraded report routes to POST body requests
- Add timezone to all daily flows to avoid relative-date drift
- Add personalization fields where user-specific editorials are desired
- Update response parsers to retain `_enterprise` and `_api_metadata_`
- Re-run integration tests against all horoscope endpoints used in production


### Horoscope Expansion — Release Notes Summary

Numerology API v1.0.0 completes a major engine-parity rollout, expands report coverage across sections and periods, introduces cleaner canonical route structure, and establishes a clearer production surface for future iterations of the in-house horoscope engine.

## Part III — Cross-API Integration Guidance

### Unified Integration Notes for Clients Using The Numerology API

Clients that consume both Numerology endpoints and Horoscope endpoints should review the following together:

#### Authentication and Access
- Numerology extended endpoints are direct-platform only (no RapidAPI gateway support)
- Engine backed horoscope routes are also direct-platform only and continue under their canonical API namespace with upgraded gateway patterns
- Preserve support for enterprise-style metadata wrappers

#### Request Modeling
- Prefer explicit structured POST bodies for all newly upgraded or expanded routes
- Validate date formats, period selectors, timezone strings, and nested objects client-side
- Where available, supply personalization vectors for richer outputs

#### Timezone and Date Semantics
- Numerology endpoints depend on correct date and month formats
- Horoscope daily routes depend on correct timezone handling for relative-day resolution
- IANA timezone strings are strongly recommended where supported

#### Language Handling
- Numerology extended endpoints have smoke-verified multilingual rendering
- Engine backed horoscope routes continue to support `en` only

#### Production Rollout Advice
- update SDKs and request validators first
- refresh integration tests second
- then promote route/path changes to production clients
- monitor any hidden compatibility aliases still in use internally so they can be retired later with confidence

## Part IV — Final Release Summary

### What v1.0.0 means

v1.0.0 is the point where both surfaces become substantially more complete and production-shaped:

- **Numerology API** now exposes a far richer extended catalog spanning timing, identity, spiritual insight, shadow work, relationships, compatibility, and predictive calendars.
- **Horoscope reports** now stand on a much stronger engine-backed foundation with canonical report namespaces, broader section coverage, clearer migration patterns, and better parity across report families.
- Documentation, examples, validation behavior, and compatibility guidance are significantly more mature than in the pre-v1.0.0 state.

This release is not just a version bump. It is a structural release that improves:

- platform completeness
- route clarity
- client migration readiness
- documentation confidence
- enterprise integration consistency

---

### Operational Recommendation

For all active integrators, the recommended path is:

1. adopt canonical routes immediately
2. update request models for POST-first payloads where applicable
3. preserve metadata wrapper parsing
4. validate timezone/date formats client-side
5. move numerology extended consumers to direct platform access
6. re-run full integration smoke coverage before production rollout

### Closing Note

This unified changelog reflects the v1.0.0 release state for **The Numerology API** and consolidates the major rollout work completed for the **2026-04-12** release window.


## 🚀 v0.1.1 — “The Conscious Expansion Release”
**Release Date:** Jan 10, 2026


### 🌌 Overview

Version **v0.1.1** marks a **major evolutionary leap** for the Numerology & Astrology API.

This release goes far beyond new endpoints — it represents a **deep refinement of the entire system**, transforming the API from a numerical calculator into a **conscious intelligence engine** delivering rich, themed, and human-centered insights.

All **core numerology endpoints (17+)** have been enhanced to return **context-aware, spiritually grounded, and clarity-driven responses**, making the API more intuitive, insightful, and valuable for real-world use cases.

### ✨ What’s New

#### 🔮 New Endpoints (5 Added)

The following **premium report endpoints** were introduced, expanding the API into **relationship, cycle, and life-pattern intelligence**:

1. **Personal Cycle Report**
   - Combines **Personal Year** and **Universal Year** cycles
   - Explains how individual energy interacts with the collective timeline
   - Designed for clarity, planning, and conscious decision-making

2. **Lifestyle Compatibility Report**
   - Analyzes daily habits, routines, social life, and living dynamics
   - Ideal for couples, co-living partners, and long-term alignment

3. **Communication Compatibility Report**
   - Explores expression styles, listening quality, conflict resolution, and emotional intelligence
   - Focuses on how conversations actually flow between two people

4. **Growth & Evolution Compatibility Report**
   - Examines mutual growth potential, change support, and spiritual or personal evolution
   - Built for conscious relationships and long-term transformation

5. **Financial Compatibility Report**
   - Analyzes money mindset, risk tolerance, wealth-building potential, and financial dynamics
   - Ideal for couples, spouses, and business collaborators


#### 🧠 Core API Enhancements

- ✅ **17+ core numerology endpoints upgraded**
- 🎨 All responses now return **themed, content-rich interpretations**
- 📖 Improved clarity and narrative flow for end users
- 🌱 More human, intuitive, and spiritually grounded insights
- 🧩 Consistent structure across all endpoints for easier integration

These upgrades significantly improve:
- User understanding
- Client-facing report quality
- Coaching, spiritual, and advisory applications


##  🚀 v0.1.0 — “The Galactic Blueprint Release” (Oct 29, 2025)

The **Dakidarts Numerology API** reaches its **first major milestone** — crossing **100 powerful endpoints**.
This release expands the numerological universe with *deeper spiritual analytics* and *premium cosmic insights* for advanced users and developers.

### ✨ **New Endpoints (v0.1.0)**

Unlock 10 advanced numerology tools for deeper personality and life-path decoding:

| Endpoint            | Description                                                                                                    |
| ------------------- | -------------------------------------------------------------------------------------------------------------- |
| `/birth-day-number` | Returns the **Birth Day Number** and its meaning (based purely on the day of birth).                           |
| `/life-essence`     | Combines **Life Path + Soul Urge + Expression** for a unified vibration summary — your core essence blueprint. |

#### 🌌 Cycles & Transits

| Endpoint         | Description                                                                                           |
| ---------------- | ----------------------------------------------------------------------------------------------------- |
| `/essence-cycle` | Calculates your **Essence Cycles**, showing numerological influence patterns across life periods.     |
| `/transits`      | Returns **letter-based transits** derived from name vibrations, revealing yearly personal influences. |

#### 🌠 Minor Numbers (Hidden Aspects)

| Endpoint              | Description                                                              |
| --------------------- | ------------------------------------------------------------------------ |
| `/minor-personality`  | Reveals how your **short name / nickname** shapes external impressions.  |
| `/minor-heart-desire` | Shows inner emotional drives derived from **vowels in your short name**. |
| `/minor-expression`   | Shows outer expression derived from the **full short name** vibration.   |

#### 🧩 Bridge Numbers (Connections Between Vibrations)

| Endpoint                    | Description                                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------------------------------------ |
| `/life-expression-bridge`   | Bridge between **Life Path & Expression** — reveals how your purpose meets your talents.                     |
| `/life-birthday-bridge`     | Bridge between **Life Path & Birth Day** — shows how to harmonize core life goals with natural gifts.        |
| `/heart-personality-bridge` | Bridge between **Heart’s Desire & Personality** — shows alignment between inner emotions and outer behavior. |

### ⚙️ Improvements

* **Unified GET & POST Support:** Every endpoint supports both GET and POST requests for maximum flexibility.
* **Enhanced Error Handling:** Cleaner, consistent error responses across all endpoints.

### 🧠 Stats Snapshot

* **Total Endpoints:** 100
* **Premium Endpoints:** 10
* **Release Date:** Oct 29, 2025
* **Codename:** *“The Galactic Blueprint Release”*

### 📜 Example (Birth Day Endpoint)

**Endpoint:** `/birth-day`
**Methods:** `GET`, `POST`

**Parameters:**

```json
{
  "birthdate": "1998-04-27"
}
```

**Response:**

```json
{
  "birth_day_number": 27,
  "keyword": "The Humanitarian Sage",
  "meaning": "Compassionate, wise, and a spiritual guide for the collective.",
  "detailed_meaning": "27 reduces to 9 with a strong 7 overlay. You merge analytical depth with universal love, often drawn to teaching, writing, or healing on a large scale. Your soul’s mission is enlightenment through service. Shadow work: release perfectionism; imperfect action still moves the world.",
  "status": 200
}
```

### 🌠 Closing Note

Stay tuned for **v0.1.1 — “The Astral Continuum Release”**

## 🚀 v0.0.9 — “The Ascension Pathway Release”

**Release Date:** September 27, 2025
**Version:** 0.0.9

### ✨ New Endpoints

#### 1️⃣ Personal Hour

* **Endpoint:** `/personal-hour`
* **Description:** Calculate the personal hour number based on a user’s birthdate, target date, and timezone.
* **Features:**

  * Supports `GET` and `POST`.
  * Optional `target_date` parameter (`YYYY-MM-DD`). Defaults to current date.
  * Optional `timezone_offset` (default: `Europe/Paris`).
  * Returns **single-digit numerology** for the hour, meaning, and 4-line detailed meaning.

#### 2️⃣ Numerology Compatibility Score

* **Endpoint:** `/compatibility-score`
* **Description:** Compare numerology numbers of two people for relationship insights.
* **Features:**

  * Calculates **Life Path, Heart’s Desire, Personality, Hidden Passion, Attitude, Balance, Subconscious Self, Rational Thought, Destiny** numbers.
  * Full names are merged before calculating **Hidden Passion**.
  * Returns individual scores, overall compatibility, and textual insights.
  * Supports `GET` query parameters and `POST` JSON body.

#### 3️⃣ Angel Number Synchronicities

* **Endpoint:** `/angel-number-sync`
* **Description:** Returns meanings for repeating digits or mirrored angel number patterns.
* **Features:**

  * Detects repeated digits (e.g., `1111`, `2222`).
  * Detects mirrored patterns (e.g., `1221`, `1212`).
  * Reduces number to core numerology vibration and returns **base meaning**, **detailed meaning**, and **synchronicity insight**.
  * Supports both `GET` and `POST`.


### 🔄 Updated Endpoints

* **Personal Day** `/personal-day`

  * Added optional `timezone_offset` parameter.
  * Uses user-local time for accurate personal day calculation.

* **Personal Month** `/personal-month`

  * Added optional `timezone_offset` parameter.
  * Ensures personal month calculation aligns with user’s local date.


### ⚡ Improvements

* All numerology endpoints now consistently return:
  * `meaning`
  * `detailed_meaning` (expanded descriptions)
* Timezone handling added for **personal day, personal month, and personal hour** to ensure local accuracy.
* Improved error handling for invalid dates, timezones, and missing parameters.


### 📌 Notes

* Master numbers (11, 22, 33) are supported where relevant.
* Personal hour only uses **single-digit numerology**.

🔥 **v0.0.9 marks our most comprehensive numerology release yet — local timezone support, compatibility insights, angel synchronicities, and richer detailed meanings across the board!**

## 🚀 v0.0.8 — “The Mirror Dimension Release” (September, 2025)

We step through the looking glass. v0.0.8 introduces **mirror-based numerology** — unlocking the hidden balance and reflective cycles between numbers. This release reveals how numbers mirror each other, form energetic loops, and guide us through transformation.

Check out the full research here: [Research Paper: Mirror Numbers and Cycles Research Paper](https://dakidarts.com/p/mirror-numbers-and-circles-novel-extensions-in-numerological-analysis/)

![HPPN & Gap Resonance Release Paper](https://res.cloudinary.com/ds64xs2lp/image/upload/v1757113153/Mirror-Numbers-Formula_vqm8j1.jpg)

#### ✨ New Endpoints in v0.0.8

#### 1️⃣ `/mirror-numbers` 💡

Returns the **Mirror Grid** — mapping each number (1–9, 11, 22, 33) to its reflective counterpart.

* Supports both `GET` & `POST`.
* Input: `base` (optional) → single number analysis, or full grid if omitted.
* Input: `expanded` (optional bool) → adds **detailed meaning + cycles**.
* Output: mirror number, keyword, meaning, and (if expanded) detailed meaning, cycles, and cycle keywords.

#### 2️⃣ `/mirror-path` 💡

Projects your **Mirror Path & Cycles** from a given birth date or base number.

* Shows how your numbers reflect into one another over time.
* Returns **mirror transitions**, cycle loops, and meanings.
* Useful for tracing karmic reflections and life balance themes.
* Supports both `GET` & `POST`.

### 🔧 Notes & Improvements

* Added **expanded analysis mode** with cycle tracing.
* Unified reduction logic for base numbers (respects master numbers 11, 22, 33).
* Full error handling with status codes and descriptive error messages.
* All responses return **keywords, meanings, and detailed meanings** where available.

### 🌟 Use this Release

* Explore the **mirror dimension of numerology** — see how numbers reflect hidden aspects of the self.
* Trace **cycles and loops** for deeper karmic insight.
* Integrate **mirror grid + mirror path** into spiritual apps, coaching tools, and personal dashboards.
* Unlock new guidance for balance, duality, and transformation.


## 🚀 v0.0.7 — *“The Awakening Release”* (August, 2025)

We’re leveling up! v0.0.7 introduces **5 brand new endpoints**, expanding insights into personal numerology, life cycles, and hidden patterns in names. The spiritual toolkit now supports up to **85 endpoints**!

This release also **includes our groundbreaking discovery** by Etuge Anselm E. — the **Hidden Passion Position Number (HPPN) & Gap Resonance**, giving users a deeper understanding of how personal energy manifests.

Check out the full research here: [Hidden Passion Position Number & Gap Resonance Research Paper](https://dakidarts.com/p/research-paper-hidden-passion-position-number-hppn-gap-resonance-by-etuge-anselm-e/)

![HPPN & Gap Resonance Release Paper](https://res.cloudinary.com/ds64xs2lp/image/upload/v1755804804/HPPN-and-Gap-Resonance_bgp1fg.jpg)

### New Endpoints in v0.0.7

#### 1️⃣ `/hidden-passion`

* Calculates your **classic Hidden Passion Number** based on the most frequent letters in your name.
* Returns **number, meaning, and detailed meaning**.
* Supports **GET & POST** requests.

#### 2️⃣ `/maturity-number`

* Computes your **Maturity Number** using your **Life Path Number and Destiny Number**.
* Reveals the **life purpose theme** you evolve into as you mature.
* Returns **number, meaning, and detailed meaning**.
* Supports **GET & POST** requests.

#### 3️⃣ `/hidden-passion-positions` 💡

* Brand new discovery by **Etuge Anselm E.**
* Calculates **Hidden Passion Position Number (HPPN)** and **Gap Resonance** for your dominant letters.
* Shows **letter positions, sum, reduced HPPN, gap vector, and meanings**.
* Adds **a fresh dimension to traditional Hidden Passion numerology**.
* [Read the Research Paper & Download Here](https://dakidarts.com/p/research-paper-hidden-passion-position-number-hppn-gap-resonance-by-etuge-anselm-e/)
* Supports **GET & POST** requests.

#### 4️⃣ `/pinnacle-cycles` 

* Breaks your life into **4 major long-term cycles** (higher-level than Personal Year Numbers).
* Each cycle includes: **start/end years, number, meaning, detailed meaning**.
* Helps discover **life patterns, challenges, and opportunities**.
* Supports **GET & POST** requests.

#### 5️⃣ `/planes-of-expression` 

* Maps letters in your **name** to **4 energy planes**: Physical, Mental, Emotional, Intuitive.
* Returns **counts, meaning, and detailed meaning** for each plane.
* Reveals **dominant energies, balance, and hidden traits**.
* Supports **GET & POST** requests.

### 🔧 Notes & Improvements

* All endpoints now handle **GET & POST requests**.
* Error handling improved across new endpoints — returns **status codes** with error messages.
* All endpoints return **meanings and detailed meanings** wherever applicable.
* Ready for integration with **RapidAPI**.

### 🌟 Use this Release

* Extend numerology insights beyond classic calculations.
* Discover **new layers of personality and destiny** with HPPN & Gap Resonance.
* Analyze **long-term cycles and energy planes** to optimize growth and alignment.

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

## v0.0.3 - Mystical Integration (Feb, 2025)

### New Features:

**Gematria Calculator:** Added a new endpoint /gematria that computes Gematria values using multiple systems, including:

**Ordinal Gematria**,
**Reverse Ordinal Gematria**,
**Pythagorean Gematria**,
**Standard Hebrew Gematria**,
**Hidden Meaning Interpretation:** Returns possible symbolic or mystical meanings for certain numerical values.

Improvements:

API Performance Optimization: Enhanced query handling and response times for all endpoints.
Better Error Handling: More detailed error messages for invalid inputs.

## v0.0.2 - Celestial Expansion (13 Dec, 2023)

### New Features:

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

### Initial Features:

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

## Getting Started

1. **API Integration:** Explore the comprehensive [documentation](https://dakidarts.com/api/the-numerology-api/) to seamlessly integrate Astro-Numerology features into your applications. You can also [view and test the API on RapidAPI](https://rapidapi.com/kidddevs/api/the-numerology-api).
2. **Contribute:** Join the cosmic journey! Contribute to the development, share insights, and enhance the API for the community.
