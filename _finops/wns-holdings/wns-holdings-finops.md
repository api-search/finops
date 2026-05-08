---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Custom
description: FOCUS-aligned FinOps stub for WNS (Holdings) Ltd. WNS sells custom outsourcing and analytics engagements rather than a metered API; this artifact captures only the contractual shape and leaves quantitative meters undefined since no public billing surface exists.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: WNS (Holdings) Ltd.
  ProviderName: WNS Holdings
  PublisherName: WNS (Holdings) Ltd.
  ServiceCategory: Business Process Outsourcing
  ServiceName: WNS Engagement
layout: finops
meters:
- aggregation: sum
  description: Negotiated outsourcing engagement; pricing, volume, and unit of measure are defined in the master services agreement.
  dimensions:
  - engagement
  - business_unit
  name: contracted_engagement
  unit: varies
name: Wns Holdings Finops
provider_name: WNS Holdings
provider_slug: wns-holdings
publisher_name: WNS (Holdings) Ltd.
service_category: Business Process Outsourcing
slug: wns-holdings-finops
source_filename: wns-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.wns.com/contact-us
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: WNS Holdings\nproviderId: wns-holdings\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Business Process Outsourcing\n  - Analytics\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for WNS (Holdings) Ltd. WNS sells custom outsourcing and analytics engagements rather than a metered API; this artifact captures only the contractual shape and leaves quantitative meters undefined since no public billing surface exists.\nsources:\n  - https://www.wns.com/contact-us\nnotes: No public pricing or usage telemetry. Generic per-request, GB-egress, and compute-second meters from the scaffold have been removed; a single contractual meter is kept so consumers see WNS is governed by master services agreements rather than metered self-service.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: WNS (Holdings) Ltd.\nserviceCategory: Business Process Outsourcing\nbillingModel:\n  pricingCategory: Contract / Custom\n  billingFrequency: Per-Invoice\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: WNS Engagement\n  ServiceCategory: Business Process Outsourcing\n  ProviderName: WNS Holdings\n  PublisherName: WNS (Holdings) Ltd.\n  InvoiceIssuerName: WNS (Holdings) Ltd.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_engagement\n    description: Negotiated outsourcing engagement; pricing, volume, and unit of measure are defined in the master services agreement.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - engagement\n      - business_unit\nprinciples:\n  - name: Visibility\n    description: Visibility is delivered through WNS-issued operational reports, dashboards, and\
  \ quarterly business reviews tied to the engagement; there is no self-serve usage API to reconcile against.\n  - name: Allocation\n    description: Allocate WNS spend at the engagement / SOW level using internal cost-center tagging; line items map to the deliverables defined in the contract rather than to API calls.\n  - name: Optimization\n    description: Optimize via SOW renegotiation, scope adjustment, automation work delivered by WNS (e.g., RPA, analytics), and consolidation of overlapping engagements rather than via runtime knobs.\n  - name: Accountability\n    description: Accountability sits with the contract owner (typically procurement plus a business sponsor) who reviews invoices against the SOW and renews or restructures the engagement on contract milestones.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wns-holdings/refs/heads/main/finops/wns-holdings-finops.yml
sources:
- https://www.wns.com/contact-us
specification: FinOps Framework
tags:
- Business Process Outsourcing
- Analytics
- FinOps
- FOCUS
---
