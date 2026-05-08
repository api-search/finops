---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: identity-toolkit-openapi.yml
  format: yaml
  label: Identity Toolkit API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-identity-platform/refs/heads/main/openapi/identity-toolkit-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Google Identity Platform: per-MAU usage charges plus per-SMS phone authentication, billed through the Google Cloud invoice with full Cloud Billing integration.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC
  ProviderName: Google
  PublisherName: Google LLC
  ServiceCategory: Identity
  ServiceName: Google Identity Platform
layout: finops
meters:
- aggregation: max
  description: MAUs authenticated via standard providers (email/password, social, anonymous, custom)
  dimensions:
  - tenant
  - provider
  - region
  name: monthly_active_users_standard
  unit: mau
- aggregation: max
  description: MAUs authenticated via SAML or OIDC enterprise providers
  dimensions:
  - tenant
  - provider
  - region
  name: monthly_active_users_saml_oidc
  unit: mau
- aggregation: sum
  description: SMS phone-auth verification messages sent
  dimensions:
  - destination_country
  - tenant
  name: phone_auth_verifications
  unit: sms
name: Google Identity Platform Finops
provider_name: Google Identity Platform
provider_slug: google-identity-platform
publisher_name: Google LLC
service_category: Identity
slug: google-identity-platform-finops
source_filename: google-identity-platform-finops.yml
source_heading: FinOps Profile
source_url: https://cloud.google.com/identity-platform/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Identity Platform\nproviderId: google-identity-platform\npublisherName: Google LLC\nserviceCategory: Identity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Identity\n  - Authentication\n  - Google Cloud\ndescription: 'FOCUS-aligned FinOps for Google Identity Platform: per-MAU usage charges plus per-SMS phone\n  authentication, billed through the Google Cloud invoice with full Cloud Billing integration.'\nsources:\n  - https://cloud.google.com/identity-platform/pricing\n  - https://firebase.google.com/pricing\n  - https://cloud.google.com/billing/docs\nbillingModel:\n  pricingCategory: Pay-As-You-Go\
  \ + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Google Identity Platform\n  ServiceCategory: Identity\n  ProviderName: Google\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: monthly_active_users_standard\n    description: MAUs authenticated via standard providers (email/password, social, anonymous, custom)\n    unit: mau\n    aggregation: max\n    dimensions:\n      - tenant\n      - provider\n      - region\n  - name: monthly_active_users_saml_oidc\n    description: MAUs authenticated via SAML or OIDC enterprise providers\n    unit: mau\n    aggregation: max\n    dimensions:\n      - tenant\n      - provider\n      - region\n  - name: phone_auth_verifications\n    description: SMS phone-auth verification messages sent\n    unit: sms\n    aggregation: sum\n  \
  \  dimensions:\n      - destination_country\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Use Google Cloud Billing exports to BigQuery and the Identity Platform usage dashboard\n      to track MAU and SMS spend per project.\n  - name: Allocation\n    description: Tag Google Cloud projects and Identity Platform tenants with team / environment labels\n      so MAU and SMS charges roll up per consuming team.\n  - name: Optimization\n    description: Move suitable workloads under the 50K-MAU no-cost tier; consolidate sandbox tenants into\n      shared projects; restrict SMS auth to high-risk geographies and prefer TOTP for low-risk users.\n  - name: Accountability\n    description: Set Cloud Billing budgets and anomaly alerts on the Identity Platform SKU; review\n      monthly MAU growth against forecast.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-identity-platform/refs/heads/main/finops/google-identity-platform-finops.yml
sources:
- https://cloud.google.com/identity-platform/pricing
- https://firebase.google.com/pricing
- https://cloud.google.com/billing/docs
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Identity
- Authentication
- Google Cloud
---
