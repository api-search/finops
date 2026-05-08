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
  - Adjustment
  pricingCategory: Enterprise / Negotiated
description: FOCUS-aligned FinOps scaffold for the John Deere developer program. Treated as a negotiated-enterprise relationship; no public usage-billing telemetry is exposed.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Deere & Company
  ProviderName: John Deere
  PublisherName: Deere & Company
  ServiceCategory: Agriculture / Equipment Telemetry
  ServiceName: John Deere Developer APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - application
  - api
  - organization
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - organization
  - machine
  name: machine_telemetry_events
  unit: event
- aggregation: count
  dimensions:
  - organization
  - operation
  name: file_transfers
  unit: file
name: John Deere Finops
provider_name: John Deere
provider_slug: john-deere
publisher_name: Deere & Company
service_category: Agriculture / Equipment Telemetry
slug: john-deere-finops
source_filename: john-deere-finops.yml
source_heading: FinOps Profile
source_url: https://developer.deere.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: John Deere\nproviderId: john-deere\npublisherName: Deere & Company\nserviceCategory: Agriculture / Equipment Telemetry\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: John Deere does not publish public pricing or a usage/billing API for its developer\n  program. FinOps shape is inferred from the partner-program model (negotiated contract).\n  Meters listed are placeholders aligned to the kinds of usage the Operations Center API\n  exposes (machine telemetry events, field operation files, equipment inventory reads).\ntags:\n  - Agriculture\n  - Equipment\n  - Machinery\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps\
  \ scaffold for the John Deere developer program. Treated as\n  a negotiated-enterprise relationship; no public usage-billing telemetry is exposed.\nsources:\n  - https://developer.deere.com/\n  - https://www.finops.org/framework/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: John Deere Developer APIs\n  ServiceCategory: Agriculture / Equipment Telemetry\n  ProviderName: John Deere\n  PublisherName: Deere & Company\n  InvoiceIssuerName: Deere & Company\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - application\n      - api\n      - organization\n  - name: machine_telemetry_events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - organization\n      - machine\n  - name: file_transfers\n \
  \   unit: file\n    aggregation: count\n    dimensions:\n      - organization\n      - operation\nprinciples:\n  - name: Visibility\n    description: Track per-application API call volume against the limits provisioned during\n      developer-program onboarding; there is no first-party usage-billing API to ingest.\n  - name: Allocation\n    description: Allocate usage by application_id and organization (dealer / customer account)\n      since John Deere scopes API access by partner application and authorized organization.\n  - name: Optimization\n    description: Reduce machine-telemetry polling cost by subscribing to Operations Center\n      webhooks where available and caching equipment / field metadata that changes infrequently.\n  - name: Accountability\n    description: A named partner-program contact at John Deere is the escalation path for\n      limit raises and contract review; pair with an internal API-product owner.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/john-deere/refs/heads/main/finops/john-deere-finops.yml
sources:
- https://developer.deere.com/
- https://www.finops.org/framework/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Agriculture
- Equipment
- Machinery
- FinOps
- FOCUS
---
