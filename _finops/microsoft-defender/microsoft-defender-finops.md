---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-defender-for-endpoint-api-openapi.yml
  format: yaml
  label: Microsoft Defender for Endpoint API
  slug: microsoft-defender-for-endpoint-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-defender/refs/heads/main/openapi/microsoft-defender-for-endpoint-api-openapi.yml
- filename: graph-explorer
  format: yaml
  label: Microsoft Graph Security API
  slug: microsoft-graph-security-api
  spec_type: OpenAPI
  url: https://developer.microsoft.com/en-us/graph/graph-explorer
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription (per Seat) + Pay-As-You-Go (per Resource)
description: FOCUS-aligned FinOps for Microsoft Defender — hybrid model. User-licensed Defender products (Endpoint, Identity, Office 365, Cloud Apps) bill per user per month and roll up through M365 commerce. Defender for Cloud (Servers, Storage, Databases, Containers, CSPM) bills per Azure resource per hour and rolls up through Azure Cost Management with FOCUS-aligned exports. Optimization centers on right-sizing seat coverage, scoping Defender for Cloud plans per subscription, and avoiding double-coverage on E5 customers.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Hybrid (Subscription + Usage)
  PricingUnit: varies (user-month, server-hour, resource-month)
  ProviderName: Microsoft Corporation
  PublisherName: Microsoft Corporation
  ServiceCategory: Security
  ServiceName: Microsoft Defender
layout: finops
meters:
- aggregation: max
  description: Defender for Endpoint Plan 1/2 user seats.
  dimensions:
  - plan
  - department
  - cost_center
  name: defender_endpoint_seats
  unit: user-month
- aggregation: max
  description: Defender for Office 365 Plan 1/2 user seats.
  dimensions:
  - plan
  - tenant
  name: defender_office_seats
  unit: user-month
- aggregation: max
  description: Defender for Identity user seats.
  dimensions:
  - tenant
  name: defender_identity_seats
  unit: user-month
- aggregation: sum
  description: Defender for Servers Plan 1/2 server-hour consumption.
  dimensions:
  - plan
  - subscription
  - region
  - resource_group
  name: defender_servers_hours
  unit: server-hour
- aggregation: max
  description: Defender for Storage protected accounts.
  dimensions:
  - subscription
  - region
  name: defender_storage_accounts
  unit: account-month
- aggregation: sum
  description: Storage operations metered by Defender for Storage.
  dimensions:
  - account
  name: defender_storage_transactions
  unit: 1000-transactions
- aggregation: sum
  description: Defender for SQL / Cosmos DB protection.
  dimensions:
  - db_type
  - subscription
  name: defender_databases_vcore_hours
  unit: vcore-hour
- aggregation: sum
  description: Defender for Containers per-vCore-hour.
  dimensions:
  - cluster
  - cloud
  name: defender_containers_vcore_hours
  unit: vcore-hour
- aggregation: max
  description: Resources covered by Defender CSPM (Plan 2).
  dimensions:
  - resource_type
  - subscription
  name: defender_cspm_resources
  unit: resource-month
name: Microsoft Defender Finops
provider_name: Microsoft Defender
provider_slug: microsoft-defender
publisher_name: Microsoft Corporation
service_category: Security / XDR
slug: microsoft-defender-finops
source_filename: microsoft-defender-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/security/business/microsoft-defender
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Defender\nproviderId: microsoft-defender\npublisherName: Microsoft Corporation\nserviceCategory: Security / XDR\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Security\n  - XDR\n  - Cloud Security\n  - Endpoint\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Microsoft Defender — hybrid model. User-licensed Defender\n  products (Endpoint, Identity, Office 365, Cloud Apps) bill per user per month and roll up\n  through M365 commerce. Defender for Cloud (Servers, Storage, Databases, Containers, CSPM)\n  bills per Azure resource per hour and rolls up through Azure Cost Management with\
  \ FOCUS-aligned\n  exports. Optimization centers on right-sizing seat coverage, scoping Defender for Cloud\n  plans per subscription, and avoiding double-coverage on E5 customers.\nsources:\n  - https://www.microsoft.com/security/business/microsoft-defender\n  - https://azure.microsoft.com/pricing/details/defender-for-cloud/\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription (per Seat) + Pay-As-You-Go (per Resource)\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Defender\n  ServiceCategory: Security\n  ProviderName: Microsoft Corporation\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Hybrid (Subscription + Usage)\n  PricingUnit:\
  \ varies (user-month, server-hour, resource-month)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: defender_endpoint_seats\n    description: Defender for Endpoint Plan 1/2 user seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - plan\n      - department\n      - cost_center\n  - name: defender_office_seats\n    description: Defender for Office 365 Plan 1/2 user seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - plan\n      - tenant\n  - name: defender_identity_seats\n    description: Defender for Identity user seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: defender_servers_hours\n    description: Defender for Servers Plan 1/2 server-hour consumption.\n    unit: server-hour\n    aggregation: sum\n    dimensions:\n      - plan\n      - subscription\n      - region\n      - resource_group\n  - name: defender_storage_accounts\n    description: Defender for Storage protected\
  \ accounts.\n    unit: account-month\n    aggregation: max\n    dimensions:\n      - subscription\n      - region\n  - name: defender_storage_transactions\n    description: Storage operations metered by Defender for Storage.\n    unit: 1000-transactions\n    aggregation: sum\n    dimensions:\n      - account\n  - name: defender_databases_vcore_hours\n    description: Defender for SQL / Cosmos DB protection.\n    unit: vcore-hour\n    aggregation: sum\n    dimensions:\n      - db_type\n      - subscription\n  - name: defender_containers_vcore_hours\n    description: Defender for Containers per-vCore-hour.\n    unit: vcore-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - cloud\n  - name: defender_cspm_resources\n    description: Resources covered by Defender CSPM (Plan 2).\n    unit: resource-month\n    aggregation: max\n    dimensions:\n      - resource_type\n      - subscription\nprinciples:\n  - name: Visibility\n    description: Microsoft 365 admin center surfaces\
  \ Defender seat allocations. Microsoft\n      Defender portal > Settings > Pricing shows Defender for Cloud plan coverage per\n      subscription. Azure Cost Management exports show per-meter line items in FOCUS format.\n      Use Microsoft Sentinel + Defender XDR for unified security event telemetry.\n  - name: Allocation\n    description: Tag Azure subscriptions with cost-center to allocate Defender for Cloud\n      charges. For seat-based SKUs, use Entra ID dynamic groups by department to drive license\n      assignment and chargeback.\n  - name: Optimization\n    description: Avoid stacking — E5 / E5 Security customers already include Defender P2,\n      Identity, MDO P2, MDCA. Disable redundant standalone purchases. Scope Defender for Cloud\n      Plans per subscription, not tenant-wide — turn off Storage / Containers plans on\n      subscriptions without those resources. Use Plan 1 for Servers if you only need EDR; use\n      P2 only where vulnerability assessment / FIM is required.\
  \ Reclaim Endpoint seats from\n      offboarded users monthly.\n  - name: Accountability\n    description: Security team owns plan selection; FinOps validates billing impact before\n      enabling new Defender for Cloud plans. Set Cost Management budgets on the security\n      management group with alerts at 80/100%. Monthly seat reconciliation against Entra ID\n      active users.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.microsoft.com/security/business/microsoft-defender\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-defender/refs/heads/main/finops/microsoft-defender-finops.yml
sources:
- https://www.microsoft.com/security/business/microsoft-defender
- https://azure.microsoft.com/pricing/details/defender-for-cloud/
- https://learn.microsoft.com/en-us/azure/cost-management-billing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Security
- XDR
- Cloud Security
- Endpoint
- Microsoft
- FinOps
- FOCUS
---
