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
  pricingCategory: Enterprise License
description: FinOps placement for Waters Corporation laboratory-informatics and analytical-instrument software. Spend is governed by enterprise license + professional services contracts rather than metered API usage; FOCUS mapping is limited until a billable API surface is published.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Waters Corporation
  ProviderName: Waters Corporation
  PublisherName: Waters Corporation
  ServiceCategory: Laboratory Informatics
  ServiceName: Waters Corporation
layout: finops
meters:
- aggregation: sum
  description: Negotiated enterprise license for Waters informatics software; not metered per call.
  name: enterprise_license
  unit: varies
name: Waters Finops
provider_name: Waters Corporation
provider_slug: waters
publisher_name: Waters Corporation
service_category: Laboratory Informatics
slug: waters-finops
source_filename: waters-finops.yml
source_heading: FinOps Profile
source_url: https://www.waters.com/nextgen/us/en.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Waters Corporation\nproviderId: waters\npublisherName: Waters Corporation\nserviceCategory: Laboratory Informatics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Laboratory\n  - Instruments\n  - Analytics\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps placement for Waters Corporation laboratory-informatics and analytical-instrument\n  software. Spend is governed by enterprise license + professional services contracts rather than\n  metered API usage; FOCUS mapping is limited until a billable API surface is published.\nnotes: No public usage-billing API or invoice schema published. Meters and FOCUS columns\
  \ reflect the\n  enterprise-license shape only.\nsources:\n  - https://www.waters.com/nextgen/us/en.html\nbillingModel:\n  pricingCategory: Enterprise License\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Waters Corporation\n  ServiceCategory: Laboratory Informatics\n  ProviderName: Waters Corporation\n  PublisherName: Waters Corporation\n  InvoiceIssuerName: Waters Corporation\n  BillingCurrency: USD\nmeters:\n  - name: enterprise_license\n    description: Negotiated enterprise license for Waters informatics software; not metered per call.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility comes from procurement and contract records held with Waters; there\n      is no public usage telemetry API to query.\n  - name: Allocation\n    description: Allocate Waters spend to the lab(s), instrument fleet, and study programs using internal\n      cost-center\
  \ tagging on the purchase order and software license.\n  - name: Optimization\n    description: Optimization levers are negotiated at renewal — license counts, module bundles, and\n      professional-services scope — rather than at per-call granularity.\n  - name: Accountability\n    description: Lab IT, scientific computing, or QC operations typically own Waters software spend and\n      coordinate renewals with Waters account management.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/waters/refs/heads/main/finops/waters-finops.yml
sources:
- https://www.waters.com/nextgen/us/en.html
specification: FinOps Framework
tags:
- Laboratory
- Instruments
- Analytics
- FinOps
- FOCUS
- Contact Sales
---
