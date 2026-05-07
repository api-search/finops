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
  - Purchase
  pricingCategory: Not Applicable
description: FOCUS-aligned FinOps placeholder for Amica Mutual Insurance. Amica has no public API metered billing surface; consumer spend is in the form of insurance premiums, which are state-regulated rather than priced as API consumption.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Amica Mutual Insurance Company
  ProviderName: Amica Mutual Insurance
  PublisherName: Amica Mutual Insurance Company
  ServiceCategory: Insurance
  ServiceName: Amica Mutual Insurance
layout: finops
meters:
- aggregation: sum
  description: Placeholder; not billed as a developer line item
  dimensions:
  - consumer
  name: api_requests
  unit: request
name: Amica Mutual Insurance Finops
provider_name: Amica Mutual Insurance
provider_slug: amica-mutual-insurance
publisher_name: Amica Mutual Insurance Company
service_category: Insurance
slug: amica-mutual-insurance-finops
source_filename: amica-mutual-insurance-finops.yml
source_heading: FinOps Profile
source_url: https://www.amica.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amica Mutual Insurance\nproviderId: amica-mutual-insurance\npublisherName: Amica Mutual Insurance Company\nserviceCategory: Insurance\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Insurance\n  - Auto Insurance\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Amica Mutual Insurance. Amica has no\n  public API metered billing surface; consumer spend is in the form of\n  insurance premiums, which are state-regulated rather than priced as API\n  consumption.\nnotes: >-\n  No public API billing surface. Premiums are not an API charge category.\nsources:\n  - https://www.amica.com\nbillingModel:\n\
  \  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Amica Mutual Insurance\n  ServiceCategory: Insurance\n  ProviderName: Amica Mutual Insurance\n  PublisherName: Amica Mutual Insurance Company\n  InvoiceIssuerName: Amica Mutual Insurance Company\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: Placeholder; not billed as a developer line item\n    unit: request\n    aggregation: sum\n    dimensions:\n      - consumer\nprinciples:\n  - name: Visibility\n    description: >-\n      No Amica-issued developer telemetry. Premium and claims spend visibility\n      sits in policyholder accounts.\n  - name: Allocation\n    description: >-\n      Allocate premium spend to the household / policy, not by API consumer.\n  - name: Optimization\n    description: >-\n      Optimization levers are policy bundling and dividends, not API tuning.\n  - name: Accountability\n\
  \    description: >-\n      Budget ownership sits with the policyholder; FinOps developer practice is\n      not applicable.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amica-mutual-insurance/refs/heads/main/finops/amica-mutual-insurance-finops.yml
sources:
- https://www.amica.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Insurance
- Auto Insurance
---
