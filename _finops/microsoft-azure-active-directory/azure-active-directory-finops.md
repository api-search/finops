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
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: microsoft-graph-identity-api.yml
  format: yaml
  label: Microsoft Graph Identity and Access API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-active-directory/refs/heads/main/openapi/microsoft-graph-identity-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Microsoft Entra ID: per-user-per-month subscription pricing for P1/P2/Governance, plus monthly-active-user metering for External ID (CIAM). Billed via Microsoft 365 / Azure invoicing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Subscription
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Identity
  ServiceName: Microsoft Entra ID
layout: finops
meters:
- aggregation: max
  description: Per-user license assignment for Entra ID P1, P2, and Governance
  dimensions:
  - sku
  - tenant
  name: licensed_users
  unit: seat
- aggregation: sum
  description: Monthly active users (B2C / customer identity)
  dimensions:
  - tenant
  - flow
  name: external_id_mau
  unit: monthly_active_user
- aggregation: max
  description: Service principals / managed identities licensed for Workload ID Premium
  dimensions:
  - tenant
  name: workload_identities
  unit: workload_identity
- aggregation: sum
  description: Verifiable credentials issued / verified
  name: verified_id_credentials
  unit: credential
name: Azure Active Directory Finops
provider_name: Microsoft Azure Active Directory
provider_slug: microsoft-azure-active-directory
publisher_name: Microsoft Corporation
service_category: Identity
slug: azure-active-directory-finops
source_filename: azure-active-directory-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Azure Active Directory\nproviderId: microsoft-azure-active-directory\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Identity\n  - Microsoft Entra\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Entra ID: per-user-per-month subscription pricing for\n  P1/P2/Governance, plus monthly-active-user metering for External ID (CIAM). Billed via Microsoft 365 /\n  Azure invoicing.'\nsources:\n  - https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing\n  - https://learn.microsoft.com/en-us/entra/fundamentals/licensing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Identity\n\
  billingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Entra ID\n  ServiceCategory: Identity\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Subscription\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: licensed_users\n    description: Per-user license assignment for Entra ID P1, P2, and Governance\n    unit: seat\n    aggregation: max\n    dimensions:\n      - sku\n      - tenant\n  - name: external_id_mau\n    description: Monthly active users (B2C / customer identity)\n    unit: monthly_active_user\n    aggregation: sum\n    dimensions:\n      - tenant\n      - flow\n  - name: workload_identities\n    description: Service principals / managed identities licensed for Workload ID Premium\n    unit: workload_identity\n\
  \    aggregation: max\n    dimensions:\n      - tenant\n  - name: verified_id_credentials\n    description: Verifiable credentials issued / verified\n    unit: credential\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft Entra admin center license usage report and Microsoft 365 admin center\n      billing exports to track P1/P2/Governance assignments and External ID MAU consumption.\n  - name: Allocation\n    description: Tag licensed users via department / cost-center attributes synced from HR; allocate\n      External ID MAU costs to consuming customer apps via app metadata.\n  - name: Optimization\n    description: Reclaim unused P1/P2 licenses via Microsoft Entra access reviews and lifecycle workflows;\n      consolidate guest invitations under External ID where pay-per-MAU is cheaper than per-seat licensing.\n  - name: Accountability\n    description: Assign IAM admins as license budget owners; review license assignments quarterly through\n\
  \      Entra ID Governance access reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-active-directory/refs/heads/main/finops/azure-active-directory-finops.yml
sources:
- https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing
- https://learn.microsoft.com/en-us/entra/fundamentals/licensing
specification: FinOps Framework
tags:
- Identity
- Microsoft Entra
- FinOps
- FOCUS
---
