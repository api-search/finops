---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: unisys-stealth-ecoapi-openapi.yaml
  format: yaml
  label: Unisys Stealth EcoAPI
  slug: unisys-stealth-ecoapi
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unisys/refs/heads/main/openapi/unisys-stealth-ecoapi-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Unisys does not expose a metered API billing model. Spend is governed by managed-services and consulting contracts; FinOps maps to engagement-level cost rather than per-API-call.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Unisys Corporation
  ProviderName: Unisys
  PublisherName: Unisys Corporation
  ServiceCategory: IT Services
  ServiceName: Unisys
layout: finops
meters:
- aggregation: sum
  description: Unisys managed-services or consulting engagement billed under negotiated terms.
  name: contract
  unit: varies
name: Unisys Finops
provider_name: Unisys
provider_slug: unisys
publisher_name: Unisys Corporation
service_category: IT Services
slug: unisys-finops
source_filename: unisys-finops.yml
source_heading: FinOps Profile
source_url: https://www.unisys.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Unisys\nproviderId: unisys\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - IT Services\n  - Cybersecurity\n  - FinOps\n  - FOCUS\n  - B2B\ndescription: Unisys does not expose a metered API billing model. Spend is governed by managed-services\n  and consulting contracts; FinOps maps to engagement-level cost rather than per-API-call.\nsources:\n  - https://www.unisys.com/\nnotes: No public usage-based API billing exists. Treat as contract-driven; this artifact captures\n  the contractual surface only.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Unisys Corporation\nserviceCategory: IT Services\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency:\
  \ Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Unisys\n  ServiceCategory: IT Services\n  ProviderName: Unisys\n  PublisherName: Unisys Corporation\n  InvoiceIssuerName: Unisys Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract\n    description: Unisys managed-services or consulting engagement billed under negotiated terms.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: API consumption is not separately metered. Track usage internally against contracted\n      service levels rather than per-call cost.\n  - name: Allocation\n    description: Allocate Unisys spend at the engagement level (per managed service or solution),\n      typically already tied to a business owner.\n  - name: Optimization\n    description: Optimization happens at contract renewal, scope adjustment, and consolidation across\n      Unisys services rather than per-API-call.\n\
  \  - name: Accountability\n    description: Assign ownership to the executive sponsor of each Unisys engagement; FinOps signals\n      come from invoice review and SLA dashboards.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unisys/refs/heads/main/finops/unisys-finops.yml
sources:
- https://www.unisys.com/
specification: FinOps Framework
tags:
- IT Services
- Cybersecurity
- FinOps
- FOCUS
- B2B
---
