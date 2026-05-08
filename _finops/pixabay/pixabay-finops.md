---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Free
description: 'FOCUS-aligned FinOps profile for Pixabay. The API is free; there is no invoice or charge from Pixabay for API usage. The only operating cost is internal: caching infrastructure to satisfy the 24-hour cache requirement and honor the 100 RPM ceiling.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Pixabay
  ProviderName: Pixabay
  PublisherName: Pixabay
  ServiceCategory: Stock Media
  ServiceName: Pixabay API
layout: finops
meters:
- aggregation: sum
  description: Pixabay API request count (free; observability only).
  dimensions:
  - app
  - endpoint
  name: api_requests
  unit: request
name: Pixabay Finops
provider_name: Pixabay
provider_slug: pixabay
publisher_name: Pixabay
service_category: Stock Media
slug: pixabay-finops
source_filename: pixabay-finops.yml
source_heading: FinOps Profile
source_url: https://pixabay.com/api/docs/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pixabay\nproviderId: pixabay\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Stock Media\n- Images\n- Videos\n- Illustrations\n- Free\n- Search\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Pixabay. The API is free; there is no invoice or charge from\n  Pixabay for API usage. The only operating cost is internal: caching infrastructure to satisfy the\n  24-hour cache requirement and honor the 100 RPM ceiling.\nnotes: Zero direct cost; internal caching infrastructure is the only cost driver.\nsources:\n- https://pixabay.com/api/docs/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Pixabay\nserviceCategory: Stock Media\nbillingModel:\n  pricingCategory: Free\n  billingFrequency: N/A\n  billingCurrency: N/A\n  chargeCategories:\n  - Usage\nfocusColumns:\n  ServiceName: Pixabay API\n  ServiceCategory: Stock Media\n  ProviderName: Pixabay\n  PublisherName: Pixabay\n  InvoiceIssuerName: Pixabay\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_requests\n  description: Pixabay API request count (free; observability only).\n  unit: request\n  aggregation: sum\n  dimensions:\n  - app\n  - endpoint\nprinciples:\n- name: Visibility\n  description: Track API call volume internally; no provider invoice.\n- name: Allocation\n  description: Allocate any caching infrastructure costs to the consuming product.\n- name: Optimization\n  description: Implement aggressive caching to stay within 100 RPM.\n- name: Accountability\n  description: App owner manages the API key.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pixabay/refs/heads/main/finops/pixabay-finops.yml
sources:
- https://pixabay.com/api/docs/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Stock Media
- Images
- Videos
- Illustrations
- Free
- Search
- FinOps
- Cost Management
- FOCUS
---
