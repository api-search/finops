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
  - Usage
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Bundled into Laboratory Services Agreement
description: 'FOCUS-aligned FinOps for Labcorp (under its full legal name Laboratory Corporation of America Holdings): API integrations are bundled inside the broader laboratory-services or biopharma master agreement, so FinOps signal at the integration layer comes from message and transaction volume that the consumer measures internally and reconciles against laboratory-services invoices.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Laboratory Corporation of America Holdings
  ProviderName: Laboratory Corporation of America (Labcorp)
  PublisherName: Laboratory Corporation of America Holdings
  ServiceCategory: Healthcare / Diagnostics
  ServiceName: Labcorp Connectivity
layout: finops
meters:
- aggregation: sum
  dimensions:
  - message_type
  - facility
  name: hl7_messages
  unit: message
- aggregation: sum
  dimensions:
  - resource_type
  - facility
  name: fhir_requests
  unit: request
- aggregation: sum
  dimensions:
  - facility
  - test_panel
  name: lab_orders
  unit: order
- aggregation: sum
  dimensions:
  - facility
  - test_panel
  name: lab_results
  unit: result
name: Laboratory Corp Of America Finops
provider_name: Laboratory Corporation of America (Labcorp)
provider_slug: laboratory-corp-of-america
publisher_name: Laboratory Corporation of America Holdings
service_category: Healthcare / Diagnostics
slug: laboratory-corp-of-america-finops
source_filename: laboratory-corp-of-america-finops.yml
source_heading: FinOps Profile
source_url: https://www.labcorp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Laboratory Corporation of America (Labcorp)\nproviderId: laboratory-corp-of-america\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Healthcare\n  - FHIR\n  - Diagnostics\n  - Alias\ndescription: 'FOCUS-aligned FinOps for Labcorp (under its full legal name Laboratory Corporation of\n  America Holdings): API integrations are bundled inside the broader laboratory-services or biopharma\n  master agreement, so FinOps signal at the integration layer comes from message and transaction volume\n  that the consumer measures internally and reconciles against laboratory-services invoices.'\nsources:\n  - https://www.labcorp.com/\nnotes: Alias of the labcorp FinOps record. No public unit pricing for the API surface itself; cost is\n  bundled in the laboratory-services agreement.\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Laboratory Corporation of America Holdings\nserviceCategory: Healthcare / Diagnostics\nbillingModel:\n  pricingCategory: Bundled into Laboratory Services Agreement\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Labcorp Connectivity\n  ServiceCategory: Healthcare / Diagnostics\n  ProviderName: Laboratory Corporation of America (Labcorp)\n  PublisherName: Laboratory Corporation of America Holdings\n  InvoiceIssuerName: Laboratory Corporation of America Holdings\n  BillingCurrency: USD\nmeters:\n  - name: hl7_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - message_type\n      - facility\n  - name: fhir_requests\n    unit: request\n    aggregation: sum\n\
  \    dimensions:\n      - resource_type\n      - facility\n  - name: lab_orders\n    unit: order\n    aggregation: sum\n    dimensions:\n      - facility\n      - test_panel\n  - name: lab_results\n    unit: result\n    aggregation: sum\n    dimensions:\n      - facility\n      - test_panel\nprinciples:\n  - name: Visibility\n    description: Capture HL7 v2 message and FHIR request counts at the interface engine; correlate volumes\n      with the laboratory-services invoice line items.\n  - name: Allocation\n    description: Tag traffic with originating facility, ordering provider, and program (e.g. employee\n      health, hospital outpatient) to support internal cost allocation against the Labcorp agreement.\n  - name: Optimization\n    description: Use standing orders and reflex testing rules to reduce duplicate orders; consolidate\n      panels; route low-acuity orders to lower-cost test menus.\n  - name: Accountability\n    description: Health-system informatics and revenue-cycle teams\
  \ jointly own integration cost; review\n      Labcorp invoices against measured order/result counts monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/laboratory-corp-of-america/refs/heads/main/finops/laboratory-corp-of-america-finops.yml
sources:
- https://www.labcorp.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Healthcare
- FHIR
- Diagnostics
- Alias
---
