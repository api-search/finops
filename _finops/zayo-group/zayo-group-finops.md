---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Contact Sales
description: 'Zayo Group''s commercial model is a sales-negotiated carrier contract; this

  artifact is a Contact Sales placeholder pending the customer''s master service

  agreement.

  '
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Zayo Group, LLC
  ProviderName: Zayo Group
  PublisherName: Zayo Group, LLC
  ServiceCategory: Network Connectivity
  ServiceName: Zayo Group
layout: finops
meters:
- aggregation: count
  description: Active circuits / wavelengths / dark fiber strands under contract; the typical primary line item on Zayo invoices.
  dimensions:
  - circuit_id
  - service_type
  - route
  name: circuits
  unit: circuit-month
- aggregation: max
  description: Committed and burstable bandwidth on Ethernet / IP / dedicated internet services.
  dimensions:
  - circuit_id
  - service_type
  name: bandwidth
  unit: Mbps
name: Zayo Group Finops
provider_name: Zayo Group Holdings
provider_slug: zayo-group
publisher_name: Zayo Group, LLC
service_category: Network Connectivity
slug: zayo-group-finops
source_filename: zayo-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.zayo.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Zayo Group Holdings\nproviderId: zayo-group\npublisherName: Zayo Group, LLC\nserviceCategory: Network Connectivity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Fiber\n  - Network\n  - Telecom\n  - FinOps\n  - FOCUS\ndescription: |\n  Zayo Group's commercial model is a sales-negotiated carrier contract; this\n  artifact is a Contact Sales placeholder pending the customer's master service\n  agreement.\nsources:\n  - https://www.zayo.com/products/\nnotes: |\n  Zayo does not publish per-meter pricing publicly. Meter and FOCUS column values\n  below are minimal placeholders pending the signed Zayo MSA / service order.\n\
  billingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Zayo Group\n  ServiceCategory: Network Connectivity\n  ProviderName: Zayo Group\n  PublisherName: Zayo Group, LLC\n  InvoiceIssuerName: Zayo Group, LLC\n  BillingCurrency: USD\nmeters:\n  - name: circuits\n    description: Active circuits / wavelengths / dark fiber strands under contract; the\n      typical primary line item on Zayo invoices.\n    unit: circuit-month\n    aggregation: count\n    dimensions:\n      - circuit_id\n      - service_type\n      - route\n  - name: bandwidth\n    description: Committed and burstable bandwidth on Ethernet / IP / dedicated internet\n      services.\n    unit: Mbps\n    aggregation: max\n    dimensions:\n      - circuit_id\n      - service_type\nprinciples:\n  - name: Visibility\n    description: Visibility comes from monthly Tranzact / customer-portal invoices and\n\
  \      service inventory; Zayo does not expose a public usage API.\n  - name: Allocation\n    description: Allocate spend by circuit ID, route (A-Z endpoints), and consuming\n      business unit / data center.\n  - name: Optimization\n    description: Optimize via term length (1 / 3 / 5 year), grooming under-utilized\n      circuits, and consolidating redundant routes during contract renewal.\n  - name: Accountability\n    description: Spend ownership sits with the network / infrastructure lead who signs\n      the Zayo MSA and individual service orders.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zayo-group/refs/heads/main/finops/zayo-group-finops.yml
sources:
- https://www.zayo.com/products/
specification: FinOps Framework
tags:
- Fiber
- Network
- Telecom
- FinOps
- FOCUS
---
