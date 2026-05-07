---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: backstage-catalog-openapi.yml
  format: yaml
  label: Backstage Catalog API
  slug: catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-catalog-openapi.yml
- filename: backstage-scaffolder-openapi.yml
  format: yaml
  label: Backstage Scaffolder API
  slug: scaffolder-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-scaffolder-openapi.yml
- filename: backstage-auth-openapi.yml
  format: yaml
  label: Backstage Auth API
  slug: auth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-auth-openapi.yml
- filename: backstage-techdocs-openapi.yml
  format: yaml
  label: Backstage TechDocs API
  slug: techdocs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-techdocs-openapi.yml
- filename: backstage-search-openapi.yml
  format: yaml
  label: Backstage Search API
  slug: search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-search-openapi.yml
- filename: backstage-permissions-openapi.yml
  format: yaml
  label: Backstage Permissions API
  slug: permissions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-permissions-openapi.yml
- filename: backstage-events-asyncapi.yml
  format: yaml
  label: Backstage Events System
  slug: events-system
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/asyncapi/backstage-events-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Backstage: open-source framework with no license cost; total cost of ownership is dominated by the underlying compute, database, storage, observability, and engineering time to operate the portal. Commercial distributions (Spotify Portal, Roadie, RHDH) introduce per-developer subscription cost on top.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: varies (self-hosted; Spotify, Roadie, Red Hat for commercial)
  PricingCategory: Open Source / Subscription
  ProviderName: CNCF / Backstage
  PublisherName: CNCF / Backstage Community
  ServiceCategory: Developer Tools
  ServiceName: Backstage
layout: finops
meters:
- aggregation: sum
  description: Cluster compute time hosting Backstage frontend / backend / scaffolder workers
  dimensions:
  - environment
  - region
  name: hosting_compute
  unit: instance-hour
- aggregation: avg
  description: PostgreSQL / managed DB capacity backing the Backstage catalog
  name: database_storage
  unit: GB-month
- aggregation: avg
  description: TechDocs static-site storage (typically S3 / Blob)
  name: techdocs_storage
  unit: GB-month
- aggregation: sum
  description: Calls into upstream developer tools (GitHub, GitLab, Jenkins, Jira, Kubernetes) made by Backstage on behalf of users
  dimensions:
  - integration
  name: integration_api_calls
  unit: request
- aggregation: max
  description: Per-developer subscription for commercial Backstage distributions (Spotify Portal, Roadie, RHDH)
  dimensions:
  - distribution
  name: developer_seats
  unit: developer
name: Backstage Finops
provider_name: Backstage
provider_slug: backstage
publisher_name: CNCF / Backstage Community
service_category: Developer Tools
slug: backstage-finops
source_filename: backstage-finops.yml
source_heading: FinOps Profile
source_url: https://backstage.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Backstage\nproviderId: backstage\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Developer Portal\n  - Open Source\n  - Internal Developer Platform\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Backstage: open-source framework with no license cost; total cost\n  of ownership is dominated by the underlying compute, database, storage, observability, and engineering\n  time to operate the portal. Commercial distributions (Spotify Portal, Roadie, RHDH) introduce per-developer\n  subscription cost on top.'\nnotes: Backstage open-source itself has no license fee; the FinOps shape captures operating cost (infrastructure\n  + engineering) plus optional commercial-distribution subscription. Reconciled=false reflects the absence\n  of a single canonical pricing surface.\nsources:\n  - https://backstage.io/\n  - https://backstage.io/docs/overview/architecture-overview\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CNCF / Backstage Community\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Backstage\n  ServiceCategory: Developer Tools\n  ProviderName: CNCF / Backstage\n  PublisherName: CNCF / Backstage Community\n  InvoiceIssuerName: varies (self-hosted; Spotify, Roadie, Red Hat for commercial)\n  PricingCategory: Open Source / Subscription\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: hosting_compute\n    description: Cluster compute time hosting Backstage frontend / backend / scaffolder workers\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n \
  \     - environment\n      - region\n  - name: database_storage\n    description: PostgreSQL / managed DB capacity backing the Backstage catalog\n    unit: GB-month\n    aggregation: avg\n  - name: techdocs_storage\n    description: TechDocs static-site storage (typically S3 / Blob)\n    unit: GB-month\n    aggregation: avg\n  - name: integration_api_calls\n    description: Calls into upstream developer tools (GitHub, GitLab, Jenkins, Jira, Kubernetes) made\n      by Backstage on behalf of users\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n  - name: developer_seats\n    description: Per-developer subscription for commercial Backstage distributions (Spotify Portal, Roadie,\n      RHDH)\n    unit: developer\n    aggregation: max\n    dimensions:\n      - distribution\nprinciples:\n  - name: Visibility\n    description: Tag the cluster / namespace running Backstage in your cloud cost tool (Cost Management,\n      OpenCost) to surface compute, DB, and storage\
  \ spend; track plugin activity via Backstage Insights\n      or equivalent.\n  - name: Allocation\n    description: Treat Backstage as a shared platform service; chargeback to consuming teams via developer-seat\n      counts or use developer-experience platform team budget.\n  - name: Optimization\n    description: Right-size frontend / backend pods; cache catalog data aggressively to reduce upstream\n      API calls; tune Scaffolder concurrency; archive unused plugins; evaluate commercial-distribution\n      ROI vs in-house engineering cost.\n  - name: Accountability\n    description: Assign a Backstage platform owner; review monthly per-team plugin usage and developer\n      activity; renegotiate commercial-distribution subscriptions at renewal based on active developer\n      counts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/finops/backstage-finops.yml
sources:
- https://backstage.io/
- https://backstage.io/docs/overview/architecture-overview
specification: FinOps Framework
tags:
- Developer Portal
- Open Source
- Internal Developer Platform
- FinOps
- FOCUS
---
