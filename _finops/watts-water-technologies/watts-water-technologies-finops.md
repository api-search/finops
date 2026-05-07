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
  - Purchase
  pricingCategory: Enterprise / Channel Agreement
description: FinOps placement for Watts Water Technologies. Spend is realized through hardware purchases and partner / OEM software agreements rather than a metered API surface; FOCUS mapping is limited until a billable API is published.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Watts Water Technologies, Inc.
  ProviderName: Watts Water Technologies
  PublisherName: Watts Water Technologies, Inc.
  ServiceCategory: Industrial / Water
  ServiceName: Watts Water Technologies
layout: finops
meters:
- aggregation: sum
  description: Negotiated OEM / channel / BMS-integration fees with Watts; not metered per call.
  name: contract_fees
  unit: varies
name: Watts Water Technologies Finops
provider_name: Watts Water Technologies
provider_slug: watts-water-technologies
publisher_name: Watts Water Technologies, Inc.
service_category: Industrial / Water
slug: watts-water-technologies-finops
source_filename: watts-water-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.watts.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Watts Water Technologies\nproviderId: watts-water-technologies\npublisherName: Watts Water Technologies, Inc.\nserviceCategory: Industrial / Water\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Water\n  - Industrial\n  - Infrastructure\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps placement for Watts Water Technologies. Spend is realized through hardware purchases\n  and partner / OEM software agreements rather than a metered API surface; FOCUS mapping is limited\n  until a billable API is published.\nnotes: No public usage-billing API published; meters and FOCUS columns reflect the contract-billing\
  \ shape.\nsources:\n  - https://www.watts.com/\nbillingModel:\n  pricingCategory: Enterprise / Channel Agreement\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Watts Water Technologies\n  ServiceCategory: Industrial / Water\n  ProviderName: Watts Water Technologies\n  PublisherName: Watts Water Technologies, Inc.\n  InvoiceIssuerName: Watts Water Technologies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    description: Negotiated OEM / channel / BMS-integration fees with Watts; not metered per call.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility is sourced from procurement, hardware POs, and the executed integration\n      contract; no public usage telemetry API exists.\n  - name: Allocation\n    description: Allocate Watts spend by site, building, or BMS instance using internal asset-tracking\n      tags on hardware and integration\
  \ deployments.\n  - name: Optimization\n    description: Cost levers are negotiated at contract / RFP stage — bundle scope, regional volume,\n      multi-year commitments — not at per-request granularity.\n  - name: Accountability\n    description: Facilities engineering or building-controls teams typically own the relationship and\n      coordinate renewals with Watts account management.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/watts-water-technologies/refs/heads/main/finops/watts-water-technologies-finops.yml
sources:
- https://www.watts.com/
specification: FinOps Framework
tags:
- Water
- Industrial
- Infrastructure
- FinOps
- FOCUS
- Contact Sales
---
