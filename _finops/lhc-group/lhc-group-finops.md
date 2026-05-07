---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps scaffold for LHC Group: partner-only healthcare API access with no public per-call pricing. Consumer-side spend tracks against the partner / BAA contract rather than metered LHC Group invoices.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: LHC Group, Inc.
  ProviderName: LHC Group
  PublisherName: LHC Group, Inc.
  ServiceCategory: Healthcare / API
  ServiceName: LHC Group API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - environment
  - partner
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - contract
  name: partner_fees
  unit: month
name: Lhc Group Finops
provider_name: LHC Group
provider_slug: lhc-group
publisher_name: LHC Group, Inc.
service_category: Healthcare / API
slug: lhc-group-finops
source_filename: lhc-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.lhcgroup.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LHC Group\nproviderId: lhc-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Home Health\n  - Hospice\n  - Healthcare\ndescription: 'FOCUS-aligned FinOps scaffold for LHC Group: partner-only healthcare API access with no\n  public per-call pricing. Consumer-side spend tracks against the partner / BAA contract rather than\n  metered LHC Group invoices.'\nnotes: Pricing is contract-driven. Meters describe the consumer-side telemetry shape; reconcile against\n  the executed partner / BAA agreement.\nsources:\n  - https://www.lhcgroup.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: LHC Group, Inc.\nserviceCategory: Healthcare\
  \ / API\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: LHC Group API\n  ServiceCategory: Healthcare / API\n  ProviderName: LHC Group\n  PublisherName: LHC Group, Inc.\n  InvoiceIssuerName: LHC Group, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - environment\n      - partner\n  - name: partner_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Track outbound API call volume and any referral / interop event volume in your own gateway\n      / observability stack; LHC Group does not expose a public usage API.\n  - name: Allocation\n    description: Tag calls by service line (home health, hospice, referrals) and by consuming application\n      so partner-contract\
  \ spend can be charged back.\n  - name: Optimization\n    description: Batch referral and authorization checks; cache static facility / clinician reference\n      data to stay within contracted volumes.\n  - name: Accountability\n    description: Assign a contract owner per LHC Group / Optum partner agreement and review monthly against\n      contracted volume and PHI handling controls.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lhc-group/refs/heads/main/finops/lhc-group-finops.yml
sources:
- https://www.lhcgroup.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Home Health
- Hospice
- Healthcare
---
