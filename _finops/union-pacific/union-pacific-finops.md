---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: union-pacific-api.yaml
  format: yaml
  label: Union Pacific API
  slug: union-pacific
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/union-pacific/refs/heads/main/openapi/union-pacific-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Union Pacific does not expose a metered API billing model. API usage is bundled with the freight customer relationship; FinOps spend is dominated by freight commercial terms, not API metering.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Union Pacific Railroad Company
  ProviderName: Union Pacific
  PublisherName: Union Pacific Railroad Company
  ServiceCategory: Freight Rail
  ServiceName: Union Pacific
layout: finops
meters:
- aggregation: sum
  description: API access bundled into the underlying freight customer contract.
  name: contract
  unit: varies
name: Union Pacific Finops
provider_name: Union Pacific
provider_slug: union-pacific
publisher_name: Union Pacific Railroad Company
service_category: Freight Rail
slug: union-pacific-finops
source_filename: union-pacific-finops.yml
source_heading: FinOps Profile
source_url: https://www.up.com/customers/index.htm
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Union Pacific\nproviderId: union-pacific\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Freight\n  - Railroads\n  - FinOps\n  - FOCUS\n  - B2B\ndescription: Union Pacific does not expose a metered API billing model. API usage is bundled with\n  the freight customer relationship; FinOps spend is dominated by freight commercial terms, not\n  API metering.\nsources:\n  - https://www.up.com/customers/index.htm\nnotes: No public usage-based API billing exists. This artifact captures the contractual surface only;\n  consumers should treat API access as part of the freight commercial relationship with Union Pacific.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Union Pacific Railroad Company\nserviceCategory: Freight Rail\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Union Pacific\n  ServiceCategory: Freight Rail\n  ProviderName: Union Pacific\n  PublisherName: Union Pacific Railroad Company\n  InvoiceIssuerName: Union Pacific Railroad Company\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract\n    description: API access bundled into the underlying freight customer contract.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: API consumption is not separately metered. Track API call volume internally for\n      operational health rather than direct cost.\n  - name: Allocation\n    description: Allocate API integration cost to the freight customer cost center, since access\n      is bundled with shipping commercial terms.\n  - name: Optimization\n  \
  \  description: Optimize API call volume against the underlying business throughput (shipments,\n      waybills) rather than per-call pricing.\n  - name: Accountability\n    description: Assign ownership to the team managing the Union Pacific commercial relationship;\n      API usage anomalies signal operational, not financial, issues.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/union-pacific/refs/heads/main/finops/union-pacific-finops.yml
sources:
- https://www.up.com/customers/index.htm
specification: FinOps Framework
tags:
- Freight
- Railroads
- FinOps
- FOCUS
- B2B
---
