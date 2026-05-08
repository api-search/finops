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
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Microsoft Intune: tiered per-user-per-month subscription (Plan 1, Plan 2, Suite) plus per-user add-ons; Plan 1 is bundled in Microsoft 365 E3 / E5 / F3 and EMS E3 / E5. No per-call API charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Endpoint Management
  ServiceName: Microsoft Intune
layout: finops
meters:
- aggregation: sum
  description: Microsoft Intune seat licences (Plan 1 / Plan 2 / Suite or bundled M365 / EMS SKU)
  dimensions:
  - tenant
  - sku
  name: intune_seats
  unit: seat
- aggregation: sum
  description: Add-on seats (EPM, Remote Help, Advanced Analytics, Enterprise App Mgmt, Cloud PKI)
  dimensions:
  - tenant
  - addon
  name: intune_addon_seats
  unit: seat
- aggregation: max
  description: Devices currently enrolled in Intune
  dimensions:
  - tenant
  - os
  - ownership
  name: managed_devices
  unit: device
- aggregation: sum
  description: Microsoft Graph deviceManagement API calls (no charge; tracked for throttling)
  dimensions:
  - application
  - tenant
  name: graph_api_requests
  unit: request
name: Microsoft Intune Finops
provider_name: Microsoft Intune
provider_slug: microsoft-intune
publisher_name: Microsoft Corporation
service_category: Endpoint Management
slug: microsoft-intune-finops
source_filename: microsoft-intune-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/security/business/microsoft-intune-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Intune\nproviderId: microsoft-intune\npublisherName: Microsoft Corporation\nserviceCategory: Endpoint Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Endpoint Management\n  - Intune\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Intune: tiered per-user-per-month subscription (Plan\n  1, Plan 2, Suite) plus per-user add-ons; Plan 1 is bundled in Microsoft 365 E3 / E5 / F3 and EMS E3\n  / E5. No per-call API charge.'\nsources:\n  - https://www.microsoft.com/en-us/security/business/microsoft-intune-pricing\n  - https://learn.microsoft.com/en-us/intune/intune-service/\n\
  billingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Intune\n  ServiceCategory: Endpoint Management\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: intune_seats\n    description: Microsoft Intune seat licences (Plan 1 / Plan 2 / Suite or bundled M365 / EMS SKU)\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: intune_addon_seats\n    description: Add-on seats (EPM, Remote Help, Advanced Analytics, Enterprise App Mgmt, Cloud PKI)\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - addon\n  - name: managed_devices\n    description: Devices currently enrolled in Intune\n    unit: device\n    aggregation: max\n   \
  \ dimensions:\n      - tenant\n      - os\n      - ownership\n  - name: graph_api_requests\n    description: Microsoft Graph deviceManagement API calls (no charge; tracked for throttling)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - application\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin centre licence report and the Intune admin centre device\n      and compliance reports for consumption visibility; capture Graph throttling telemetry from response\n      headers.\n  - name: Allocation\n    description: Map seat licences to Entra groups bound to cost-centres; tag enrolled devices with team\n      / business-unit attributes.\n  - name: Optimization\n    description: Stack Plan 1 + targeted add-ons rather than the Suite when only one or two add-ons are\n      needed; eliminate duplicate licensing where M365 E3/E5/F3 already includes Intune; audit enrolment\n      of unmanaged or orphaned devices.\n  - name: Accountability\n\
  \    description: Endpoint engineering owns enrolment and policy authoring; security owns compliance baseline;\n      finance owns the M365 / EMS / Intune SKU mix.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-intune/refs/heads/main/finops/microsoft-intune-finops.yml
sources:
- https://www.microsoft.com/en-us/security/business/microsoft-intune-pricing
- https://learn.microsoft.com/en-us/intune/intune-service/
specification: FinOps Framework
tags:
- Endpoint Management
- Intune
- Microsoft
- FinOps
- FOCUS
---
