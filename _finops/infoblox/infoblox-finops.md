---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: infoblox-wapi-openapi.yml
  format: yaml
  label: Infoblox WAPI (Web API)
  slug: infoblox-wapi-web-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/infoblox/refs/heads/main/openapi/infoblox-wapi-openapi.yml
- filename: openapi.yaml
  format: yaml
  label: Infoblox BloxOne API
  slug: infoblox-bloxone-api
  spec_type: OpenAPI
  url: https://csp.infoblox.com/apidoc/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Enterprise Subscription
description: FOCUS-aligned FinOps shape for Infoblox. Billing is enterprise subscription (per-protected-asset / per-appliance, annual) plus support; APIs are bundled. FinOps practice for Infoblox focuses on entitlement utilization, environment consolidation, and renewal-cycle right-sizing rather than per-API-call accounting.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Infoblox Inc.
  PricingCategory: Subscription
  PricingUnit: protected-asset-year
  ProviderName: Infoblox
  PublisherName: Infoblox Inc.
  ServiceCategory: Network Services + Security
  ServiceName: Infoblox Universal DDI / NIOS / Threat Defense
layout: finops
meters:
- aggregation: max
  description: Count of assets / endpoints / IP space under management or protection
  dimensions:
  - product_line
  - region
  - business_unit
  name: protected_assets
  unit: asset-month
- aggregation: max
  description: NIOS appliances (physical or virtual) under license
  dimensions:
  - model
  - data_center
  name: appliances
  unit: appliance-month
- aggregation: sum
  description: DNS queries protected by Threat Defense
  dimensions:
  - region
  - threat_category
  name: dns_queries_protected
  unit: query
name: Infoblox Finops
provider_name: Infoblox
provider_slug: infoblox
publisher_name: Infoblox Inc.
service_category: Network Services + Security
slug: infoblox-finops
source_filename: infoblox-finops.yml
source_heading: FinOps Profile
source_url: https://www.infoblox.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Infoblox\nproviderId: infoblox\npublisherName: Infoblox Inc.\nserviceCategory: Network Services + Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - DDI\n  - DNS\n  - DHCP\n  - IPAM\n  - Network Management\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Infoblox. Billing is enterprise subscription (per-protected-asset\n  / per-appliance, annual) plus support; APIs are bundled. FinOps practice for Infoblox focuses on entitlement\n  utilization, environment consolidation, and renewal-cycle right-sizing rather than per-API-call accounting.\nnotes: No public per-call or per-query meter; meters below\
  \ describe the business-level cost drivers (assets,\n  appliances, queries protected). Reconcile against the customer's own Infoblox subscription and CSP usage\n  reports.\nsources:\n  - https://www.infoblox.com/products/\n  - https://www.infoblox.com/company/contact-us/\nprinciples:\n  - name: Visibility\n    description: Use the Infoblox Cloud Services Portal to see protected-asset counts, query volume,\n      threat-intel hits, and licensed-feature utilization across the Universal DDI suite.\n  - name: Allocation\n    description: Tag managed assets in Universal DDI and NIOS by business unit / data center / cloud\n      account so renewal cost can be attributed; map appliances to cost centers in CMDB.\n  - name: Optimization\n    description: Right-size protected-asset counts at renewal; consolidate redundant on-prem NIOS appliances\n      into cloud-managed Universal DDI; retire stale extensible attributes and unused IPAM networks.\n  - name: Accountability\n    description: Designate\
  \ a Network Services owner with annual Infoblox-renewal budget; review utilization\n      and growth quarterly with the Infoblox Customer Success team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Infoblox Universal DDI / NIOS / Threat Defense\n  ServiceCategory:\
  \ Network Services + Security\n  ProviderName: Infoblox\n  PublisherName: Infoblox Inc.\n  InvoiceIssuerName: Infoblox Inc.\n  PricingCategory: Subscription\n  PricingUnit: protected-asset-year\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: protected_assets\n    description: Count of assets / endpoints / IP space under management or protection\n    unit: asset-month\n    aggregation: max\n    dimensions:\n      - product_line\n      - region\n      - business_unit\n  - name: appliances\n    description: NIOS appliances (physical or virtual) under license\n    unit: appliance-month\n    aggregation: max\n    dimensions:\n      - model\n      - data_center\n  - name: dns_queries_protected\n    description: DNS queries protected by Threat Defense\n    unit: query\n    aggregation: sum\n    dimensions:\n      - region\n      - threat_category\napis:\n  - name: Infoblox Universal DDI API\n    baseURL: https://csp.infoblox.com/api\n    serviceCategory: API\n  - name:\
  \ Infoblox NIOS WAPI\n    baseURL: https://{grid-master}/wapi/v2.x\n    serviceCategory: API\n  - name: Infoblox Cloud Services Portal API\n    baseURL: https://csp.infoblox.com/api\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Protected Asset\n    metric: billed_cost / protected_assets\n    target: TBD\n  - name: Cost per Million DNS Queries Protected\n    metric: billed_cost / (dns_queries_protected / 1000000)\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/infoblox/refs/heads/main/finops/infoblox-finops.yml
sources:
- https://www.infoblox.com/products/
- https://www.infoblox.com/company/contact-us/
specification: FinOps Framework
tags:
- DDI
- DNS
- DHCP
- IPAM
- Network Management
- FinOps
- FOCUS
---
