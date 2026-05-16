---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: powerbi.json
  format: json
  label: Power BI REST API
  slug: power-bi-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/powerbi/data-plane/Microsoft.PowerBI/stable/v1.0/powerbi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (per-user) and Hourly (capacity)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Capacity (Pay-As-You-Go + Reservation)
description: 'FOCUS-aligned FinOps for Power BI: hybrid model combining per-user subscriptions (Free, Pro $14/user/month, Premium Per User $24/user/month) with hourly Azure capacity (Power BI Embedded A SKUs and Microsoft Fabric F SKUs that host Power BI Premium workloads). Per-user charges land on the Microsoft 365 / commerce invoice; capacity charges land on the Azure invoice and reconcile to FOCUS Pay-As-You-Go + Commitment Discount.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingUnit: seat-month or v-core-hour
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  RegionId: varies (capacity is non-regional; data plane region per tenant)
  ServiceCategory: Analytics
  ServiceName: Power BI
  ServiceSubcategory: Business Intelligence
layout: finops
meters:
- aggregation: max
  description: Power BI Pro per-user subscriptions.
  dimensions:
  - tenant
  - department
  - cost_center
  name: pro_seats
  unit: seat-month
- aggregation: max
  description: Power BI Premium Per User subscriptions.
  dimensions:
  - tenant
  - department
  - cost_center
  name: ppu_seats
  unit: seat-month
- aggregation: sum
  description: Hourly v-core capacity billed for Power BI Embedded (A SKUs).
  dimensions:
  - sku
  - region
  - capacity_id
  name: embedded_capacity_hours
  unit: capacity-hour
- aggregation: sum
  description: Hourly v-core capacity billed for Microsoft Fabric (F SKUs) hosting Power BI Premium workloads.
  dimensions:
  - sku
  - region
  - capacity_id
  - workload
  name: fabric_capacity_hours
  unit: capacity-hour
- aggregation: count
  description: Annual capacity reservation purchase that earns the 40.5% commitment discount over pay-as-you-go.
  dimensions:
  - sku
  - region
  name: capacity_reservation
  unit: reservation-year
- aggregation: max
  description: Storage consumed by datasets, dataflows, and Lakehouse content.
  dimensions:
  - workspace
  - capacity_id
  name: dataset_storage
  unit: GB-month
- aggregation: sum
  description: Scheduled and on-demand dataset refresh operations.
  dimensions:
  - dataset
  - workspace
  name: dataset_refreshes
  unit: refresh
name: Power Bi Finops
provider_name: Power BI
provider_slug: power-bi
publisher_name: Microsoft Corporation
service_category: Analytics
slug: power-bi-finops
source_filename: power-bi-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/power-platform/products/power-bi/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Power BI\nproviderId: power-bi\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Analytics\n  - Business Intelligence\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Power BI: hybrid model combining per-user\n  subscriptions (Free, Pro $14/user/month, Premium Per User $24/user/month)\n  with hourly Azure capacity (Power BI Embedded A SKUs and Microsoft Fabric\n  F SKUs that host Power BI Premium workloads). Per-user charges land on the\n  Microsoft 365 / commerce invoice; capacity charges land on the Azure\n  invoice and reconcile to FOCUS Pay-As-You-Go + Commitment Discount.\nsources:\n  - https://www.microsoft.com/en-us/power-platform/products/power-bi/pricing\n  - https://learn.microsoft.com/en-us/power-bi/developer/embedded/embedded-faq\n  - https://learn.microsoft.com/en-us/rest/api/power-bi/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Analytics\nbillingModel:\n  pricingCategory: Subscription + Capacity (Pay-As-You-Go + Reservation)\n  billingFrequency: Monthly (per-user) and Hourly (capacity)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Power BI\n  ServiceCategory: Analytics\n  ServiceSubcategory: Business Intelligence\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: seat-month or v-core-hour\n  RegionId: varies (capacity is non-regional; data plane region per tenant)\nmeters:\n  - name: pro_seats\n    description: Power\
  \ BI Pro per-user subscriptions.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - tenant\n      - department\n      - cost_center\n  - name: ppu_seats\n    description: Power BI Premium Per User subscriptions.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - tenant\n      - department\n      - cost_center\n  - name: embedded_capacity_hours\n    description: Hourly v-core capacity billed for Power BI Embedded (A SKUs).\n    unit: capacity-hour\n    aggregation: sum\n    dimensions:\n      - sku\n      - region\n      - capacity_id\n  - name: fabric_capacity_hours\n    description: Hourly v-core capacity billed for Microsoft Fabric (F SKUs) hosting Power BI Premium workloads.\n    unit: capacity-hour\n    aggregation: sum\n    dimensions:\n      - sku\n      - region\n      - capacity_id\n      - workload\n  - name: capacity_reservation\n    description: Annual capacity reservation purchase that earns the 40.5% commitment discount over pay-as-you-go.\n\
  \    unit: reservation-year\n    aggregation: count\n    dimensions:\n      - sku\n      - region\n  - name: dataset_storage\n    description: Storage consumed by datasets, dataflows, and Lakehouse content.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - workspace\n      - capacity_id\n  - name: dataset_refreshes\n    description: Scheduled and on-demand dataset refresh operations.\n    unit: refresh\n    aggregation: sum\n    dimensions:\n      - dataset\n      - workspace\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft Fabric Capacity Metrics app and Azure diagnostic logs to track v-core utilization on a 30-second evaluation cycle; per-user license consumption surfaces in the Microsoft 365 admin center and Cost Management exports.\n  - name: Allocation\n    description: Allocate per-user costs by department/cost center via Microsoft Entra group membership; allocate capacity costs by workspace assignment - the utilization report's bar chart visual\
  \ maps directly to chargeback by workspace owner.\n  - name: Optimization\n    description: Pause Embedded A-SKU capacity when not in use to stop hourly billing; choose annual capacity reservation for 40.5% over pay-as-you-go; right-size SKUs using the metrics-app utilization data to avoid interactive request delay.\n  - name: Accountability\n    description: Capacity admins receive utilization-threshold notifications (default 80%) from the Power BI admin portal; Azure Alerts can be configured on the Premium CPU metric; workspace owners are accountable for refresh and dataflow load profiles that drive background utilization.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/power-bi/refs/heads/main/finops/power-bi-finops.yml
sources:
- https://www.microsoft.com/en-us/power-platform/products/power-bi/pricing
- https://learn.microsoft.com/en-us/power-bi/developer/embedded/embedded-faq
- https://learn.microsoft.com/en-us/rest/api/power-bi/
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Microsoft
- FinOps
- FOCUS
---
