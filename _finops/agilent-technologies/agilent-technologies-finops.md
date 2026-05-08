---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: agilent-ilab-operations-api.yaml
  format: yaml
  label: Agilent iLab Operations API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/agilent-technologies/refs/heads/main/openapi/agilent-ilab-operations-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Custom Contract / License
description: FOCUS-aligned FinOps shape for Agilent's lab software portfolio. Pricing is custom (per-product contract or instrument-bundled) rather than a public usage-based rate card; FinOps focus is allocating spend by lab / instrument / facility and tying it to scientific throughput.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Agilent Technologies, Inc.
  ProviderName: Agilent Technologies
  PublisherName: Agilent Technologies, Inc.
  ServiceCategory: Life Sciences / Lab Software
  ServiceName: Agilent Lab Software Portfolio
layout: finops
meters:
- aggregation: sum
  description: iLab Operations Software subscription (typically per facility / per institution)
  dimensions:
  - facility
  - module
  name: ilab_subscription
  unit: subscription-month
- aggregation: sum
  description: SLIMS LIMS license (per seat or per environment)
  dimensions:
  - seat
  - environment
  name: slims_license
  unit: license-month
- aggregation: sum
  description: CrossLab service contract covering instrument maintenance and asset management
  dimensions:
  - instrument
  - service_tier
  name: crosslab_service_contract
  unit: contract-month
- aggregation: sum
  description: VWorks lab-automation software license per workstation
  dimensions:
  - workstation
  name: vworks_license
  unit: license-month
- aggregation: sum
  description: API requests against any Agilent product API (customer-side telemetry only)
  dimensions:
  - api
  - tier
  name: api_requests
  unit: request
name: Agilent Technologies Finops
provider_name: agilent-technologies
provider_slug: agilent-technologies
publisher_name: Agilent Technologies, Inc.
service_category: Life Sciences / Lab Software
slug: agilent-technologies-finops
source_filename: agilent-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.agilent.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Agilent Technologies\nproviderId: agilent-technologies\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Agilent Technologies, Inc.\nserviceCategory: Life Sciences / Lab Software\ntags:\n  - Life Sciences\n  - Diagnostics\n  - Laboratory\n  - LIMS\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Agilent's lab software portfolio. Pricing is custom (per-product\n  contract or instrument-bundled) rather than a public usage-based rate card; FinOps focus is allocating\n  spend by lab / instrument / facility and tying it to scientific throughput.\nnotes: No public pricing; meters reflect the contract dimensions\
  \ Agilent typically uses (instruments,\n  seats, samples) plus API request volume customers can self-track.\nsources:\n  - https://www.agilent.com/\nbillingModel:\n  pricingCategory: Custom Contract / License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Agilent Lab Software Portfolio\n  ServiceCategory: Life Sciences / Lab Software\n  ProviderName: Agilent Technologies\n  PublisherName: Agilent Technologies, Inc.\n  InvoiceIssuerName: Agilent Technologies, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: ilab_subscription\n    description: iLab Operations Software subscription (typically per facility / per institution)\n    unit: subscription-month\n    aggregation: sum\n    dimensions:\n      - facility\n      - module\n  - name: slims_license\n    description: SLIMS LIMS license (per seat or per environment)\n    unit: license-month\n    aggregation: sum\n    dimensions:\n\
  \      - seat\n      - environment\n  - name: crosslab_service_contract\n    description: CrossLab service contract covering instrument maintenance and asset management\n    unit: contract-month\n    aggregation: sum\n    dimensions:\n      - instrument\n      - service_tier\n  - name: vworks_license\n    description: VWorks lab-automation software license per workstation\n    unit: license-month\n    aggregation: sum\n    dimensions:\n      - workstation\n  - name: api_requests\n    description: API requests against any Agilent product API (customer-side telemetry only)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tier\nprinciples:\n  - name: Visibility\n    description: Track Agilent costs from product invoices and CrossLab service-contract statements; for\n      API request visibility, instrument it client-side since Agilent does not expose a unified usage API.\n  - name: Allocation\n    description: Allocate by instrument serial number, facility,\
  \ and lab / cost center — these are the\n      same dimensions Agilent uses to scope contracts.\n  - name: Optimization\n    description: Optimize by right-sizing iLab seat counts, retiring unused SLIMS environments, and\n      negotiating CrossLab tiers to match instrument criticality (response-time SLAs vs basic coverage).\n  - name: Accountability\n    description: Lab operations / core-facility leadership owns Agilent spend; align reviews with the\n      annual CrossLab and SLIMS renewal cycles and instrument capital cycles.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/agilent-technologies/refs/heads/main/finops/agilent-technologies-finops.yml
sources:
- https://www.agilent.com/
specification: FinOps Framework
tags:
- Life Sciences
- Diagnostics
- Laboratory
- LIMS
- FinOps
- FOCUS
---
