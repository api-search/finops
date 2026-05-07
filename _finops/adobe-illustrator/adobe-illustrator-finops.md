---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-illustrator-scripting-openapi-original.yml
  format: yaml
  label: Adobe Illustrator Scripting API
  slug: scripting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-illustrator/refs/heads/main/openapi/adobe-illustrator-scripting-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Refund
  pricingCategory: Subscription + Generative Credits
description: 'FOCUS-aligned FinOps shape for Adobe Illustrator: per-seat Creative Cloud subscription (Single App or All Apps) plus generative-credit metering for Firefly Vector / Pattern / Recolor APIs.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Creative SaaS
  ServiceName: Adobe Illustrator
layout: finops
meters:
- aggregation: sum
  description: Per-seat Illustrator subscription (Single App or All Apps)
  dimensions:
  - sku
  - geography
  name: illustrator_seat
  unit: seat-month
- aggregation: sum
  description: Firefly Vector / Pattern / Recolor API generative-credit consumption
  dimensions:
  - api
  - account
  name: vector_generative_credits
  unit: credit
name: Adobe Illustrator Finops
provider_name: Adobe Illustrator
provider_slug: adobe-illustrator
publisher_name: Adobe Inc.
service_category: Creative SaaS
slug: adobe-illustrator-finops
source_filename: adobe-illustrator-finops.yml
source_heading: FinOps Profile
source_url: https://www.adobe.com/products/illustrator/plans.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Illustrator\nproviderId: adobe-illustrator\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Illustration\n  - Generative AI\nnotes: >-\n  Illustrator is per-seat SaaS (Single App or All Apps) plus optional\n  generative-credit usage for Firefly vector APIs. Public list prices\n  were not retrievable via WebFetch.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe Illustrator: per-seat Creative\n  Cloud subscription (Single App or All Apps) plus generative-credit\n  metering for Firefly Vector / Pattern / Recolor APIs.\nsources:\n  - https://www.adobe.com/products/illustrator/plans.html\n  - https://developer.adobe.com/firefly-services/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\nserviceCategory: Creative SaaS\nbillingModel:\n  pricingCategory: Subscription + Generative Credits\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Refund\nfocusColumns:\n  ServiceName: Adobe Illustrator\n  ServiceCategory: Creative SaaS\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\nmeters:\n  - name: illustrator_seat\n    description: Per-seat Illustrator subscription (Single App or All Apps)\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - sku\n      - geography\n  - name: vector_generative_credits\n    description: Firefly Vector / Pattern / Recolor API generative-credit consumption\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api\n      - account\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Adobe\
  \ Admin Console for seat usage; Firefly Services dashboard\n      for generative-credit burn against Vector API.\n  - name: Allocation\n    description: >-\n      Tag seats with department metadata in the Admin Console; attribute\n      Vector API calls to consuming team via API key per integration.\n  - name: Optimization\n    description: >-\n      Move occasional users from Single App to a shared All Apps seat where\n      they need other tools; cache vector outputs server-side; route bulk\n      pattern generation through Firefly Services bundles instead of\n      ad-hoc API calls.\n  - name: Accountability\n    description: >-\n      Design-team owner accountable for active seat count; engineering\n      owner accountable for Vector API generative-credit burn rate.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-illustrator/refs/heads/main/finops/adobe-illustrator-finops.yml
sources:
- https://www.adobe.com/products/illustrator/plans.html
- https://developer.adobe.com/firefly-services/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Illustration
- Generative AI
---
