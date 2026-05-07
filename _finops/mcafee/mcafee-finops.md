---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mcafee-epo-openapi.yml
  format: yaml
  label: McAfee ePO API
  slug: mcafee-epo-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/openapi/mcafee-epo-openapi.yml
- filename: mcafee-mvision-openapi.yml
  format: yaml
  label: McAfee MVISION API
  slug: mcafee-mvision-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/openapi/mcafee-mvision-openapi.yml
- filename: mcafee-web-gateway-openapi.yml
  format: yaml
  label: McAfee Web Gateway API
  slug: mcafee-web-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/openapi/mcafee-web-gateway-openapi.yml
- filename: mcafee-esm-openapi.yml
  format: yaml
  label: McAfee ESM API
  slug: mcafee-esm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/openapi/mcafee-esm-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Per-Seat / Per-Node Subscription
description: 'FOCUS-aligned FinOps shape for McAfee / Trellix: per-seat / per-node enterprise license for the underlying security product, with API access bundled inside the product license rather than metered separately. Consumer McAfee is per-subscription seat licensing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Musarubra US LLC (Trellix) / McAfee, LLC
  ProviderName: McAfee / Trellix
  PublisherName: Musarubra US LLC (Trellix) / McAfee, LLC
  ServiceCategory: Cybersecurity Software
  ServiceName: McAfee / Trellix Security Platform
layout: finops
meters:
- aggregation: max
  description: Endpoints under management for ePO / Endpoint Security / XDR.
  dimensions:
  - product
  - business_unit
  - environment
  name: managed_endpoints
  unit: seat-year
- aggregation: max
  description: Sustained events-per-second ingested into ESM SIEM.
  dimensions:
  - log_source
  - business_unit
  name: siem_eps
  unit: events_per_second
- aggregation: max
  description: Users / throughput covered by Web Gateway license.
  dimensions:
  - office
  - business_unit
  name: web_gateway_users
  unit: seat-year
- aggregation: max
  description: Number of DXL brokers deployed to support fabric throughput.
  dimensions:
  - region
  - environment
  name: dxl_broker_count
  unit: instance
name: Mcafee Finops
provider_name: McAfee (Trellix)
provider_slug: mcafee
publisher_name: Musarubra US LLC (Trellix) / McAfee, LLC
service_category: Cybersecurity Software
slug: mcafee-finops
source_filename: mcafee-finops.yml
source_heading: FinOps Profile
source_url: https://www.trellix.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: McAfee (Trellix)\nproviderId: mcafee\npublisherName: Musarubra US LLC (Trellix) / McAfee, LLC\nserviceCategory: Cybersecurity Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Antivirus\n  - Cybersecurity\n  - Endpoint Protection\n  - Security\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for McAfee / Trellix: per-seat / per-node enterprise license\n  for the underlying security product, with API access bundled inside the product license rather than\n  metered separately. Consumer McAfee is per-subscription seat licensing.'\nnotes: |\n  No public per-API pricing. Cost is realized at the product\
  \ license level (seats, nodes, EPS, throughput).\n  FOCUS columns assume USD and the Trellix / Musarubra publisher entity for enterprise; consumer McAfee\n  invoices come from McAfee LLC.\nsources:\n  - https://www.trellix.com/\n  - https://www.mcafee.com/\nprinciples:\n  - name: Visibility\n    description: Use the ePO console (on-prem) and the Trellix XDR / MVISION cloud console to observe\n      seat / node consumption and license headroom; reconcile against the annual enterprise agreement\n      true-up. Pull SIEM EPS metrics from the ESM dashboard.\n  - name: Allocation\n    description: Allocate by business unit and managed-endpoint group in ePO; tag policy assignments and\n      device groups with cost-center metadata so chargeback aligns with the seat / node count actually\n      consumed.\n  - name: Optimization\n    description: Reclaim seats from decommissioned endpoints during quarterly reviews, right-size SIEM\n      EPS by tuning event filters and noisy log sources, and consolidate\
  \ broker / proxy footprint to\n      reduce VM / appliance count.\n  - name: Accountability\n    description: Assign a security-product owner per product line who reconciles the annual true-up\n      against deployed counts and negotiates renewal with the channel partner.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Per-Seat / Per-Node Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName:\
  \ McAfee / Trellix Security Platform\n  ServiceCategory: Cybersecurity Software\n  ProviderName: McAfee / Trellix\n  PublisherName: Musarubra US LLC (Trellix) / McAfee, LLC\n  InvoiceIssuerName: Musarubra US LLC (Trellix) / McAfee, LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: managed_endpoints\n    description: Endpoints under management for ePO / Endpoint Security / XDR.\n    unit: seat-year\n    aggregation: max\n    dimensions:\n      - product\n      - business_unit\n      - environment\n  - name: siem_eps\n    description: Sustained events-per-second ingested into ESM SIEM.\n    unit: events_per_second\n    aggregation: max\n    dimensions:\n      - log_source\n      - business_unit\n  - name: web_gateway_users\n    description: Users / throughput covered by Web Gateway license.\n    unit: seat-year\n    aggregation: max\n    dimensions:\n      - office\n      - business_unit\n  - name: dxl_broker_count\n    description: Number of DXL brokers deployed\
  \ to support fabric throughput.\n    unit: instance\n    aggregation: max\n    dimensions:\n      - region\n      - environment\napis:\n  - name: McAfee ePO API\n    baseURL: https://your-epo-server:8443/remote\n    tags:\n      - Endpoint Management\n      - Policy Orchestrator\n      - Security Management\n    serviceName: McAfee ePO API\n    serviceCategory: API\n  - name: McAfee MVISION API\n    baseURL: https://api.mvision.mcafee.com\n    tags:\n      - Cloud Security\n      - EDR\n      - MVISION\n      - Threat Detection\n    serviceName: McAfee MVISION API\n    serviceCategory: API\n  - name: McAfee Threat Intelligence Exchange (TIE) API\n    baseURL: https://your-tie-server/api\n    tags:\n      - Malware Analysis\n      - Reputation\n      - Threat Intelligence\n    serviceName: McAfee Threat Intelligence Exchange (TIE) API\n    serviceCategory: API\n  - name: McAfee Data Exchange Layer (DXL) API\n    baseURL: https://your-dxl-broker\n    tags:\n      - Data Exchange\n      -\
  \ Fabric\n      - Integration\n      - Messaging\n    serviceName: McAfee Data Exchange Layer (DXL) API\n    serviceCategory: API\n  - name: McAfee Web Gateway API\n    baseURL: https://your-mwg-server/Konfigurator/REST\n    tags:\n      - Proxy\n      - Web Gateway\n      - Web Security\n    serviceName: McAfee Web Gateway API\n    serviceCategory: API\n  - name: McAfee ESM API\n    baseURL: https://your-esm-server/rs/esm\n    tags:\n      - Log Management\n      - Security Events\n      - SIEM\n    serviceName: McAfee ESM API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Managed Endpoint\n    metric: billed_cost / managed_endpoints\n    target: TBD\n  - name: Cost per EPS\n    metric: siem_billed_cost / siem_eps\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mcafee/refs/heads/main/finops/mcafee-finops.yml
sources:
- https://www.trellix.com/
- https://www.mcafee.com/
specification: FinOps Framework
tags:
- Antivirus
- Cybersecurity
- Endpoint Protection
- Security
- FinOps
- FOCUS
---
