# Bunny.net (bunny-net)

Bunny.net is a content-delivery and edge platform offering a global CDN, edge storage, video streaming, DNS, image optimisation, edge scripting, and WAF / security shielding. The Bunny.net Core Platform REST API at api.bunny.net manages account-level resources - Pull Zones, Storage Zones, DNS Zones, Stream video libraries, statistics, billing, purge, API keys, and reference data (countries, regions). Product-specific data-plane APIs sit on dedicated hosts: Edge Storage at storage.bunnycdn.com, Stream uploads at video.bunnycdn.com, Shield (WAF), Optimizer, and the Scripting / Magic Containers edge-compute API. All APIs use the AccessKey header for authentication, with API keys issued from the bunny.net dashboard.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bunny-net/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bunny-net/refs/heads/main/apis.yml)

## Tags

- CDN
- Edge
- Video
- Storage
- DNS
- WAF
- Edge Compute
- Image Optimization

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-30

## APIs

### Bunny.net Core Platform API

REST API for managing account-level bunny.net resources - Pull Zones, Storage Zones, DNS Zones, Stream Video Libraries, statistics, billing, purge, API keys, and reference data (countries, regions).

- **Human URL:** [https://docs.bunny.net/reference/bunnynet-api-overview](https://docs.bunny.net/reference/bunnynet-api-overview)
- **Base URL:** `https://api.bunny.net`

#### Tags

- REST
- Account
- Management

#### Properties

- [Documentation](https://docs.bunny.net/reference/bunnynet-api-overview)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Pull Zones API

Endpoints for creating and configuring CDN Pull Zones - origin configuration, edge rules, hostnames, SSL certificates, cache settings, and security headers.

- **Human URL:** [https://docs.bunny.net/reference/pullzonepublic_index](https://docs.bunny.net/reference/pullzonepublic_index)
- **Base URL:** `https://api.bunny.net/pullzone`

#### Tags

- CDN
- Pull Zones
- Edge Rules

#### Properties

- [Documentation](https://docs.bunny.net/reference/pullzonepublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Storage Zones API

Endpoints for creating and managing edge Storage Zones, replication regions, and access keys used by the Edge Storage data-plane.

- **Human URL:** [https://docs.bunny.net/reference/storagezonepublic_index](https://docs.bunny.net/reference/storagezonepublic_index)
- **Base URL:** `https://api.bunny.net/storagezone`

#### Tags

- Storage
- Edge Storage
- Replication

#### Properties

- [Documentation](https://docs.bunny.net/reference/storagezonepublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Edge Storage API

Object-storage data-plane API for uploading, downloading, listing, and deleting files inside a Storage Zone. Regional hosts are derived from the zone's primary region (e.g. ny.storage.bunnycdn.com, la.storage.bunnycdn.com, syd.storage.bunnycdn.com), with the default host at storage.bunnycdn.com.

- **Human URL:** [https://docs.bunny.net/reference/storage-api](https://docs.bunny.net/reference/storage-api)
- **Base URL:** `https://storage.bunnycdn.com`

#### Tags

- Storage
- Object Storage
- Data Plane

#### Properties

- [Documentation](https://docs.bunny.net/reference/storage-api)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net DNS API

Endpoints for managing DNS zones and records on the Bunny.net DNS platform, including geo-steering and load-balancing record types.

- **Human URL:** [https://docs.bunny.net/reference/dnszonepublic_index](https://docs.bunny.net/reference/dnszonepublic_index)
- **Base URL:** `https://api.bunny.net/dnszone`

#### Tags

- DNS
- Geo Steering

#### Properties

- [Documentation](https://docs.bunny.net/reference/dnszonepublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Stream API

Video streaming API for managing Video Libraries, videos, collections, captions, chapters, transcoding profiles, and DRM. Upload and playback are served via dedicated video.bunnycdn.com endpoints; library-level management uses video.bunnycdn.com/library/{libraryId}.

- **Human URL:** [https://docs.bunny.net/reference/video_getvideo](https://docs.bunny.net/reference/video_getvideo)
- **Base URL:** `https://video.bunnycdn.com`

#### Tags

- Video
- Streaming
- VOD
- Transcoding

#### Properties

- [Documentation](https://docs.bunny.net/reference/video_getvideo)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Stream Webhooks

Signed HTTP POST webhooks delivered by Bunny Stream to the WebhookUrl configured on a Video Library whenever a video transitions to a new processing state (Queued, Processing, Encoding, Finished, ResolutionFinished, Failed, PresignedUploadStarted / Finished / Failed, CaptionsGenerated, TitleOrDescriptionGenerated). Each request is authenticated with an HMAC-SHA256 signature over the raw body using the library's Read-Only API key.

- **Human URL:** [https://docs.bunny.net/stream/webhooks](https://docs.bunny.net/stream/webhooks)

#### Tags

- Webhooks
- AsyncAPI
- Video
- Streaming
- Events

#### Properties

- [Documentation](https://docs.bunny.net/stream/webhooks)
- [AsyncAPI](asyncapi/bunny-net-stream-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Shield API

Security and WAF configuration API for Bunny Shield - managed rules, custom rules, bot detection, rate-limiting policies, and DDoS mitigation settings attached to Pull Zones.

- **Human URL:** [https://docs.bunny.net/reference/shield-api](https://docs.bunny.net/reference/shield-api)
- **Base URL:** `https://api.bunny.net/shield`

#### Tags

- WAF
- Security
- DDoS
- Bot Mitigation

#### Properties

- [Documentation](https://docs.bunny.net/reference/shield-api)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Optimizer

Image and front-end optimisation service attached to Pull Zones - image resizing, format conversion (WebP/AVIF), quality controls, and automatic CSS/JS minification. Configured via Pull Zone settings on the Core Platform API.

- **Human URL:** [https://docs.bunny.net/docs/cdn-optimizer-overview](https://docs.bunny.net/docs/cdn-optimizer-overview)
- **Base URL:** `https://api.bunny.net/pullzone`

#### Tags

- Image Optimization
- WebP
- AVIF
- Front-End

#### Properties

- [Documentation](https://docs.bunny.net/docs/cdn-optimizer-overview)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Scripting / Edge Compute API

Edge-compute API for deploying and managing Bunny Edge Scripts - JavaScript/TypeScript functions that run on the Bunny.net edge network to mutate requests and responses, with associated routes, environment variables, and deployments.

- **Human URL:** [https://docs.bunny.net/reference/scripting-api](https://docs.bunny.net/reference/scripting-api)
- **Base URL:** `https://api.bunny.net/compute/script`

#### Tags

- Edge Compute
- Scripting
- JavaScript

#### Properties

- [Documentation](https://docs.bunny.net/reference/scripting-api)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Purge API

Cache purge endpoints for invalidating cached content by URL, by Pull Zone, or by tag across the Bunny.net global edge network.

- **Human URL:** [https://docs.bunny.net/reference/purgepublic_index](https://docs.bunny.net/reference/purgepublic_index)
- **Base URL:** `https://api.bunny.net/purge`

#### Tags

- Cache
- Purge
- Invalidation

#### Properties

- [Documentation](https://docs.bunny.net/reference/purgepublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Statistics API

Endpoints returning bandwidth, request, status-code, and geographic traffic statistics for the account and per Pull Zone or Storage Zone.

- **Human URL:** [https://docs.bunny.net/reference/statisticspublic_index](https://docs.bunny.net/reference/statisticspublic_index)
- **Base URL:** `https://api.bunny.net/statistics`

#### Tags

- Statistics
- Analytics
- Bandwidth

#### Properties

- [Documentation](https://docs.bunny.net/reference/statisticspublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Billing API

Billing endpoints for retrieving account balance, monthly usage and invoices, and applying promo codes.

- **Human URL:** [https://docs.bunny.net/reference/billingpublic_index](https://docs.bunny.net/reference/billingpublic_index)
- **Base URL:** `https://api.bunny.net/billing`

#### Tags

- Billing
- Usage
- Invoices

#### Properties

- [Documentation](https://docs.bunny.net/reference/billingpublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net API Keys API

Endpoints for managing API keys (AccessKey) issued for the account.

- **Human URL:** [https://docs.bunny.net/reference/apikeypublic_index](https://docs.bunny.net/reference/apikeypublic_index)
- **Base URL:** `https://api.bunny.net/apikey`

#### Tags

- API Keys
- Authentication

#### Properties

- [Documentation](https://docs.bunny.net/reference/apikeypublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Countries API

Reference endpoint returning the list of countries Bunny.net supports for geo-targeting in Pull Zone and DNS rules.

- **Human URL:** [https://docs.bunny.net/reference/countriespublic_index](https://docs.bunny.net/reference/countriespublic_index)
- **Base URL:** `https://api.bunny.net/country`

#### Tags

- Reference
- Geography

#### Properties

- [Documentation](https://docs.bunny.net/reference/countriespublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bunny.net Regions API

Reference endpoint returning the list of Bunny.net edge and storage regions for use in zone configuration.

- **Human URL:** [https://docs.bunny.net/reference/regionpublic_index](https://docs.bunny.net/reference/regionpublic_index)
- **Base URL:** `https://api.bunny.net/region`

#### Tags

- Reference
- Regions

#### Properties

- [Documentation](https://docs.bunny.net/reference/regionpublic_index)
- [Postman Collection](collections/bunny-net.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bunny-net.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/bunny-net)
- [Website](https://bunny.net/)
- [Documentation](https://docs.bunny.net/)
- [Git Hub](https://github.com/BunnyWay)
- [Status](https://status.bunny.net/)
- [Pricing](https://bunny.net/pricing/)
- [Plans](plans/bunny-net-plans-pricing.yml)
- [Rate Limits](rate-limits/bunny-net-rate-limits.yml)
- [Fin Ops](finops/bunny-net-finops.yml)
- [L L Ms Txt](https://docs.bunny.net/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
