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
  pricingCategory: Lease / Partnership Contract
description: FOCUS-aligned FinOps placeholder for Simon Property Group. Simon does not bill API consumption as a discrete line; cost flows through leasing, marketing, and partnership contracts. No public usage telemetry or per-call billing surface exists.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Simon Property Group, L.P.
  ProviderName: Simon Property Group
  PublisherName: Simon Property Group, L.P.
  ServiceCategory: Commercial Real Estate
  ServiceName: Simon Property Group
layout: finops
meters:
- aggregation: sum
  description: Partner cost is governed by the underlying lease or marketing agreement, not by per-API-call meters.
  name: contractual_partnership
  unit: varies
name: Simon Property Group Finops
provider_name: Simon Property Group
provider_slug: simon-property-group
publisher_name: Simon Property Group, L.P.
service_category: Commercial Real Estate
slug: simon-property-group-finops
source_filename: simon-property-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.simon.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Simon Property Group\nproviderId: simon-property-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Commercial Real Estate\n  - REIT\n  - Fortune 500\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Simon Property Group. Simon does not bill API\n  consumption as a discrete line; cost flows through leasing, marketing, and partnership contracts.\n  No public usage telemetry or per-call billing surface exists.\nsources:\n  - https://www.simon.com/\nnotes: No public API billing model. FinOps treatment is contract-driven; reconciliation pending\n  direct partner-channel confirmation.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Simon Property Group, L.P.\nserviceCategory: Commercial Real Estate\nbillingModel:\n  pricingCategory: Lease / Partnership Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Simon Property Group\n  ServiceCategory: Commercial Real Estate\n  ProviderName: Simon Property Group\n  PublisherName: Simon Property Group, L.P.\n  InvoiceIssuerName: Simon Property Group, L.P.\n  BillingCurrency: USD\nmeters:\n  - name: contractual_partnership\n    description: Partner cost is governed by the underlying lease or marketing agreement, not by\n      per-API-call meters.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility comes from the AP/finance system that processes lease and marketing\n      invoices, not from a usage API.\n  - name: Allocation\n    description: Allocate via the originating lease, store, or campaign captured in the partner's\n      financial\
  \ system; tag integration traffic with the contract reference.\n  - name: Optimization\n    description: Optimization is contractual — renegotiate marketing or co-tenancy terms and consolidate\n      duplicate integrations rather than tuning request volume.\n  - name: Accountability\n    description: Real-estate, retail-marketing, and brand teams own the Simon partnership; integration\n      teams own technical SLA conformance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/simon-property-group/refs/heads/main/finops/simon-property-group-finops.yml
sources:
- https://www.simon.com/
specification: FinOps Framework
tags:
- Commercial Real Estate
- REIT
- Fortune 500
- FinOps
- FOCUS
---
