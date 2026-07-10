# Zinrelo (zinrelo)

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
