# Bunny.net GraphQL Schema

## Overview

This is a conceptual GraphQL schema for the Bunny.net platform, representing the data model underlying Bunny.net's CDN, edge storage, video streaming, DNS, security (Shield/WAF), image optimization, edge scripting, and billing services.

Bunny.net exposes its functionality through a set of REST APIs (Core Platform, Pull Zones, Storage, Stream, DNS, Shield, Scripting, etc.). This GraphQL schema unifies those surfaces into a single, coherent type system that reflects the resources and relationships documented at https://docs.bunny.net/reference/bunnynet-api-overview.

**Source:** Conceptual schema derived from Bunny.net REST API documentation and public developer resources.
**Endpoint probed:** `https://api.bunny.net/graphql` — no live GraphQL endpoint found (404). Schema is documentation-derived.
**Reference:** https://docs.bunny.net/reference/bunnynet-api-overview

---

## Schema Source

- Bunny.net Core Platform API: https://docs.bunny.net/reference/bunnynet-api-overview
- Pull Zones: https://docs.bunny.net/reference/pullzonepublic_index
- Storage Zones: https://docs.bunny.net/reference/storagezonepublic_index
- Edge Storage: https://docs.bunny.net/reference/storage-api
- DNS: https://docs.bunny.net/reference/dnszonepublic_index
- Stream: https://docs.bunny.net/reference/video_getvideo
- Shield: https://docs.bunny.net/reference/shield-api
- Statistics: https://docs.bunny.net/reference/statisticspublic_index
- Billing: https://docs.bunny.net/reference/billingpublic_index
- API Keys: https://docs.bunny.net/reference/apikeypublic_index
- Countries: https://docs.bunny.net/reference/countriespublic_index
- Regions: https://docs.bunny.net/reference/regionpublic_index
- GitHub: https://github.com/BunnyWay

---

## Type Summary

| Domain | Types |
|--------|-------|
| CDN / Pull Zones | Zone, PullZone, EdgeRule, CacheFile, CacheClearRequest, PullZoneHostname, OriginConfig, ShieldZone |
| Storage | StorageZone, StorageFile, StorageDirectory, StorageStats, StorageReplicationRegion |
| Video / Stream | VideoLibrary, Video, VideoCollection, VideoTranscoding, Chapter, Moment, Caption, Stream, StreamRecord, DRMConfig |
| DNS | DnsZone, DnsRecord, DnsGeoSteering |
| Security / WAF | WAFConfig, WAFRule, RateLimitPolicy, BotDetectionConfig, CustomRule |
| Edge Compute | EdgeScript, ScriptDeployment, ScriptRoute, ScriptEnvVar |
| Image Optimization | OptimizerConfig, ImageTransform |
| Networking | CDNNode, Region, Country, EdgeServerConfig |
| Identity / Auth | APIKey, Token, Certificate |
| Webhooks | Webhook, WebhookDelivery, WebhookEvent |
| Analytics | BandwidthStat, PullZoneStat, EdgeNodeStats, StorageStatSnapshot, TotalStat |
| Billing | Invoice, Payment, Plan, Billing, BillingUsageEntry |
| Branding / Meta | BunnyBranding, Domain, DomainConfiguration |

Total types defined in schema file: **55**

---

## Key Relationships

- A **PullZone** belongs to an **Account** and has many **EdgeRule**, **PullZoneHostname**, **Certificate**, and **CacheFile** objects.
- A **StorageZone** has many **StorageFile** and **StorageDirectory** objects across one or more **StorageReplicationRegion** regions.
- A **VideoLibrary** contains many **Video** objects; each **Video** has **Caption**, **Chapter**, **Moment**, and **VideoTranscoding** children.
- A **DnsZone** contains **DnsRecord** objects with optional **DnsGeoSteering** configuration.
- **WAFConfig** is attached to a **PullZone** and contains **WAFRule**, **RateLimitPolicy**, and **BotDetectionConfig** entries.
- **EdgeScript** objects are deployed via **ScriptDeployment** and routed through **ScriptRoute** definitions.
- **BandwidthStat**, **PullZoneStat**, and **EdgeNodeStats** aggregate traffic metrics per zone or node.
- **Invoice** and **Payment** are children of **Billing**; each **Plan** defines pricing tiers.
