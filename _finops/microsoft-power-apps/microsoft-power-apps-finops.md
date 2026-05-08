---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Power Apps API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.microsoft.com/en-us/connectors/powerappsforappmakers/
- filename: openapi
  format: yaml
  label: Dataverse API (Common Data Service)
  slug: ''
  spec_type: OpenAPI
  url: https://docs.microsoft.com/en-us/power-apps/developer/data-platform/webapi/openapi
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Microsoft Power Apps: per-user subscriptions plus Dataverse capacity add-ons and optional Azure-billed pay-as-you-go meter, governed by 24-hour Power Platform request entitlements.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingUnit: seat-month
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Business Applications
  ServiceName: Microsoft Power Apps
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - environment
  - assigned_user
  name: premium_seats
  unit: seat
- aggregation: count
  dimensions:
  - tenant
  name: developer_seats
  unit: seat
- aggregation: sum
  dimensions:
  - user
  - environment
  - product
  - tenant
  name: power_platform_requests
  unit: request
- aggregation: max
  dimensions:
  - environment
  - tenant
  name: dataverse_database_capacity
  unit: GB-month
- aggregation: max
  dimensions:
  - environment
  - tenant
  name: dataverse_file_capacity
  unit: GB-month
- aggregation: sum
  dimensions:
  - tenant
  name: ppr_capacity_addon_packs
  unit: pack-month
- aggregation: count
  dimensions:
  - app
  - environment
  name: payg_active_users
  unit: user
name: Microsoft Power Apps Finops
provider_name: Microsoft Power Apps
provider_slug: microsoft-power-apps
publisher_name: Microsoft Corporation
service_category: Business Applications / Low-Code
slug: microsoft-power-apps-finops
source_filename: microsoft-power-apps-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/power-platform/products/power-apps/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Power Apps\nproviderId: microsoft-power-apps\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Microsoft\n  - Power Platform\n  - Low-Code\ndescription: 'FOCUS-aligned FinOps for Microsoft Power Apps: per-user subscriptions plus Dataverse capacity\n  add-ons and optional Azure-billed pay-as-you-go meter, governed by 24-hour Power Platform request entitlements.'\nsources:\n  - https://www.microsoft.com/en-us/power-platform/products/power-apps/pricing\n  - https://learn.microsoft.com/en-us/power-platform/admin/api-request-limits-allocations\n  - https://learn.microsoft.com/en-us/power-apps/developer/data-platform/api-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Business Applications / Low-Code\nbillingModel:\n  pricingCategory: Tiered Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Power Apps\n  ServiceCategory: Business Applications\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  PricingUnit: seat-month\n  ChargeCategory: Usage\nmeters:\n  - name: premium_seats\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - environment\n      - assigned_user\n  - name: developer_seats\n    unit: seat\n    aggregation: count\n    dimensions:\n      - tenant\n  - name: power_platform_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - user\n  \
  \    - environment\n      - product\n      - tenant\n  - name: dataverse_database_capacity\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - environment\n      - tenant\n  - name: dataverse_file_capacity\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - environment\n      - tenant\n  - name: ppr_capacity_addon_packs\n    unit: pack-month\n    aggregation: sum\n    dimensions:\n      - tenant\n  - name: payg_active_users\n    unit: user\n    aggregation: count\n    dimensions:\n      - app\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use the Power Platform admin center capacity reports (Licensed user, Non-licensed\n      user, Per-flow) to download CSV usage of Power Platform requests; surface seat licensing through\n      the Microsoft 365 admin center.\n  - name: Allocation\n    description: Tag environments with consuming team / cost center; attribute seat licenses to assigned\n      users via Microsoft 365 license groups;\
  \ allocate Dataverse capacity by environment to map back\n      to product owners.\n  - name: Optimization\n    description: Right-size between Premium ($20) and per-app / pay-as-you-go for low-frequency users;\n      consolidate apps to fewer environments to reduce Dataverse capacity floor; cache Dataverse reads\n      to stay under the 6,000-requests / 5-minute service-protection ceiling rather than buying PPR\n      add-ons.\n  - name: Accountability\n    description: Assign each environment to a budget owner; review the Capacity page monthly; investigate\n      users who breach 75% of their PPR daily entitlement two days in a row to determine whether they\n      need an add-on, a license upgrade, or a code fix.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-power-apps/refs/heads/main/finops/microsoft-power-apps-finops.yml
sources:
- https://www.microsoft.com/en-us/power-platform/products/power-apps/pricing
- https://learn.microsoft.com/en-us/power-platform/admin/api-request-limits-allocations
- https://learn.microsoft.com/en-us/power-apps/developer/data-platform/api-limits
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Microsoft
- Power Platform
- Low-Code
---
