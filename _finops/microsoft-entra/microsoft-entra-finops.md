---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-entra-graph-identity-openapi.yml
  format: yaml
  label: Microsoft Entra ID (Azure AD) API
  slug: graph-identity
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-entra/refs/heads/main/openapi/microsoft-entra-graph-identity-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription + Pay-As-You-Go (External ID)
description: 'FOCUS-aligned FinOps for Microsoft Entra: per-user-per-month subscriptions for the ID tiers (Free, P1, P2, Suite, Governance, Internet Access, Private Access), per-workload-identity for Workload ID, and per-monthly-active-user metering for External ID beyond the 50K free tier.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Identity
  ServiceName: Microsoft Entra
layout: finops
meters:
- aggregation: sum
  description: Per-user seat licences across ID Free / P1 / P2 / Suite
  dimensions:
  - tenant
  - sku
  name: entra_id_seats
  unit: seat
- aggregation: sum
  description: ID Governance seats (requires P1 or P2)
  dimensions:
  - tenant
  name: entra_id_governance_seats
  unit: seat
- aggregation: sum
  description: Internet Access add-on seats
  dimensions:
  - tenant
  name: entra_internet_access_seats
  unit: seat
- aggregation: sum
  description: Private Access add-on seats
  dimensions:
  - tenant
  name: entra_private_access_seats
  unit: seat
- aggregation: sum
  description: Workload identities under Workload ID protection
  dimensions:
  - tenant
  name: workload_identities
  unit: workload_identity
- aggregation: max
  description: Monthly active users for External ID; first 50K free per tenant
  dimensions:
  - tenant
  name: external_id_mau
  unit: monthly_active_user
- aggregation: sum
  description: Verified ID Face Check verification calls (premium add-on)
  name: verified_id_face_check
  unit: verification
name: Microsoft Entra Finops
provider_name: Microsoft Entra
provider_slug: microsoft-entra
publisher_name: Microsoft Corporation
service_category: Identity
slug: microsoft-entra-finops
source_filename: microsoft-entra-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Entra\nproviderId: microsoft-entra\npublisherName: Microsoft Corporation\nserviceCategory: Identity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Identity\n  - Access Management\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Entra: per-user-per-month subscriptions for the ID tiers\n  (Free, P1, P2, Suite, Governance, Internet Access, Private Access), per-workload-identity for Workload\n  ID, and per-monthly-active-user metering for External ID beyond the 50K free tier.'\nsources:\n  - https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing\n  - https://learn.microsoft.com/en-us/entra/\n\
  billingModel:\n  pricingCategory: Tiered Subscription + Pay-As-You-Go (External ID)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Entra\n  ServiceCategory: Identity\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: entra_id_seats\n    description: Per-user seat licences across ID Free / P1 / P2 / Suite\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: entra_id_governance_seats\n    description: ID Governance seats (requires P1 or P2)\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n  - name: entra_internet_access_seats\n    description: Internet Access add-on seats\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n  - name: entra_private_access_seats\n\
  \    description: Private Access add-on seats\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n  - name: workload_identities\n    description: Workload identities under Workload ID protection\n    unit: workload_identity\n    aggregation: sum\n    dimensions:\n      - tenant\n  - name: external_id_mau\n    description: Monthly active users for External ID; first 50K free per tenant\n    unit: monthly_active_user\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: verified_id_face_check\n    description: Verified ID Face Check verification calls (premium add-on)\n    unit: verification\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use Microsoft 365 admin centre for seat licence usage and the Microsoft Entra usage and\n      insights workbooks for sign-ins, MFA, and Conditional Access activity.\n  - name: Allocation\n    description: Tag licence assignments via Entra groups bound to cost-centres; flow External ID MAU\n   \
  \   to the consuming app via Azure subscription tags.\n  - name: Optimization\n    description: Reclaim unused P1 / P2 seats with access reviews and lifecycle workflows; avoid double-licensing\n      where Microsoft 365 E5 already includes Entra ID P2; pre-warm the External ID free 50K MAU tier.\n  - name: Accountability\n    description: Identity team owns Conditional Access scope and Workload ID coverage; finance owns Microsoft\n      365 / Entra licence counts; app owners reconcile External ID MAU against Azure invoices.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-entra/refs/heads/main/finops/microsoft-entra-finops.yml
sources:
- https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing
- https://learn.microsoft.com/en-us/entra/
specification: FinOps Framework
tags:
- Identity
- Access Management
- Microsoft
- FinOps
- FOCUS
---
