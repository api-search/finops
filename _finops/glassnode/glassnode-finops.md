---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Subscription
  - Adjustment
  pricingCategory: Subscription
description: FinOps view of Glassnode. Subscription-based, with Studio access at lower tiers and API access starting at Professional or via institutional add-on. Institutional contracts include redistribution rights and dedicated SLA.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Glassnode
  ProviderName: Glassnode
  PublisherName: Glassnode
  ServiceCategory: Crypto Analytics
  ServiceName: Glassnode Metrics API
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription per Studio seat / API key.
  dimensions:
  - api_key
  name: subscription
  unit: month
name: Glassnode Finops
provider_name: Glassnode
provider_slug: glassnode
publisher_name: Glassnode
service_category: Crypto Analytics
slug: glassnode-finops
source_filename: glassnode-finops.yml
source_heading: FinOps Profile
source_url: https://studio.glassnode.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Glassnode\nproviderId: glassnode\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Crypto\n  - On-Chain\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Glassnode. Subscription-based, with Studio access at lower tiers and API access\n  starting at Professional or via institutional add-on. Institutional contracts include\n  redistribution rights and dedicated SLA.\nsources:\n  - https://studio.glassnode.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Glassnode\nserviceCategory: Crypto Analytics\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Subscription\n    - Adjustment\nfocusColumns:\n  ServiceName: Glassnode Metrics API\n  ServiceCategory: Crypto Analytics\n  ProviderName: Glassnode\n  PublisherName: Glassnode\n  InvoiceIssuerName: Glassnode\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly subscription per Studio seat / API key.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Tag each API key to a single owning workload.\n  - name: Allocation\n    description: Allocate subscription across consuming research teams.\n  - name: Optimization\n    description: Use Studio dashboards where possible; reserve API for automated workflows.\n  - name: Accountability\n    description: Assign a billing owner; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/glassnode/refs/heads/main/finops/glassnode-finops.yml
sources:
- https://studio.glassnode.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Crypto
- On-Chain
- FinOps
- FOCUS
---
