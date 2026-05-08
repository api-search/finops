---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-photoshop-api-openapi-original.yml
  format: yaml
  label: Adobe Photoshop API
  slug: photoshop-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-photoshop/refs/heads/main/openapi/adobe-photoshop-api-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Refund
  pricingCategory: Subscription + Generative Credits
description: 'FOCUS-aligned FinOps shape for Adobe Photoshop: per-seat Creative Cloud subscription (Photography, Single App, or All Apps) plus generative-credit metering for Firefly Photoshop server-side APIs.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Creative SaaS
  ServiceName: Adobe Photoshop
layout: finops
meters:
- aggregation: sum
  description: Per-seat Photoshop subscription (Photography, Single App, or All Apps)
  dimensions:
  - sku
  - geography
  name: photoshop_seat
  unit: seat-month
- aggregation: sum
  description: Firefly Photoshop API generative-credit consumption
  dimensions:
  - api
  - account
  name: photoshop_generative_credits
  unit: credit
- aggregation: max
  description: Cloud storage consumed per Photoshop seat (included; tracked for capacity)
  dimensions:
  - seat
  name: cloud_storage
  unit: GB-month
name: Adobe Photoshop Finops
provider_name: Adobe Photoshop
provider_slug: adobe-photoshop
publisher_name: Adobe Inc.
service_category: Creative SaaS
slug: adobe-photoshop-finops
source_filename: adobe-photoshop-finops.yml
source_heading: FinOps Profile
source_url: https://www.adobe.com/products/photoshop/plans.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Photoshop\nproviderId: adobe-photoshop\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Photo\n  - Image Editing\n  - Generative AI\nnotes: >-\n  Photoshop is per-seat SaaS (Photography, Single App, or All Apps) plus\n  optional generative-credit usage for Firefly Photoshop APIs. Public\n  list prices were not retrievable via WebFetch.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe Photoshop: per-seat Creative Cloud\n  subscription (Photography, Single App, or All Apps) plus generative-credit\n  metering for Firefly Photoshop server-side APIs.\nsources:\n  - https://www.adobe.com/products/photoshop/plans.html\n  - https://developer.adobe.com/firefly-services/docs/photoshop/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\nserviceCategory: Creative SaaS\nbillingModel:\n  pricingCategory: Subscription + Generative Credits\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Refund\nfocusColumns:\n  ServiceName: Adobe Photoshop\n  ServiceCategory: Creative SaaS\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\nmeters:\n  - name: photoshop_seat\n    description: Per-seat Photoshop subscription (Photography, Single App, or All Apps)\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - sku\n      - geography\n  - name: photoshop_generative_credits\n    description: Firefly Photoshop API generative-credit consumption\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api\n      - account\n  - name: cloud_storage\n    description:\
  \ Cloud storage consumed per Photoshop seat (included; tracked for capacity)\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - seat\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Adobe Admin Console for seat usage; Firefly Services\n      dashboard for generative-credit burn against Photoshop API.\n  - name: Allocation\n    description: >-\n      Tag seats with department metadata in the Admin Console; attribute\n      Photoshop API calls to consuming team via API key per integration.\n  - name: Optimization\n    description: >-\n      Right-size between Photography (cheapest), Single App, and All Apps\n      based on actual usage; cache server-side render outputs;\n      reserve high-credit calls (high-resolution generative fill) for\n      final assets and use lower-resolution drafts for iteration.\n  - name: Accountability\n    description: >-\n      Design / creative team owner accountable for active seat count;\n      engineering owner accountable\
  \ for Firefly Photoshop API credit burn.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-photoshop/refs/heads/main/finops/adobe-photoshop-finops.yml
sources:
- https://www.adobe.com/products/photoshop/plans.html
- https://developer.adobe.com/firefly-services/docs/photoshop/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Photo
- Image Editing
- Generative AI
---
