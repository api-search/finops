---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: signal-server-openapi.yml
  format: yaml
  label: Signal Server
  slug: signal-server
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/signal/refs/heads/main/openapi/signal-server-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories: []
  pricingCategory: Donation-Funded / Non-Commercial
description: FOCUS-aligned FinOps placeholder for Signal. Signal is a donation-funded non-profit; there is no commercial API, no invoice issued to consumers of the service, and no FOCUS data export. This artifact is included for catalog completeness only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Signal Foundation
  ProviderName: Signal
  PublisherName: Signal Messenger, LLC
  ServiceCategory: Messaging (Non-Commercial)
  ServiceName: Signal
layout: finops
meters:
- aggregation: sum
  description: Signal does not bill consumers and emits no usage meter for FinOps purposes.
  name: not_applicable
  unit: varies
name: Signal Finops
provider_name: Signal
provider_slug: signal
publisher_name: Signal Messenger, LLC / Signal Foundation
service_category: Messaging (Non-Commercial)
slug: signal-finops
source_filename: signal-finops.yml
source_heading: FinOps Profile
source_url: https://www.signal.org/donate/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Signal\nproviderId: signal\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Messaging\n  - Privacy\n  - Open Source\n  - Non-Profit\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Signal. Signal is a donation-funded non-profit;\n  there is no commercial API, no invoice issued to consumers of the service, and no FOCUS data export.\n  This artifact is included for catalog completeness only.\nsources:\n  - https://www.signal.org/donate/\nnotes: Signal is non-commercial. No billing model, FOCUS columns, or meters apply; this artifact\n  exists solely so consumers understand the absence of a billable surface.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Signal Messenger, LLC / Signal Foundation\nserviceCategory: Messaging (Non-Commercial)\nbillingModel:\n  pricingCategory: Donation-Funded / Non-Commercial\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Signal\n  ServiceCategory: Messaging (Non-Commercial)\n  ProviderName: Signal\n  PublisherName: Signal Messenger, LLC\n  InvoiceIssuerName: Signal Foundation\n  BillingCurrency: USD\nmeters:\n  - name: not_applicable\n    description: Signal does not bill consumers and emits no usage meter for FinOps purposes.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: There is no consumer-facing spend on Signal; visibility is limited to optional donations\n      that an organization may make to the Signal Foundation.\n  - name: Allocation\n    description: Donations may be allocated to the philanthropy/community-investment cost center if\n      a company chooses to support Signal.\n\
  \  - name: Optimization\n    description: Not applicable — there is no usage cost to optimize.\n  - name: Accountability\n    description: If donating, the giving entity (foundation, philanthropy, or executive sponsor) owns\n      the donation decision; engineering does not own a spend line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/signal/refs/heads/main/finops/signal-finops.yml
sources:
- https://www.signal.org/donate/
specification: FinOps Framework
tags:
- Messaging
- Privacy
- Open Source
- Non-Profit
- FinOps
- FOCUS
---
