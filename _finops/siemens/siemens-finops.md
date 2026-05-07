---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: siemens-building-operations-openapi.yml
  format: yaml
  label: Siemens Building Operations API
  slug: building-operations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/siemens/refs/heads/main/openapi/siemens-building-operations-openapi.yml
billing_model:
  billingCurrency: EUR/USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Enterprise License / Contract
description: FOCUS-aligned FinOps placeholder for Siemens. Siemens does not bill API consumption as a discrete line; cost is bundled into the underlying industrial software license or platform contract. No public usage telemetry or per-call billing surface is documented at the corporate level.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Siemens AG
  ProviderName: Siemens
  PublisherName: Siemens AG
  ServiceCategory: Industrial Software
  ServiceName: Siemens
layout: finops
meters:
- aggregation: sum
  description: Siemens product license fee (per-product, per-seat, or per-asset depending on the product line); APIs ride on top of the licensed product.
  dimensions:
  - product
  - region
  name: license_subscription
  unit: varies
name: Siemens Finops
provider_name: Siemens
provider_slug: siemens
publisher_name: Siemens AG
service_category: Industrial Software
slug: siemens-finops
source_filename: siemens-finops.yml
source_heading: FinOps Profile
source_url: https://www.siemens.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Siemens\nproviderId: siemens\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Industry\n  - Industrial IoT\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Siemens. Siemens does not bill API consumption as\n  a discrete line; cost is bundled into the underlying industrial software license or platform contract.\n  No public usage telemetry or per-call billing surface is documented at the corporate level.\nsources:\n  - https://www.siemens.com/\nnotes: No corporate-wide API billing model. FinOps treatment is product-specific; reconciliation\n  pending direct vendor confirmation per Siemens product.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Siemens AG\nserviceCategory: Industrial Software\nbillingModel:\n  pricingCategory: Enterprise License / Contract\n  billingFrequency: Per-Contract\n  billingCurrency: EUR/USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Siemens\n  ServiceCategory: Industrial Software\n  ProviderName: Siemens\n  PublisherName: Siemens AG\n  InvoiceIssuerName: Siemens AG\n  BillingCurrency: EUR\nmeters:\n  - name: license_subscription\n    description: Siemens product license fee (per-product, per-seat, or per-asset depending on the\n      product line); APIs ride on top of the licensed product.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\n      - region\nprinciples:\n  - name: Visibility\n    description: Spend visibility comes from the Siemens enterprise software invoice and asset/seat\n      management within each product, not a unified usage API at the corporate level.\n  - name: Allocation\n    description: Allocate by Siemens product\
  \ line, plant/site, and the engineering team operating the\n      asset; tie back to procurement contract IDs.\n  - name: Optimization\n    description: Optimization is contractual and architectural — consolidate Siemens products, right-size\n      seats and assets at renewal, and minimize duplicated platforms within the same plant.\n  - name: Accountability\n    description: Operations technology and procurement own the Siemens contract; integration teams\n      own technical SLA conformance for each product API.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/siemens/refs/heads/main/finops/siemens-finops.yml
sources:
- https://www.siemens.com/
specification: FinOps Framework
tags:
- Industry
- Industrial IoT
- FinOps
- FOCUS
---
