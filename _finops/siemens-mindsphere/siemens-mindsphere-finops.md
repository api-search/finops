---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: siemens-mindsphere-asset-management-openapi.yml
  format: yaml
  label: Siemens MindSphere Asset Management API
  slug: asset-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/siemens-mindsphere/refs/heads/main/openapi/siemens-mindsphere-asset-management-openapi.yml
- filename: siemens-mindsphere-iot-timeseries-openapi.yml
  format: yaml
  label: Siemens MindSphere IoT Time Series API
  slug: iot-timeseries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/siemens-mindsphere/refs/heads/main/openapi/siemens-mindsphere-iot-timeseries-openapi.yml
billing_model:
  billingCurrency: EUR/USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Enterprise IIoT Subscription
description: FOCUS-aligned FinOps placeholder for Siemens MindSphere/Insights Hub. Pricing is contracted rather than self-service; cost is driven by tenant size, asset/agent counts, ingested data volume, and named users rather than per-API-call charges.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Siemens AG
  ProviderName: Siemens
  PublisherName: Siemens AG
  ServiceCategory: Industrial IoT
  ServiceName: Siemens MindSphere
layout: finops
meters:
- aggregation: sum
  description: Tenant subscription fee covering platform access, included assets, and base data ingest.
  dimensions:
  - tenant
  - region
  name: tenant_subscription
  unit: month
- aggregation: max
  description: Number of connected industrial assets/agents against the contracted ceiling; primary MindSphere/Insights Hub sizing dimension.
  dimensions:
  - tenant
  - asset_type
  name: asset_or_agent_count
  unit: asset
- aggregation: sum
  description: Time-series and event data volume ingested into the tenant; usually capped per contract.
  dimensions:
  - tenant
  - source
  name: data_ingest
  unit: GB
name: Siemens Mindsphere Finops
provider_name: Siemens MindSphere
provider_slug: siemens-mindsphere
publisher_name: Siemens AG
service_category: Industrial IoT
slug: siemens-mindsphere-finops
source_filename: siemens-mindsphere-finops.yml
source_heading: FinOps Profile
source_url: https://siemens.mindsphere.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Siemens MindSphere\nproviderId: siemens-mindsphere\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Industrial IoT\n  - IIoT\n  - Insights Hub\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Siemens MindSphere/Insights Hub. Pricing is contracted\n  rather than self-service; cost is driven by tenant size, asset/agent counts, ingested data volume,\n  and named users rather than per-API-call charges.\nsources:\n  - https://siemens.mindsphere.io/\nnotes: No public billing model documented. FinOps treatment is contract-driven; reconciliation pending\n  tenant-specific invoice and capacity terms.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Siemens AG\nserviceCategory: Industrial IoT\nbillingModel:\n  pricingCategory: Enterprise IIoT Subscription\n  billingFrequency: Per-Contract\n  billingCurrency: EUR/USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Siemens MindSphere\n  ServiceCategory: Industrial IoT\n  ProviderName: Siemens\n  PublisherName: Siemens AG\n  InvoiceIssuerName: Siemens AG\n  BillingCurrency: EUR\nmeters:\n  - name: tenant_subscription\n    description: Tenant subscription fee covering platform access, included assets, and base data ingest.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - region\n  - name: asset_or_agent_count\n    description: Number of connected industrial assets/agents against the contracted ceiling; primary\n      MindSphere/Insights Hub sizing dimension.\n    unit: asset\n    aggregation: max\n    dimensions:\n      - tenant\n      - asset_type\n  - name: data_ingest\n    description: Time-series and event data volume\
  \ ingested into the tenant; usually capped per contract.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - tenant\n      - source\nprinciples:\n  - name: Visibility\n    description: Visibility is via the tenant admin console (assets, agents, data volume) and the\n      Siemens enterprise invoice; no FOCUS export is publicly documented.\n  - name: Allocation\n    description: Allocate by tenant, plant/site, asset family, and the engineering team operating\n      the connected equipment.\n  - name: Optimization\n    description: Optimize by retiring offline assets, sampling time-series at appropriate rates, and\n      right-sizing tenant capacity at renewal rather than running at burst headroom continuously.\n  - name: Accountability\n    description: OT plant managers and central IIoT platform owners share accountability; procurement\n      owns the contract and renewal terms.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/siemens-mindsphere/refs/heads/main/finops/siemens-mindsphere-finops.yml
sources:
- https://siemens.mindsphere.io/
specification: FinOps Framework
tags:
- Industrial IoT
- IIoT
- Insights Hub
- FinOps
- FOCUS
---
