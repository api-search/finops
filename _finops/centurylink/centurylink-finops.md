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
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Usage (Contract)
description: 'FOCUS-aligned FinOps framing for Lumen/CenturyLink: enterprise telecom and network services billed by contract; API access bundled with underlying network, edge, CDN, and security service charges rather than separately metered.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Lumen Technologies, Inc.
  ProviderName: Lumen Technologies
  PublisherName: Lumen Technologies, Inc.
  ServiceCategory: Telecommunications
  ServiceName: Lumen Network Services
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - location
  name: connectivity_circuits
  unit: circuit-month
- aggregation: max
  dimensions:
  - service
  - location
  name: bandwidth_committed
  unit: Mbps-month
- aggregation: sum
  dimensions:
  - region
  name: cdn_traffic
  unit: GB
- aggregation: max
  name: ddos_protected_capacity
  unit: Mbps-month
- aggregation: sum
  name: edge_compute
  unit: instance-hour
name: Centurylink Finops
provider_name: CenturyLink (Lumen Technologies)
provider_slug: centurylink
publisher_name: Lumen Technologies, Inc.
service_category: Telecommunications / Network
slug: centurylink-finops
source_filename: centurylink-finops.yml
source_heading: FinOps Profile
source_url: https://developer.lumen.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CenturyLink (Lumen Technologies)\nproviderId: centurylink\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Telecom\n  - Network\ndescription: 'FOCUS-aligned FinOps framing for Lumen/CenturyLink: enterprise telecom and network services\n  billed by contract; API access bundled with underlying network, edge, CDN, and security service charges\n  rather than separately metered.'\nnotes: API consumption is not separately priced. Meters and FOCUS columns reflect the bundled telecom\n  / network service billing surface.\nsources:\n  - https://developer.lumen.com/\n  - https://apimarketplace.lumen.com/\n  - https://www.lumen.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Lumen Technologies, Inc.\nserviceCategory: Telecommunications / Network\nbillingModel:\n  pricingCategory: Subscription + Usage (Contract)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Lumen Network Services\n  ServiceCategory: Telecommunications\n  ProviderName: Lumen Technologies\n  PublisherName: Lumen Technologies, Inc.\n  InvoiceIssuerName: Lumen Technologies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: connectivity_circuits\n    unit: circuit-month\n    aggregation: sum\n    dimensions:\n      - service\n      - location\n  - name: bandwidth_committed\n    unit: Mbps-month\n    aggregation: max\n    dimensions:\n      - service\n      - location\n  - name: cdn_traffic\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n  - name: ddos_protected_capacity\n    unit: Mbps-month\n    aggregation: max\n  - name: edge_compute\n\
  \    unit: instance-hour\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use the Lumen Control Center and Billing API for invoice and service inventory data;\n      reconcile against contract MRC.\n  - name: Allocation\n    description: Allocate by site / circuit ID / service ID; tag in your CMDB to attribute cost to consuming\n      business units.\n  - name: Optimization\n    description: Right-size committed bandwidth, consolidate circuits at strategic POPs, and exercise\n      contract renewals to renegotiate MRC and term commitments.\n  - name: Accountability\n    description: Network engineering or telecom expense management owns Lumen invoices; review monthly\n      against forecast and outage credits.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/centurylink/refs/heads/main/finops/centurylink-finops.yml
sources:
- https://developer.lumen.com/
- https://apimarketplace.lumen.com/
- https://www.lumen.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Telecom
- Network
---
