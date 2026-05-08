---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: decision-api-openapi.yml
  format: yaml
  label: AB Tasty Decision API
  slug: ab-tasty-decision-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ab-tasty/refs/heads/main/openapi/decision-api-openapi.yml
billing_model:
  billingCurrency: USD/EUR
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription
description: AB Tasty is sold as an annual contract priced by traffic volume and feature scope. There is no public per-call price; FinOps mapping focuses on the contract structure and traffic-tier meters.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AB Tasty SAS
  PricingCategory: Subscription
  ProviderName: AB Tasty
  PublisherName: AB Tasty SAS
  ServiceCategory: Experimentation / Personalization
  ServiceName: AB Tasty
layout: finops
meters:
- aggregation: max
  description: Tracked unique visitors per month — typical traffic-tier meter for experimentation contracts.
  dimensions:
  - site
  - region
  name: monthly_unique_visitors
  unit: visitor
- aggregation: sum
  description: Pageviews subjected to experimentation / personalization rules.
  dimensions:
  - site
  - campaign
  name: pageviews
  unit: pageview
- aggregation: sum
  description: Feature-flag evaluations served by Flagship / release-management SDKs.
  dimensions:
  - environment
  - feature
  name: feature_flag_evaluations
  unit: evaluation
- aggregation: count
  description: Annual subscription line item.
  dimensions:
  - plan
  name: contract_year
  unit: year
name: Ab Tasty Finops
provider_name: AB Tasty
provider_slug: ab-tasty
publisher_name: AB Tasty SAS
service_category: Experimentation / Personalization
slug: ab-tasty-finops
source_filename: ab-tasty-finops.yml
source_heading: FinOps Profile
source_url: https://www.abtasty.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AB Tasty\nproviderId: ab-tasty\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Experimentation\n  - A/B Testing\n  - Personalization\n  - Feature Flags\n  - FinOps\n  - FOCUS\ndescription: AB Tasty is sold as an annual contract priced by traffic volume and feature scope. There\n  is no public per-call price; FinOps mapping focuses on the contract structure and traffic-tier meters.\nnotes: No public developer pricing — placeholder only. Plan price is quoted per opportunity by AB Tasty\n  sales.\nsources:\n  - https://www.abtasty.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AB Tasty SAS\nserviceCategory: Experimentation / Personalization\n\
  billingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD/EUR\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: AB Tasty\n  ServiceCategory: Experimentation / Personalization\n  ProviderName: AB Tasty\n  PublisherName: AB Tasty SAS\n  InvoiceIssuerName: AB Tasty SAS\n  BillingCurrency: USD\n  PricingCategory: Subscription\nmeters:\n  - name: monthly_unique_visitors\n    description: Tracked unique visitors per month — typical traffic-tier meter for experimentation contracts.\n    unit: visitor\n    aggregation: max\n    dimensions:\n      - site\n      - region\n  - name: pageviews\n    description: Pageviews subjected to experimentation / personalization rules.\n    unit: pageview\n    aggregation: sum\n    dimensions:\n      - site\n      - campaign\n  - name: feature_flag_evaluations\n    description: Feature-flag evaluations served by Flagship / release-management SDKs.\n    unit: evaluation\n    aggregation:\
  \ sum\n    dimensions:\n      - environment\n      - feature\n  - name: contract_year\n    description: Annual subscription line item.\n    unit: year\n    aggregation: count\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Use AB Tasty dashboards and the analytics export to track campaign volume against the\n      contracted traffic ceiling each month.\n  - name: Allocation\n    description: Tag campaigns and feature flags by product team / business unit so cost can be allocated\n      against the products driving experimentation volume.\n  - name: Optimization\n    description: Sunset stale campaigns and stop running long-tail experiments to keep traffic inside\n      the contracted tier; consolidate environments.\n  - name: Accountability\n    description: Growth / product leadership owns the AB Tasty subscription; engineering owns Flagship\n      SDK integrations. Review traffic vs contract ceiling monthly with the AB Tasty CSM.\nmaintainers:\n  -\
  \ FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ab-tasty/refs/heads/main/finops/ab-tasty-finops.yml
sources:
- https://www.abtasty.com/pricing/
specification: FinOps Framework
tags:
- Experimentation
- A/B Testing
- Personalization
- Feature Flags
- FinOps
- FOCUS
---
