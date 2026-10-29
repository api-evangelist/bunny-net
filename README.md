# Bunny.net

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Bunny.net is a content-delivery and edge platform offering a global CDN, edge storage, video streaming, DNS, image optimisation, edge scripting, and WAF / security shielding. The Bunny.net Core Platform REST API at api.bunny.net manages account-level resources - Pull Zones, Storage Zones, DNS Zones, Stream video libraries, statistics, billing, purge, API keys, and reference data (countries, regions). Product-specific data-plane APIs sit on dedicated hosts: Edge Storage at storage.bunnycdn.com, Stream uploads at video.bunnycdn.com, Shield (WAF), Optimizer, and the Scripting / Magic Containers edge-compute API. All APIs use the AccessKey header for authentication, with API keys issued from the bunny.net dashboard.

**Areas:** CDN · Edge · Video · Storage · DNS · WAF · Edge Compute · Image Optimization

## Bunny.net on APIs.io

Everything profiled for Bunny.net is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/bunny-net/](https://apis.io/providers/bunny-net/)** — or go straight to one of the APIs or properties below.

### APIs (26)

- [Bunny.net Core Platform API](https://apis.io/apis/bunny-net/core/) — REST API for managing account-level bunny.net resources - Pull Zones, Storage Zones, DNS Zones, Stream Video Libraries, statistics, billing, purge, API…
- [Bunny.net Pull Zones API](https://apis.io/apis/bunny-net/pull-zones/) — Endpoints for creating and configuring CDN Pull Zones - origin configuration, edge rules, hostnames, SSL certificates, cache settings, and security headers.
- [Bunny.net Storage Zones API](https://apis.io/apis/bunny-net/storage-zones/) — Endpoints for creating and managing edge Storage Zones, replication regions, and access keys used by the Edge Storage data-plane.
- [Bunny.net Edge Storage API](https://apis.io/apis/bunny-net/edge-storage/) — Object-storage data-plane API for uploading, downloading, listing, and deleting files inside a Storage Zone. Regional hosts are derived from the zone's…
- [Bunny.net DNS API](https://apis.io/apis/bunny-net/dns/) — Endpoints for managing DNS zones and records on the Bunny.net DNS platform, including geo-steering and load-balancing record types.
- [Bunny.net Stream API](https://apis.io/apis/bunny-net/stream/) — Video streaming API for managing Video Libraries, videos, collections, captions, chapters, transcoding profiles, and DRM. Upload and playback are served via…
- [Bunny.net Stream Webhooks](https://apis.io/apis/bunny-net/stream-webhooks/) — Signed HTTP POST webhooks delivered by Bunny Stream to the WebhookUrl configured on a Video Library whenever a video transitions to a new processing state…
- [Bunny.net Shield API](https://apis.io/apis/bunny-net/shield/) — Security and WAF configuration API for Bunny Shield - managed rules, custom rules, bot detection, rate-limiting policies, and DDoS mitigation settings…
- [Bunny.net Optimizer](https://apis.io/apis/bunny-net/optimizer/) — Image and front-end optimisation service attached to Pull Zones - image resizing, format conversion (WebP/AVIF), quality controls, and automatic CSS/JS…
- [Bunny.net Scripting / Edge Compute API](https://apis.io/apis/bunny-net/scripting/) — Edge-compute API for deploying and managing Bunny Edge Scripts - JavaScript/TypeScript functions that run on the Bunny.net edge network to mutate requests…
- [Bunny.net Purge API](https://apis.io/apis/bunny-net/purge/) — Cache purge endpoints for invalidating cached content by URL, by Pull Zone, or by tag across the Bunny.net global edge network.
- [Bunny.net Statistics API](https://apis.io/apis/bunny-net/statistics/) — Endpoints returning bandwidth, request, status-code, and geographic traffic statistics for the account and per Pull Zone or Storage Zone.
- [Bunny.net Billing API](https://apis.io/apis/bunny-net/billing/) — Billing endpoints for retrieving account balance, monthly usage and invoices, and applying promo codes.
- [Bunny.net API Keys API](https://apis.io/apis/bunny-net/api-keys/) — Endpoints for managing API keys (AccessKey) issued for the account.
- [Bunny.net Countries API](https://apis.io/apis/bunny-net/countries/) — Reference endpoint returning the list of countries Bunny.net supports for geo-targeting in Pull Zone and DNS rules.
- [Bunny.net Regions API](https://apis.io/apis/bunny-net/regions/) — Reference endpoint returning the list of Bunny.net edge and storage regions for use in zone configuration.
- [Bunny.net Billing API](https://apis.io/apis/bunny-net/bunny-net-billing-api/) — The Billing API from Bunny.net — 3 operation(s) for billing.
- [Bunny.net Countries API](https://apis.io/apis/bunny-net/bunny-net-countries-api/) — The Countries API from Bunny.net — 1 operation(s) for countries.
- [Bunny.net PullZones API](https://apis.io/apis/bunny-net/bunny-net-pullzones-api/) — The PullZones API from Bunny.net — 12 operation(s) for pullzones.
- [Bunny.net Purge API](https://apis.io/apis/bunny-net/bunny-net-purge-api/) — The Purge API from Bunny.net — 1 operation(s) for purge.
- [Bunny.net Regions API](https://apis.io/apis/bunny-net/bunny-net-regions-api/) — The Regions API from Bunny.net — 1 operation(s) for regions.
- [Bunny.net Statistics API](https://apis.io/apis/bunny-net/bunny-net-statistics-api/) — The Statistics API from Bunny.net — 3 operation(s) for statistics.
- [Bunny.net StorageZones API](https://apis.io/apis/bunny-net/bunny-net-storagezones-api/) — The StorageZones API from Bunny.net — 4 operation(s) for storagezones.
- [Bunny.net Stream API](https://apis.io/apis/bunny-net/bunny-net-stream-api/) — The Stream API from Bunny.net — 2 operation(s) for stream.
- [Bunny.net API Keys API](https://apis.io/apis/bunny-net/bunny-net-api-keys-api/) — The API Keys API from Bunny.net — 1 operation(s) for api keys.
- [Bunny.net DNS Zones API](https://apis.io/apis/bunny-net/bunny-net-dns-zones-api/) — The DNS Zones API from Bunny.net — 6 operation(s) for dns zones.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Bunny.net Stream Webhooks](https://apis.io/asyncapis/bunny-net/bunny-net-stream-webhooks-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [stream/video/state-changed](https://apis.io/channels/bunny-net/stream-video-state-changed/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/bunny-net/](https://apis.io/graphqls/bunny-net/bunny-net-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Bunny Net Agentic Access](https://apis.io/agentic-access/bunny-net/bunny-net-agentic-access/)

#### Collections (11)

Postman and Open Collection request collections.

- [Bunny.net Core Platform API](https://apis.io/collections/bunny-net/open-bunny-net/)
- [Bunny.net Core Platform APIKeys API](https://apis.io/collections/bunny-net/open-bunny-net-apikeys-api/)
- [Bunny.net Core Platform APIKeys Billing API](https://apis.io/collections/bunny-net/open-bunny-net-billing-api/)
- [Bunny.net Core Platform APIKeys Countries API](https://apis.io/collections/bunny-net/open-bunny-net-countries-api/)
- [Bunny.net Core Platform APIKeys DNSZones API](https://apis.io/collections/bunny-net/open-bunny-net-dnszones-api/)
- [Bunny.net Core Platform APIKeys PullZones API](https://apis.io/collections/bunny-net/open-bunny-net-pullzones-api/)
- [Bunny.net Core Platform APIKeys Purge API](https://apis.io/collections/bunny-net/open-bunny-net-purge-api/)
- [Bunny.net Core Platform APIKeys Regions API](https://apis.io/collections/bunny-net/open-bunny-net-regions-api/)
- [Bunny.net Core Platform APIKeys Statistics API](https://apis.io/collections/bunny-net/open-bunny-net-statistics-api/)
- [Bunny.net Core Platform APIKeys StorageZones API](https://apis.io/collections/bunny-net/open-bunny-net-storagezones-api/)
- [Bunny.net Core Platform APIKeys Stream API](https://apis.io/collections/bunny-net/open-bunny-net-stream-api/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Bunny.net — asyncapi rules](https://apis.io/rules/bunny-net/bunny-net-asyncapi-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Bunny Net Authentication](https://apis.io/security/bunny-net/bunny-net-authentication/)
- [Bunny Net Domain Security](https://apis.io/security/bunny-net/bunny-net-domain-security/)

#### Plans and pricing (2)

Published plans, tiers and prices.

- [Bunny Net Plans Pricing](https://apis.io/plans/bunny-net/bunny-net-plans-pricing/)
- [Bunny Net Price Estimates](https://apis.io/plans/bunny-net/bunny-net-price-estimates/)

#### Rate limits (1)

Published request limits.

- [Bunny Net Rate Limits](https://apis.io/rate-limits/bunny-net/bunny-net-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Bunny Net Finops](https://apis.io/finops/bunny-net/bunny-net-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://bunny.net/)
- [Documentation](https://docs.bunny.net/)
- [Pricing](https://bunny.net/pricing/)
- [Blog](https://bunny.net/blog/)

## API Evangelist rating

**Kin Score 35.6** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 56.9 |
| Contract governance | 13.6 |
| Operational transparency | 10.5 |
| Developer ergonomics | 23.8 |
| Access clarity | 42.1 |

**Agent readiness 19.0** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 11.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/bunny-net/](https://apis.io/providers/bunny-net/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Bunny.net: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/bunny-net/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
