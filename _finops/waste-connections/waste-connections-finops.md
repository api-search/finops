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
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Service Contract
description: FinOps view of Waste Connections at the corporate level. Waste Connections does not bill API consumption; what flows on its invoices is scheduled service (collection, disposal, recycling) priced under the bilateral service contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Waste Connections, Inc.
  ProviderName: Waste Connections
  PublisherName: Waste Connections, Inc.
  ServiceCategory: Environmental / Waste Services
  ServiceName: Waste Connections Services
layout: finops
meters:
- aggregation: sum
  description: Scheduled waste / recycling pickup events delivered under the customer service agreement (out-of-scope for software FinOps; included to give the FOCUS row a unit of measure).
  dimensions:
  - account
  - service_type
  name: service_pickup
  unit: pickup
name: Waste Connections Finops
provider_name: Waste Connections
provider_slug: waste-connections
publisher_name: Waste Connections, Inc.
service_category: Environmental / Waste Services
slug: waste-connections-finops
source_filename: waste-connections-finops.yml
source_heading: FinOps Profile
source_url: https://www.wasteconnections.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Waste Connections\nproviderId: waste-connections\npublisherName: Waste Connections, Inc.\nserviceCategory: Environmental / Waste Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Waste Management\n  - Environmental Services\n  - FinOps\n  - FOCUS\ndescription: FinOps view of Waste Connections at the corporate level. Waste\n  Connections does not bill API consumption; what flows on its invoices is\n  scheduled service (collection, disposal, recycling) priced under the\n  bilateral service contract.\nsources:\n  - https://www.wasteconnections.com/\nnotes: No API invoice surface. FOCUS attribution maps onto the bilateral\n  service contract, not a metered\
  \ API line.\nbillingModel:\n  pricingCategory: Service Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Waste Connections Services\n  ServiceCategory: Environmental / Waste Services\n  ProviderName: Waste Connections\n  PublisherName: Waste Connections, Inc.\n  InvoiceIssuerName: Waste Connections, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: service_pickup\n    description: Scheduled waste / recycling pickup events delivered under\n      the customer service agreement (out-of-scope for software FinOps;\n      included to give the FOCUS row a unit of measure).\n    unit: pickup\n    aggregation: sum\n    dimensions:\n      - account\n      - service_type\nprinciples:\n  - name: Visibility\n    description: Track service-line usage via the Waste Connections\n      customer portal; reconcile against the monthly invoice.\n  - name: Allocation\n    description:\
  \ Allocate environmental-service spend to the consuming\n      site / property / cost-center based on the service account.\n  - name: Optimization\n    description: Optimize collection cadence, dumpster sizing, and\n      recycling-stream contamination to reduce monthly service charges.\n  - name: Accountability\n    description: Facilities / property-management owns the service\n      contract and per-site allocation.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/waste-connections/refs/heads/main/finops/waste-connections-finops.yml
sources:
- https://www.wasteconnections.com/
specification: FinOps Framework
tags:
- Waste Management
- Environmental Services
- FinOps
- FOCUS
---
