---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: scout-rfp-events-openapi.yml
  format: yaml
  label: Workday Strategic Sourcing API
  slug: workday-strategic-sourcing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scout-rfp/refs/heads/main/openapi/scout-rfp-events-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps shape for Scout RFP / Workday Strategic Sourcing — a quote-based enterprise SaaS subscription billed through Workday's master agreement. No public usage-meter pricing exists; cost allocation is driven by the negotiated subscription line.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: Procurement / Sourcing SaaS
  ServiceName: Workday Strategic Sourcing
layout: finops
meters:
- aggregation: sum
  description: Negotiated enterprise subscription line item billed via Workday master agreement
  name: enterprise_subscription
  unit: varies
name: Scout Rfp Finops
provider_name: Scout RFP
provider_slug: scout-rfp
publisher_name: Workday, Inc.
service_category: Procurement / Sourcing SaaS
slug: scout-rfp-finops
source_filename: scout-rfp-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/products/spend-management/strategic-sourcing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Scout RFP\nproviderId: scout-rfp\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Procurement\n  - Sourcing\n  - RFP\n  - Workday\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Scout RFP / Workday Strategic Sourcing — a quote-based enterprise SaaS subscription\n  billed through Workday's master agreement. No public usage-meter pricing exists; cost allocation is\n  driven by the negotiated subscription line.\nsources:\n  - https://www.workday.com/en-us/products/spend-management/strategic-sourcing.html\nnotes: Scout RFP is sold as part of a Workday enterprise contract. Public meters, FOCUS column mappings,\n  and cost levers were not reconcilable from open documentation.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday, Inc.\nserviceCategory: Procurement / Sourcing SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Strategic Sourcing\n  ServiceCategory: Procurement / Sourcing SaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: enterprise_subscription\n    description: Negotiated enterprise subscription line item billed via Workday master agreement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility is limited to the Workday subscription invoice and any internal allocation\n      Workday admins do via the customer's own ERP. Scout RFP itself does not expose a consumption API.\n  - name: Allocation\n    description: Allocate the subscription to the procurement\
  \ / sourcing cost center; show-back to business\n      units that run the most events / RFPs based on internal Scout activity reports.\n  - name: Optimization\n    description: Optimization happens at contract negotiation and module bundling time, not by tuning\n      API usage. Track adoption (events run, suppliers engaged) to justify the subscription.\n  - name: Accountability\n    description: Procurement / Sourcing leadership owns the Scout RFP line. Workday CSM is the escalation\n      point for entitlement questions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scout-rfp/refs/heads/main/finops/scout-rfp-finops.yml
sources:
- https://www.workday.com/en-us/products/spend-management/strategic-sourcing.html
specification: FinOps Framework
tags:
- Procurement
- Sourcing
- RFP
- Workday
- FinOps
- FOCUS
---
