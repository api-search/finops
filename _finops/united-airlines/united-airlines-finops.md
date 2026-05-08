---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: united-airlines-ndc-openapi.yml
  format: yaml
  label: United Airlines NDC API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-airlines/main/openapi/united-airlines-ndc-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: United Airlines does not expose a metered API billing model. API/content access is bundled with NDC, GDS, and corporate distribution agreements; FinOps maps to ticketing and distribution spend rather than per-call billing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: United Airlines, Inc.
  ProviderName: United Airlines
  PublisherName: United Airlines, Inc.
  ServiceCategory: Travel
  ServiceName: United Airlines
layout: finops
meters:
- aggregation: sum
  description: NDC / GDS / direct distribution agreement covering API and content access.
  name: distribution_agreement
  unit: varies
name: United Airlines Finops
provider_name: United Airlines
provider_slug: united-airlines
publisher_name: United Airlines, Inc.
service_category: Travel
slug: united-airlines-finops
source_filename: united-airlines-finops.yml
source_heading: FinOps Profile
source_url: https://www.united.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: United Airlines\nproviderId: united-airlines\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Airlines\n  - Travel\n  - NDC\n  - FinOps\n  - FOCUS\n  - B2B\ndescription: United Airlines does not expose a metered API billing model. API/content access is bundled\n  with NDC, GDS, and corporate distribution agreements; FinOps maps to ticketing and distribution\n  spend rather than per-call billing.\nsources:\n  - https://www.united.com\nnotes: No public usage-based API billing exists. This artifact captures the contractual surface only.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: United Airlines, Inc.\nserviceCategory: Travel\nbillingModel:\n  pricingCategory:\
  \ Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: United Airlines\n  ServiceCategory: Travel\n  ProviderName: United Airlines\n  PublisherName: United Airlines, Inc.\n  InvoiceIssuerName: United Airlines, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: distribution_agreement\n    description: NDC / GDS / direct distribution agreement covering API and content access.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: API consumption is not separately metered. Track query volume against the negotiated\n      partner SLA rather than dollar-per-call.\n  - name: Allocation\n    description: Allocate United integration cost to the travel-procurement or distribution function;\n      ticket cost is the dominant downstream financial line.\n  - name: Optimization\n    description: Optimize at the contract level - NDC vs GDS routing, corporate-rate\
  \ consolidation,\n      caching availability calls - rather than per-API-call.\n  - name: Accountability\n    description: Assign ownership to the team that holds the United distribution contract; review\n      partner usage reports against contracted volumes.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/united-airlines/refs/heads/main/finops/united-airlines-finops.yml
sources:
- https://www.united.com
specification: FinOps Framework
tags:
- Airlines
- Travel
- NDC
- FinOps
- FOCUS
- B2B
---
