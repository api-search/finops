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
  label: Microsoft Graph API
  slug: microsoft-graph-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: microsoft-graph-identity-api.yml
  format: yaml
  label: Microsoft Graph Identity and Access API
  slug: microsoft-graph-identity-and-access-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-active-directory/refs/heads/main/openapi/microsoft-graph-identity-api.yml
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
description: 'FOCUS-aligned FinOps for Microsoft Entra ID: per-user-per-month subscription licenses (Free, P1, P2, Suite) plus standalone add-ons (Internet/Private Access, ID Governance, Workload ID) and usage-based External ID monthly active users.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Identity
  ServiceName: Microsoft Entra ID
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - department
  name: entra_id_seat_p1
  unit: seat-month
- aggregation: sum
  dimensions:
  - tenant
  - department
  name: entra_id_seat_p2
  unit: seat-month
- aggregation: sum
  name: entra_suite_seat
  unit: seat-month
- aggregation: sum
  name: entra_id_governance_seat
  unit: seat-month
- aggregation: sum
  name: entra_internet_access_seat
  unit: seat-month
- aggregation: sum
  name: entra_private_access_seat
  unit: seat-month
- aggregation: sum
  name: entra_workload_identity
  unit: workload_identity-month
- aggregation: sum
  dimensions:
  - tenant
  - app
  name: external_id_mau
  unit: monthly_active_user
name: Microsoft Azure Active Directory Finops
provider_name: Microsoft Azure Active Directory
provider_slug: microsoft-azure-active-directory
publisher_name: Microsoft Corporation
service_category: Identity
slug: microsoft-azure-active-directory-finops
source_filename: microsoft-azure-active-directory-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Azure Active Directory\nproviderId: microsoft-azure-active-directory\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Identity\n  - Microsoft Entra\ndescription: 'FOCUS-aligned FinOps for Microsoft Entra ID: per-user-per-month subscription licenses\n  (Free, P1, P2, Suite) plus standalone add-ons (Internet/Private Access, ID Governance, Workload ID)\n  and usage-based External ID monthly active users.'\nsources:\n  - https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing\n  - https://azure.microsoft.com/en-us/pricing/details/active-directory/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft\
  \ Corporation\nserviceCategory: Identity\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Entra ID\n  ServiceCategory: Identity\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: entra_id_seat_p1\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - department\n  - name: entra_id_seat_p2\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - department\n  - name: entra_suite_seat\n    unit: seat-month\n    aggregation: sum\n  - name: entra_id_governance_seat\n    unit: seat-month\n    aggregation: sum\n  - name: entra_internet_access_seat\n    unit: seat-month\n    aggregation: sum\n  - name: entra_private_access_seat\n\
  \    unit: seat-month\n    aggregation: sum\n  - name: entra_workload_identity\n    unit: workload_identity-month\n    aggregation: sum\n  - name: external_id_mau\n    unit: monthly_active_user\n    aggregation: sum\n    dimensions:\n      - tenant\n      - app\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin center license usage reports and Azure Cost Management\n      to view Entra ID, External ID, and add-on consumption. Export usage to a Log Analytics workspace\n      for detailed reporting.\n  - name: Allocation\n    description: Tag licensed users via Microsoft 365 license groups and Entra group-based licensing\n      to attribute spend to departments and cost centers.\n  - name: Optimization\n    description: Reclaim unused P1/P2 licenses with access reviews; right-size between Free, P1, and\n      P2 based on per-user feature consumption; switch eligible CIAM workloads from B2C legacy to\n      External ID free MAU tier.\n  - name: Accountability\n\
  \    description: Assign license budget owners per business unit; review annually at Microsoft Enterprise\n      Agreement true-up; alert on access-review completions and over-provisioning.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-active-directory/refs/heads/main/finops/microsoft-azure-active-directory-finops.yml
sources:
- https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing
- https://azure.microsoft.com/en-us/pricing/details/active-directory/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Identity
- Microsoft Entra
---
