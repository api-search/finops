---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: discgolfapi-openapi.yml
  format: yaml
  label: DiscGolfAPI REST API
  slug: discgolfapi-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/discgolfapi/refs/heads/main/openapi/discgolfapi-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: NotApplicable
  chargeCategories:
  - Usage
  chargeFrequency: NotApplicable
  pricingCategory: Free
description: FinOps framework definition for the DiscGolfAPI public API. The provider's service is free and read-only, so this artefact primarily models the cost-visibility and unit-economics surface for consumers integrating DiscGolfAPI, aligned with the FinOps Foundation framework and FOCUS data spec.
focus_columns:
  BilledCost: '0.00'
  BillingCurrency: USD
  ChargeCategory: Usage
  EffectiveCost: '0.00'
  InvoiceIssuerName: DiscGolfAPI
  ListCost: '0.00'
  ListUnitPrice: '0.00'
  PricingCategory: Free
  PricingUnit: request
  ProviderName: DiscGolfAPI
  PublisherName: DiscGolfAPI
  ServiceCategory: Open Data API
  ServiceName: DiscGolfAPI
layout: finops
meters:
- aggregation: sum
  description: Count of API requests issued to DiscGolfAPI endpoints.
  dimensions:
  - endpoint
  - status_code
  - country_filter
  - region_filter
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned by DiscGolfAPI responses.
  dimensions:
  - endpoint
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Count of bulk artefact downloads from the dataset manifest base URL.
  dimensions:
  - artefact
  - publish_version
  - consumer
  name: manifest_artefact_downloads
  unit: download
name: Discgolfapi Finops
provider_name: DiscGolfAPI
provider_slug: discgolfapi
publisher_name: DiscGolfAPI
service_category: Open Data API
slug: discgolfapi-finops
source_filename: discgolfapi-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: DiscGolfAPI\nproviderId: discgolfapi\npublisherName: DiscGolfAPI\nserviceCategory: Open Data API\ncreated: '2026-05-16'\nmodified: '2026-05-16'\nreconciled: false\nnotes: >-\n  DiscGolfAPI is a free, read-only public service with no published billing\n  surface, invoicing, or chargeable units. The FinOps framework definition\n  below describes the cost-allocation surface for consumers (engineering\n  teams that integrate DiscGolfAPI) rather than a provider billing model.\n  No FOCUS-billed columns apply on the provider side; the chargeCategory\n  is \"Usage\" with a zero-rated PricingCategory (\"Free\"). Reconcile if and\n  when DiscGolfAPI introduces a paid tier.\ntags:\n  - Disc Golf\n\
  \  - Sports\n  - Courses\n  - Open Data\n  - Recreation\n  - FinOps\n  - FOCUS\n  - Free\ndescription: >-\n  FinOps framework definition for the DiscGolfAPI public API. The\n  provider's service is free and read-only, so this artefact primarily\n  models the cost-visibility and unit-economics surface for consumers\n  integrating DiscGolfAPI, aligned with the FinOps Foundation framework\n  and FOCUS data spec.\nprinciples:\n  - name: Visibility\n    description: >-\n      Make DiscGolfAPI consumption volume visible to engineering, product,\n      and operations teams so fair-use posture and reliance are understood\n      even when no fee is charged.\n  - name: Allocation\n    description: >-\n      Tag DiscGolfAPI calls with consumer team, environment, application,\n      and feature so the cost of replacement (should DiscGolfAPI become\n      unavailable) can be allocated and forecast.\n  - name: Optimization\n    description: >-\n      Continuously evaluate request patterns, caching,\
  \ and bulk-artefact\n      downloads from the dataset manifest to reduce request volume and\n      respect fair use.\n  - name: Accountability\n    description: >-\n      Establish owners on the consuming side for monitoring DiscGolfAPI\n      availability and for upholding the licence attribution requirement\n      across all surfaces where data is displayed.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n\
  \  pricingCategory: Free\n  billingFrequency: NotApplicable\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  chargeFrequency: NotApplicable\nfocusColumns:\n  ServiceName: DiscGolfAPI\n  ServiceCategory: Open Data API\n  ProviderName: DiscGolfAPI\n  PublisherName: DiscGolfAPI\n  InvoiceIssuerName: DiscGolfAPI\n  PricingCategory: Free\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  BilledCost: '0.00'\n  EffectiveCost: '0.00'\n  ListCost: '0.00'\n  ListUnitPrice: '0.00'\nmeters:\n  - name: api_requests\n    description: Count of API requests issued to DiscGolfAPI endpoints.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - status_code\n      - country_filter\n      - region_filter\n      - consumer\n  - name: data_egress\n    description: Bytes returned by DiscGolfAPI responses.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - consumer\n  - name: manifest_artefact_downloads\n    description:\
  \ Count of bulk artefact downloads from the dataset manifest base URL.\n    unit: download\n    aggregation: sum\n    dimensions:\n      - artefact\n      - publish_version\n      - consumer\napis:\n  - name: DiscGolfAPI REST API\n    baseURL: https://io.discgolfapi.com/v1\n    tags:\n      - Courses\n      - Countries\n      - Regions\n      - Updates\n      - Metadata\n    serviceName: DiscGolfAPI REST API\n    serviceCategory: Open Data API\nunitEconomics:\n  - name: Requests per Active Consumer\n    metric: api_requests / active_consumers\n    target: TBD\n  - name: Cache Hit Ratio\n    metric: cache_hits / (cache_hits + api_requests)\n    target: \">= 0.7\"\n  - name: Egress per 1K Requests\n    metric: data_egress_gb / (api_requests / 1000)\n    target: TBD\nmaintainers:\n  - FN: DiscGolfAPI\n    url: https://discgolfapi.com/contact/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/discgolfapi/refs/heads/main/finops/discgolfapi-finops.yml
sources: []
specification: FinOps Framework
tags:
- Disc Golf
- Sports
- Courses
- Open Data
- Recreation
- FinOps
- FOCUS
- Free
---
