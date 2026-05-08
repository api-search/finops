---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Not Applicable
  pricingCategory: Not Applicable
description: TPG Inc. is an asset manager rather than an API/SaaS vendor. The FinOps framework does not meaningfully apply because there is no consumption-billed API surface; LP economics (management fees, carried interest) are governed by fund agreements and are out of scope.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TPG Inc.
  ProviderName: TPG Inc
  PublisherName: TPG Inc.
  ServiceCategory: Alternative Asset Management
  ServiceName: TPG
layout: finops
meters:
- aggregation: sum
  description: TPG does not bill on a consumption meter. LP-level fund economics are governed by partnership agreements, not by FOCUS columns.
  name: not_applicable
  unit: varies
name: Tpg Finops
provider_name: TPG Inc
provider_slug: tpg
publisher_name: TPG Inc.
service_category: Alternative Asset Management
slug: tpg-finops
source_filename: tpg-finops.yml
source_heading: FinOps Profile
source_url: https://www.tpg.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: TPG Inc\nproviderId: tpg\npublisherName: TPG Inc.\nserviceCategory: Alternative Asset Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Private Equity\n  - Alternative Assets\n  - Investment Management\n  - FinOps\n  - FOCUS\ndescription: TPG Inc. is an asset manager rather than an API/SaaS vendor. The FinOps framework does not\n  meaningfully apply because there is no consumption-billed API surface; LP economics (management fees,\n  carried interest) are governed by fund agreements and are out of scope.\nsources:\n  - https://www.tpg.com/\nnotes: Not an API provider; no FOCUS-aligned consumption meters apply.\n\
  billingModel:\n  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Not Applicable\nfocusColumns:\n  ServiceName: TPG\n  ServiceCategory: Alternative Asset Management\n  ProviderName: TPG Inc\n  PublisherName: TPG Inc.\n  InvoiceIssuerName: TPG Inc.\n  BillingCurrency: USD\nmeters:\n  - name: not_applicable\n    description: TPG does not bill on a consumption meter. LP-level fund economics are governed by partnership\n      agreements, not by FOCUS columns.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Not applicable — fund-level reporting is provided through investor-relations channels,\n      not through a self-service usage API.\n  - name: Allocation\n    description: Not applicable at the API level; LP capital accounts are allocated per the partnership\n      agreement.\n  - name: Optimization\n    description: Not applicable — there are no consumption levers to optimize.\n\
  \  - name: Accountability\n    description: LP relationship managers handle commercial accountability; not a FinOps surface.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tpg/refs/heads/main/finops/tpg-finops.yml
sources:
- https://www.tpg.com/
specification: FinOps Framework
tags:
- Private Equity
- Alternative Assets
- Investment Management
- FinOps
- FOCUS
---
