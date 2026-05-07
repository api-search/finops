---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: wegowise-openapi.yml
  format: yaml
  label: WegoWise API
  slug: wegowise
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wegowise/refs/heads/main/openapi/wegowise-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps placement for WegoWise (Comply, AppFolio). Spend is a SaaS subscription scaled to the portfolio (buildings / units), not a metered API surface; FOCUS mapping reflects subscription billing only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AppFolio, Inc.
  ProviderName: WegoWise
  PublisherName: AppFolio, Inc.
  ServiceCategory: Building Energy / Benchmarking SaaS
  ServiceName: WegoWise
layout: finops
meters:
- aggregation: sum
  description: WegoWise / Comply benchmarking subscription, scaled by portfolio size and tier.
  dimensions:
  - tier
  - portfolio_size
  name: subscription_fee
  unit: month
name: Wegowise Finops
provider_name: WegoWise
provider_slug: wegowise
publisher_name: AppFolio, Inc.
service_category: Building Energy / Benchmarking SaaS
slug: wegowise-finops
source_filename: wegowise-finops.yml
source_heading: FinOps Profile
source_url: https://www.wegowise.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: WegoWise\nproviderId: wegowise\npublisherName: AppFolio, Inc.\nserviceCategory: Building Energy / Benchmarking SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Benchmarking\n  - Building Energy\n  - Energy Efficiency\n  - Multifamily\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps placement for WegoWise (Comply, AppFolio). Spend is a SaaS subscription scaled to\n  the portfolio (buildings / units), not a metered API surface; FOCUS mapping reflects subscription\n  billing only.\nnotes: No public usage-billing API. Publisher reflects current ownership; verify legal entity at\n  contract time.\nsources:\n\
  \  - https://www.wegowise.com/\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: WegoWise\n  ServiceCategory: Building Energy / Benchmarking SaaS\n  ProviderName: WegoWise\n  PublisherName: AppFolio, Inc.\n  InvoiceIssuerName: AppFolio, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    description: WegoWise / Comply benchmarking subscription, scaled by portfolio size and tier.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - portfolio_size\nprinciples:\n  - name: Visibility\n    description: Spend visibility comes from the WegoWise / Comply subscription invoice and the\n      portfolio-size record on the customer's account.\n  - name: Allocation\n    description: Allocate WegoWise spend across owners / portfolios / buildings using the platform's\n      portfolio hierarchy and internal property-management cost-center tags.\n\
  \  - name: Optimization\n    description: Cost levers are tier selection (Premium / Pro / Home), portfolio rationalization, and\n      multi-year commitments at renewal.\n  - name: Accountability\n    description: Sustainability / asset-management leads in the property owner / manager organization\n      hold accountability and coordinate renewals with WegoWise account management.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wegowise/refs/heads/main/finops/wegowise-finops.yml
sources:
- https://www.wegowise.com/
specification: FinOps Framework
tags:
- Benchmarking
- Building Energy
- Energy Efficiency
- Multifamily
- FinOps
- FOCUS
- Contact Sales
---
