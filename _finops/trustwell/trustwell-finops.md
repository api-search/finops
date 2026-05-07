---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: trustwell-foodlogiq-openapi.yml
  format: yaml
  label: Trustwell FoodLogiQ API
  slug: trustwell-foodlogiq-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trustwell/refs/heads/main/openapi/trustwell-foodlogiq-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Trustwell is sold as a contracted enterprise SaaS for food manufacturers and retailers; no public pricing, metered usage API, or FOCUS-aligned export is published. FinOps surface is limited to the contracted subscription line.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Trustwell
  ProviderName: Trustwell
  PublisherName: Trustwell
  ServiceCategory: Food Safety & Compliance SaaS
  ServiceName: Trustwell
layout: finops
meters:
- aggregation: sum
  description: Contracted Trustwell subscription line covering the modules selected (Genesis labeling, FoodLogiQ supply chain, etc.).
  name: subscription
  unit: month
name: Trustwell Finops
provider_name: Trustwell
provider_slug: trustwell
publisher_name: Trustwell
service_category: Food Safety & Compliance SaaS
slug: trustwell-finops
source_filename: trustwell-finops.yml
source_heading: FinOps Profile
source_url: https://www.trustwell.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Trustwell\nproviderId: trustwell\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Food Safety\n  - Compliance\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: Trustwell is sold as a contracted enterprise SaaS for food manufacturers and retailers; no\n  public pricing, metered usage API, or FOCUS-aligned export is published. FinOps surface is limited to\n  the contracted subscription line.\nsources:\n  - https://www.trustwell.com/\nnotes: No public pricing or usage telemetry. Trimmed pending vendor disclosure.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Trustwell\nserviceCategory: Food Safety & Compliance SaaS\nbillingModel:\n  pricingCategory: Contract\n\
  \  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Trustwell\n  ServiceCategory: Food Safety & Compliance SaaS\n  ProviderName: Trustwell\n  PublisherName: Trustwell\n  InvoiceIssuerName: Trustwell\n  BillingCurrency: USD\nmeters:\n  - name: subscription\n    description: Contracted Trustwell subscription line covering the modules selected (Genesis labeling,\n      FoodLogiQ supply chain, etc.).\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is limited to the contracted subscription invoice; Trustwell does not expose\n      a public usage or cost API.\n  - name: Allocation\n    description: Allocate the Trustwell subscription to the food-safety, regulatory affairs, or supply-chain\n      function that owns the modules in use.\n  - name: Optimization\n    description: Optimization happens at renewal — re-scope the module mix (Genesis vs FoodLogiQ vs supplier\n   \
  \   onboarding) against actual usage and audit findings.\n  - name: Accountability\n    description: A regulatory or supply-chain owner manages the Trustwell relationship; finance approves\n      annual renewal terms.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trustwell/refs/heads/main/finops/trustwell-finops.yml
sources:
- https://www.trustwell.com/
specification: FinOps Framework
tags:
- Food Safety
- Compliance
- SaaS
- FinOps
- FOCUS
---
