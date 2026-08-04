# Zinrelo (zinrelo)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Zinrelo is an enterprise SaaS loyalty and rewards platform that helps brands run holistic loyalty programs spanning transactional, social, advocacy, engagement, behavioral, and emotional loyalty across web, mobile, and in-store channels. Its documented REST Loyalty API lets you enroll and manage members, award and deduct points, record purchases and returns, list rewards, and redeem points for rewards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/zinrelo/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/zinrelo/refs/heads/main/apis.yml)

## Access Model

Zinrelo's API **reference documentation is public** and self-serve to read (both the classic v1 API reference at `zinrelo.github.io/slate` and the v2 loyalty / loyalty-storefront reference in the Zinrelo help center). However, **API access itself is account-gated**: every request is authenticated with a `partner-id` and an `api-key` that are provisioned to your Zinrelo account, and Zinrelo does not offer open, public, credit-card-free API keys. Pricing is quote-based through sales (a free trial and a Shopify app tier free up to 500 loyalty members also exist). In practice you must be a Zinrelo customer to obtain working credentials.

**Rebrand note:** Zinrelo is rebranding to **TrueLoyal**. Some documentation now redirects to `help.trueloyal.com` and `www.trueloyal.com`, though the API host remains `api.zinrelo.com` and the `zinrelo.com` help URLs still resolve. The `zinrelo` folder slug and Zinrelo naming are retained here.

**Modeling note:** The endpoint paths, headers, and query parameters in this catalog are drawn from Zinrelo's public documentation and are accurate. Request and response body schemas in the OpenAPI are **honestly modeled** from the public docs and examples, since Zinrelo does not publish a machine-readable OpenAPI with full field-level schemas. Verify exact field names against the live reference before production use.

## Tags

- Loyalty
- Rewards
- Points
- Customer Retention
- Ecommerce
- SaaS

## Timestamps

- **Created:** 2026-07-10
- **Modified:** 2026-07-10

## APIs

### Zinrelo Members API

Enroll, retrieve, list, update, block, and unsubscribe loyalty program members, and read a member's point balances, transactions, redemptions, eligible activities, and next-tier status. Members are identified by email.

- **Human URL:** [https://help.zinrelo.com/reference/introduction](https://help.zinrelo.com/reference/introduction)
- **Base URL:** `https://api.zinrelo.com`

### Zinrelo Points API

Award points to a member for a completed activity (points determined by the activity configuration in the Zinrelo admin console) and deduct points from a member's account. Powers the earning side of a loyalty program.

- **Human URL:** [https://help.zinrelo.com/reference/perform-activity-api](https://help.zinrelo.com/reference/perform-activity-api)
- **Base URL:** `https://api.zinrelo.com`

### Zinrelo Transactions API

Record purchases (awarding points and storing order and product data) and returns (deducting previously awarded points), and list program-wide or member-scoped transactions with pagination and date and status filters. The v2 loyalty-storefront transactions endpoint returns the authenticated member's transactions.

- **Human URL:** [https://help.zinrelo.com/reference/list-members-transaction-api](https://help.zinrelo.com/reference/list-members-transaction-api)
- **Base URL:** `https://api.zinrelo.com`

### Zinrelo Rewards API

List all rewards a program offers, sorted by last modified date by default and filterable and sortable by rank and points to be redeemed. This is the catalog side of the loyalty program that members redeem points against.

- **Human URL:** [https://help.zinrelo.com/reference/list-all-rewards](https://help.zinrelo.com/reference/list-all-rewards)
- **Base URL:** `https://api.zinrelo.com`

### Zinrelo Redemptions API

Redeem a member's points for a reward and list the redemption options configured for the program or available to a specific member. Powers the spending side of a loyalty program.

- **Human URL:** [https://help.zinrelo.com/reference/introduction](https://help.zinrelo.com/reference/introduction)
- **Base URL:** `https://api.zinrelo.com`

## Authentication

All API requests must include two HTTP headers:

- `partner-id` — your Zinrelo Partner ID
- `api-key` — your Zinrelo API key

Both are provisioned to your Zinrelo account.

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/zinrelo)
- [Website](https://www.zinrelo.com)
- [Documentation](https://help.zinrelo.com/reference/introduction)
- [API Reference](https://zinrelo.github.io/slate/)
- [Plans](plans/zinrelo-plans-pricing.yml)
- [Rate Limits](rate-limits/zinrelo-rate-limits.yml)
- [Fin Ops](finops/zinrelo-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
