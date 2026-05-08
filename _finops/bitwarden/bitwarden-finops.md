---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Members
  slug: public-members
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Groups
  slug: public-groups
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Collections
  slug: public-collections
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Policies
  slug: public-policies
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Event Logs
  slug: public-events
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Subscription (Per User) + Optional Add-Ons
description: FOCUS-aligned FinOps for Bitwarden. The Public API and SCIM endpoints are not metered separately - they are bundled in the underlying password-manager subscription (Teams $4/user/month or Enterprise $6/user/month, billed annually). Personal plans (Premium $9.99/year, Families $40/year for 6 users) do not include API access. Secrets Manager is sold as a separate per-user-per-month add-on with a tier-dependent machine-account allowance. Self-host is included; cloud regions split US and EU with no price difference.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Bitwarden, Inc.
  ProviderName: Bitwarden
  PublisherName: Bitwarden, Inc.
  ServiceCategory: Identity and Access Management
  ServiceName: Bitwarden
layout: finops
meters:
- aggregation: sum
  description: Recurring per-user subscription for the active password-manager tier (Teams, Enterprise) or per-account fee for personal plans (Premium, Families).
  dimensions:
  - plan_tier
  - billing_cycle
  name: subscription_fee_per_user
  unit: user_month
- aggregation: sum
  description: Per-user-per-month subscription for the Secrets Manager add-on; price varies by Teams or Enterprise underlying tier.
  dimensions:
  - plan_tier
  - billing_cycle
  name: secrets_manager_fee
  unit: user_month
- aggregation: max
  description: Machine accounts consumed against the Secrets Manager allowance bundled with the add-on; overage requires moving to a higher tier.
  dimensions:
  - organization_id
  name: machine_accounts
  unit: machine_account
- aggregation: max
  description: Encrypted storage consumed by file attachments and Send across the organization and personal accounts; bundled GB included by tier.
  dimensions:
  - organization_id
  name: storage
  unit: GB
name: Bitwarden Finops
provider_name: Bitwarden
provider_slug: bitwarden
publisher_name: Bitwarden, Inc.
service_category: Identity and Access Management
slug: bitwarden-finops
source_filename: bitwarden-finops.yml
source_heading: FinOps Profile
source_url: https://bitwarden.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bitwarden\nproviderId: bitwarden\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Security\n  - Password Manager\n  - Open Source\n  - Vault\n  - Identity\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Bitwarden. The Public API and SCIM endpoints are not metered\n  separately - they are bundled in the underlying password-manager subscription\n  (Teams $4/user/month or Enterprise $6/user/month, billed annually). Personal plans\n  (Premium $9.99/year, Families $40/year for 6 users) do not include API access.\n  Secrets Manager is sold as a separate per-user-per-month add-on with a tier-dependent\n  machine-account allowance. Self-host is included; cloud regions split US and EU\n  with no price difference.\nsources:\n  - https://bitwarden.com/pricing/\n  - https://www.bitwarden.com/products/business/\n  - https://bitwarden.com/help/public-api/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Bitwarden, Inc.\nserviceCategory: Identity and Access Management\nbillingModel:\n  pricingCategory: Subscription (Per User) + Optional Add-Ons\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Bitwarden\n  ServiceCategory: Identity and Access Management\n  ProviderName: Bitwarden\n  PublisherName: Bitwarden, Inc.\n  InvoiceIssuerName: Bitwarden, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_fee_per_user\n    description: >-\n      Recurring per-user subscription for the active password-manager tier (Teams,\n      Enterprise) or per-account fee for personal plans (Premium, Families).\n    unit:\
  \ user_month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n      - billing_cycle\n  - name: secrets_manager_fee\n    description: >-\n      Per-user-per-month subscription for the Secrets Manager add-on; price varies by\n      Teams or Enterprise underlying tier.\n    unit: user_month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n      - billing_cycle\n  - name: machine_accounts\n    description: >-\n      Machine accounts consumed against the Secrets Manager allowance bundled with the\n      add-on; overage requires moving to a higher tier.\n    unit: machine_account\n    aggregation: max\n    dimensions:\n      - organization_id\n  - name: storage\n    description: >-\n      Encrypted storage consumed by file attachments and Send across the organization\n      and personal accounts; bundled GB included by tier.\n    unit: GB\n    aggregation: max\n    dimensions:\n      - organization_id\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the\
  \ Public API event-logs endpoint to track member activity and feed invoice\n      reconciliation. Member counts in the Admin Console map directly to the per-user\n      billing line.\n  - name: Allocation\n    description: >-\n      Map Bitwarden organizations and groups to business units. Use directory connector\n      or SCIM to keep member counts aligned with HR truth so the per-user line cannot\n      drift.\n  - name: Optimization\n    description: >-\n      Choose Teams over Enterprise unless SSO, account recovery, or enterprise policies\n      are needed. Offboard inactive members promptly via SCIM. Self-host where data\n      residency or contractual requirements would otherwise drive add-on costs.\n  - name: Accountability\n    description: >-\n      Assign a security or IT owner per Bitwarden organization. Review SCIM\n      reconciliation logs each cycle and renegotiate Secrets Manager seats and\n      machine-account allowances at renewal.\nmaintainers:\n  - FN: Kin Lane\n\
  \    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/finops/bitwarden-finops.yml
sources:
- https://bitwarden.com/pricing/
- https://www.bitwarden.com/products/business/
- https://bitwarden.com/help/public-api/
specification: FinOps Framework
tags:
- Security
- Password Manager
- Open Source
- Vault
- Identity
- FinOps
- FOCUS
---
