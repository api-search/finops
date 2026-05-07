---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: waste-management-customer-api-openapi.yml
  format: yaml
  label: Waste Management Customer API
  slug: waste-management-customer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/waste-management/refs/heads/main/openapi/waste-management-customer-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Service Contract
description: FinOps view of Waste Management (WM) at the corporate level. WM does not bill API consumption directly; the API surface (account, services, invoices, pickups, ETAs) is a read interface to the existing service contract whose costs are environmental-service charges, not API line items.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Waste Management, Inc.
  ProviderName: Waste Management
  PublisherName: WM Intellectual Property Holdings, L.L.C.
  ServiceCategory: Environmental / Waste Services
  ServiceName: Waste Management Services
layout: finops
meters:
- aggregation: sum
  description: Scheduled waste / recycling pickup events delivered under the WM customer service agreement (the API exposes these events but does not bill them per call).
  dimensions:
  - account
  - service_type
  name: service_pickup
  unit: pickup
- aggregation: sum
  description: Ad-hoc on-call pickups, container swaps, and contamination surcharges added to the monthly invoice.
  dimensions:
  - account
  - charge_type
  name: extra_service
  unit: event
name: Waste Management Finops
provider_name: Waste Management
provider_slug: waste-management
publisher_name: WM Intellectual Property Holdings, L.L.C.
service_category: Environmental / Waste Services
slug: waste-management-finops
source_filename: waste-management-finops.yml
source_heading: FinOps Profile
source_url: https://www.wm.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Waste Management\nproviderId: waste-management\npublisherName: WM Intellectual Property Holdings, L.L.C.\nserviceCategory: Environmental / Waste Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Waste Management\n  - Environmental Services\n  - FinOps\n  - FOCUS\ndescription: FinOps view of Waste Management (WM) at the corporate level. WM\n  does not bill API consumption directly; the API surface (account, services,\n  invoices, pickups, ETAs) is a read interface to the existing service\n  contract whose costs are environmental-service charges, not API line items.\nsources:\n  - https://www.wm.com\nnotes: No metered API invoice; FOCUS attribution maps\
  \ onto the underlying WM\n  service contract.\nbillingModel:\n  pricingCategory: Service Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Waste Management Services\n  ServiceCategory: Environmental / Waste Services\n  ProviderName: Waste Management\n  PublisherName: WM Intellectual Property Holdings, L.L.C.\n  InvoiceIssuerName: Waste Management, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: service_pickup\n    description: Scheduled waste / recycling pickup events delivered under\n      the WM customer service agreement (the API exposes these events but\n      does not bill them per call).\n    unit: pickup\n    aggregation: sum\n    dimensions:\n      - account\n      - service_type\n  - name: extra_service\n    description: Ad-hoc on-call pickups, container swaps, and contamination\n      surcharges added to the monthly invoice.\n    unit: event\n\
  \    aggregation: sum\n    dimensions:\n      - account\n      - charge_type\nprinciples:\n  - name: Visibility\n    description: Use the WM Account / Services / Invoices APIs to pull\n      monthly service consumption and invoice line items; reconcile API-\n      reported events against the customer-portal invoice view.\n  - name: Allocation\n    description: Allocate environmental-service spend to site / property /\n      cost-center using the WM account-id dimension; tag containers and\n      pickup schedules to map them to the consuming team.\n  - name: Optimization\n    description: Use Pickup Schedules and ETAs to right-size pickup cadence\n      and container count; reduce contamination surcharges by improving\n      stream sorting at the source.\n  - name: Accountability\n    description: Facilities / property-management owns the WM contract and\n      per-site allocation; engineering owns API-key / JWT hygiene for the\n      portal integration.\nmaintainers:\n  - FN: Kin Lane\n\
  \    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/waste-management/refs/heads/main/finops/waste-management-finops.yml
sources:
- https://www.wm.com
specification: FinOps Framework
tags:
- Waste Management
- Environmental Services
- FinOps
- FOCUS
---
