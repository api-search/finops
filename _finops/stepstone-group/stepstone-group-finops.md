---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: StepStone Group has no public, metered API surface. Costs land inside the broader institutional / advisory client engagement (advisory fees, fund commitments), not as a per-call API line; nothing public to reconcile against the FOCUS spec.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: StepStone Group Inc.
  ProviderName: StepStone Group
  PublisherName: StepStone Group Inc.
  ServiceCategory: Private Markets / Investment Management
  ServiceName: StepStone Group
layout: finops
meters:
- aggregation: sum
  description: Placeholder for line items defined in a StepStone institutional / advisory contract.
  name: contracted_engagement
  unit: varies
name: Stepstone Group Finops
provider_name: StepStone Group
provider_slug: stepstone-group
publisher_name: StepStone Group Inc.
service_category: Private Markets / Investment Management
slug: stepstone-group-finops
source_filename: stepstone-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.stepstonegroup.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: StepStone Group\nproviderId: stepstone-group\npublisherName: StepStone Group Inc.\nserviceCategory: Private Markets / Investment Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Private Markets\n  - Investment Management\ndescription: StepStone Group has no public, metered API surface. Costs land inside the broader institutional\n  / advisory client engagement (advisory fees, fund commitments), not as a per-call API line; nothing\n  public to reconcile against the FOCUS spec.\nsources:\n  - https://www.stepstonegroup.com/\nnotes: No public StepStone API billing surface. Meters and FOCUS\
  \ columns are placeholders pending a\n  contracted engagement.\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: StepStone Group\n  ServiceCategory: Private Markets / Investment Management\n  ProviderName: StepStone Group\n  PublisherName: StepStone Group Inc.\n  InvoiceIssuerName: StepStone Group Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_engagement\n    description: Placeholder for line items defined in a StepStone institutional / advisory contract.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is whatever client / advisory reporting StepStone provides under the underlying\n      mandate — there is no public usage / billing API.\n  - name: Allocation\n    description: Allocate StepStone-related fees and data costs in your own portfolio cost system against\n      the underlying mandate, fund,\
  \ or advisory engagement.\n  - name: Optimization\n    description: Optimization happens via mandate / fee renegotiation and product-mix decisions, not\n      via API plan changes.\n  - name: Accountability\n    description: A named investment / portfolio owner should hold the StepStone engagement cost line\n      and renewal review.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stepstone-group/refs/heads/main/finops/stepstone-group-finops.yml
sources:
- https://www.stepstonegroup.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Private Markets
- Investment Management
---
