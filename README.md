# Bunny.net (bunny-net)

Bunny.net is a Slovenian content-delivery and edge platform offering a global CDN, edge storage, video streaming, DNS, image optimisation, edge scripting / Magic Containers, and WAF (Bunny Shield). The Bunny.net Core Platform REST API at `api.bunny.net` manages account-level resources — Pull Zones, Storage Zones, DNS Zones, Stream video libraries, statistics, billing, purge, API keys, and reference data (countries, regions). Product-specific data-plane APIs sit on dedicated hosts: Edge Storage at `storage.bunnycdn.com`, Stream uploads at `video.bunnycdn.com`, Shield (WAF), Optimizer, and the Scripting / Magic Containers edge-compute API. All APIs use the `AccessKey` header for authentication, with API keys issued from the bunny.net dashboard.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/bunny-net/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=bunny-net-api-evangelist&utm_content=repo)

## Type
- **x-type:** company

## Tags
- CDN, Edge, Video, Storage, DNS, WAF, Edge Compute, Image Optimization

## APIs
- **Bunny.net Core Platform API** — REST API at `api.bunny.net` for managing account-level resources: Pull Zones, Storage Zones, DNS Zones, Stream Video Libraries, statistics, billing, purge, API keys, and reference data. [OpenAPI](openapi/bunny-net-openapi.yml) · [Docs](https://docs.bunny.net/reference/bunnynet-api-overview)
- **Bunny.net Pull Zones API** — Create and configure CDN Pull Zones — origin configuration, edge rules, hostnames, SSL certificates, cache settings, and security headers. [Docs](https://docs.bunny.net/reference/pullzonepublic_index)
- **Bunny.net Storage Zones API** — Create and manage edge Storage Zones, replication regions, and access keys used by the Edge Storage data-plane. [Docs](https://docs.bunny.net/reference/storagezonepublic_index)
- **Bunny.net Edge Storage API** — Object-storage data-plane at `storage.bunnycdn.com` (and regional hosts like `ny.storage.bunnycdn.com`, `la.storage.bunnycdn.com`, `syd.storage.bunnycdn.com`) for upload, download, list, and delete operations against a Storage Zone. [Docs](https://docs.bunny.net/reference/storage-api)
- **Bunny.net DNS API** — Manage DNS zones and records on the Bunny.net DNS platform, including geo-steering and load-balancing record types. [Docs](https://docs.bunny.net/reference/dnszonepublic_index)
- **Bunny.net Stream API** — Video streaming API at `video.bunnycdn.com` for managing Video Libraries, videos, collections, captions, chapters, transcoding profiles, and DRM. [Docs](https://docs.bunny.net/reference/video_getvideo)
- **Bunny.net Shield API** — Security and WAF configuration for Bunny Shield — managed rules, custom rules, bot detection, rate-limiting policies, and DDoS mitigation attached to Pull Zones. [Docs](https://docs.bunny.net/reference/shield-api)
- **Bunny.net Optimizer** — Image and front-end optimisation attached to Pull Zones — image resizing, WebP/AVIF conversion, quality controls, and automatic CSS/JS minification. [Docs](https://docs.bunny.net/docs/cdn-optimizer-overview)
- **Bunny.net Scripting / Edge Compute API** — Deploy and manage Bunny Edge Scripts — JavaScript/TypeScript functions running on the Bunny.net edge network, with routes, environment variables, and deployments. [Docs](https://docs.bunny.net/reference/scripting-api)
- **Bunny.net Purge API** — Cache invalidation by URL, by Pull Zone, or by tag across the global edge. [Docs](https://docs.bunny.net/reference/purgepublic_index)
- **Bunny.net Statistics API** — Bandwidth, request, status-code, and geographic traffic statistics for the account and per Pull Zone / Storage Zone. [Docs](https://docs.bunny.net/reference/statisticspublic_index)
- **Bunny.net Billing API** — Account balance, monthly usage, invoices, and promo code application. [Docs](https://docs.bunny.net/reference/billingpublic_index)
- **Bunny.net API Keys API** — Manage `AccessKey` API keys issued for the account. [Docs](https://docs.bunny.net/reference/apikeypublic_index)
- **Bunny.net Countries API** — Reference list of countries supported for geo-targeting in Pull Zone and DNS rules. [Docs](https://docs.bunny.net/reference/countriespublic_index)
- **Bunny.net Regions API** — Reference list of Bunny.net edge and storage regions for use in zone configuration. [Docs](https://docs.bunny.net/reference/regionpublic_index)

## Artifacts
- [OpenAPI — Bunny.net Core Platform API](openapi/bunny-net-openapi.yml)

## Plans, Rate Limits, FinOps
- [Plans](plans/bunny-net-plans-pricing.yml) — Pay-as-you-go bandwidth pricing across regional zones (HVF Europe/North America, Asia/Oceania, South America, Africa), Storage Zone pricing per GB/month, Stream per-minute encoded and per-GB delivered, with monthly minimums for production accounts.
- [Rate Limits](rate-limits/bunny-net-rate-limits.yml) — Bunny.net API enforces per-account request rate ceilings on `api.bunny.net`; data-plane endpoints (Edge Storage, Stream upload) are governed by per-region throughput rather than per-key quotas. Excess management-plane requests return `429 Too Many Requests`.
- [FinOps](finops/bunny-net-finops.yml) — Cost surface spans CDN bandwidth (by region), Edge Storage (capacity + replication), Stream (encoding + delivery), and Shield/Optimizer add-ons; tag spend by Pull Zone / Storage Zone / Video Library for chargeback.

## GitHub
The Bunny.net engineering org publishes SDKs, integrations, and tooling at [github.com/BunnyWay](https://github.com/BunnyWay) — including the official PHP, .NET, and Node.js SDKs, the Magic Containers CLI, a Terraform provider, and storage / streaming sample apps.

## Anthropic
Bunny.net does not federate to Anthropic's Claude models directly, but the Bunny Edge Scripting / Magic Containers runtime is a natural execution surface for AI-assisted edge workloads — including calls out to the Anthropic Messages API from JavaScript/TypeScript edge functions running on the Bunny.net network. Bunny Shield and Optimizer also pair well with Anthropic-powered origin services where AI inference happens behind the CDN.

## Timestamps
- **Created:** 2026-05-23
- **Modified:** 2026-05-25

## Notes
- Authentication uses the `AccessKey` request header carrying the account API key issued from the bunny.net dashboard. Some scoped operations (e.g. Storage Zone uploads) use a separate per-zone access key.
- Bunny.net publishes an `llms.txt` at `https://docs.bunny.net/llms.txt` — registered in `apis.yml` under `common.LLMsTxt`.
- The Bunny.net documentation site (docs.bunny.net) is powered by ReadMe; the per-endpoint reference pages are the canonical machine-readable surface — there is no single official OpenAPI download as of profiling.
- Geographic edge footprint covers 100+ PoPs; regional pricing tiers reflect transit cost differences (HVF Europe/NA being the cheapest, Africa/South America the highest).

## Maintainers
**FN:** Kin Lane
**Email:** kin@apievangelist.com
