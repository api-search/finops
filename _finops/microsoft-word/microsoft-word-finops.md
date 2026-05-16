---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-word-graph-api.yaml
  format: yaml
  label: Microsoft Graph Word API
  slug: microsoft-graph-word-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-word/refs/heads/main/openapi/microsoft-word-graph-api.yaml
- filename: microsoft-word-javascript-api.yaml
  format: yaml
  label: Office JavaScript API for Word
  slug: office-javascript-api-for-word
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-word/refs/heads/main/openapi/microsoft-word-javascript-api.yaml
- filename: microsoft-word-open-xml-sdk.yaml
  format: yaml
  label: Open XML SDK for Word
  slug: open-xml-sdk-for-word
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-word/refs/heads/main/openapi/microsoft-word-open-xml-sdk.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Microsoft Word: Word is bundled into Microsoft 365 per-user subscriptions; cost is captured at the seat level rather than per-API-call, and storage spend rolls up via the OneDrive entitlement included with each plan.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingUnit: seat-month
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Productivity
  ServiceName: Microsoft Word
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  name: m365_personal_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - tenant
  name: m365_family_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  name: m365_premium_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  name: apps_for_business_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  - has_teams
  name: business_standard_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  - has_teams
  name: business_premium_seats
  unit: seat-month
- aggregation: max
  dimensions:
  - tenant
  - assigned_user
  name: onedrive_storage_consumed
  unit: GB-month
name: Microsoft Word Finops
provider_name: Microsoft Word
provider_slug: microsoft-word
publisher_name: Microsoft Corporation
service_category: Productivity / Documents
slug: microsoft-word-finops
source_filename: microsoft-word-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-365/word
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Word\nproviderId: microsoft-word\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Microsoft\n  - Productivity\ndescription: 'FOCUS-aligned FinOps for Microsoft Word: Word is bundled into Microsoft 365 per-user\n  subscriptions; cost is captured at the seat level rather than per-API-call, and storage spend rolls\n  up via the OneDrive entitlement included with each plan.'\nsources:\n  - https://www.microsoft.com/en-us/microsoft-365/word\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Productivity / Documents\nbillingModel:\n  pricingCategory: Tiered Subscription\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Word\n  ServiceCategory: Productivity\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  PricingUnit: seat-month\n  ChargeCategory: Usage\nmeters:\n  - name: m365_personal_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - assigned_user\n  - name: m365_family_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n  - name: m365_premium_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - assigned_user\n  - name: apps_for_business_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - assigned_user\n  - name: business_standard_seats\n    unit: seat-month\n    aggregation: sum\n\
  \    dimensions:\n      - tenant\n      - assigned_user\n      - has_teams\n  - name: business_premium_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - assigned_user\n      - has_teams\n  - name: onedrive_storage_consumed\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - tenant\n      - assigned_user\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin center license usage report and Productivity Score for\n      per-seat utilization; surface OneDrive storage usage per user via the SharePoint admin center.\n  - name: Allocation\n    description: Allocate seat costs per user via license groups and cost-center attributes in Entra\n      ID; chargeback OneDrive storage to the assigned user's department.\n  - name: Optimization\n    description: Right-size between Apps for Business ($8.25), Business Standard ($12.50/$9.29) and\n      Business Premium ($22.00/$18.79); skip the Teams variant when not needed;\
  \ reclaim seats for\n      inactive users (Productivity Score 30-day inactivity).\n  - name: Accountability\n    description: Assign a license owner per business unit; review monthly seat utilization; require\n      approval for upgrades from Apps for Business to Business Premium based on security need.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-word/refs/heads/main/finops/microsoft-word-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-365/word
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Microsoft
- Productivity
---
