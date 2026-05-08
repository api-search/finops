---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Subscription (Per User) + Optional Add-Ons
description: FOCUS-aligned FinOps for LastPass. Cost is dominated by per-user-per-month subscriptions (Teams, Business, MFA, Identity bundles); the Enterprise API and SCIM endpoint themselves are not metered separately. Personal plans bill annually with a small monthly equivalent. Add-ons stack as separate per-user lines (MFA, advanced reporting). Optimization levers are seat hygiene (offboarding inactive users) and bundle selection (Identity vs. Business + MFA add-on).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: LastPass US LP
  ProviderName: LastPass
  PublisherName: LastPass US LP
  ServiceCategory: Identity and Access Management
  ServiceName: LastPass
layout: finops
meters:
- aggregation: sum
  description: Recurring per-user subscription for the active business tier (Teams, Business, Identity bundle) or the personal subscription line (Premium, Families).
  dimensions:
  - plan_tier
  - billing_cycle
  name: subscription_fee_per_user
  unit: user_month
- aggregation: sum
  description: Per-user-per-month subscription for the MFA add-on layered on top of Teams or Business.
  dimensions:
  - plan_tier
  name: mfa_addon_fee
  unit: user_month
- aggregation: max
  description: Encrypted file storage consumed across vaults; bundled per-user GB included by tier.
  dimensions:
  - organization_id
  name: storage
  unit: GB
name: Lastpass Finops
provider_name: LastPass
provider_slug: lastpass
publisher_name: LastPass US LP
service_category: Identity and Access Management
slug: lastpass-finops
source_filename: lastpass-finops.yml
source_heading: FinOps Profile
source_url: https://www.lastpass.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LastPass\nproviderId: lastpass\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Security\n  - Password Manager\n  - Vault\n  - Identity\n  - Enterprise\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for LastPass. Cost is dominated by per-user-per-month\n  subscriptions (Teams, Business, MFA, Identity bundles); the Enterprise API and SCIM\n  endpoint themselves are not metered separately. Personal plans bill annually with a\n  small monthly equivalent. Add-ons stack as separate per-user lines (MFA, advanced\n  reporting). Optimization levers are seat hygiene (offboarding inactive users) and\n  bundle selection (Identity vs. Business + MFA add-on).\nsources:\n  - https://www.lastpass.com/pricing\n  - https://support.lastpass.com/help/use-the-lastpass-enterprise-api\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: LastPass US LP\nserviceCategory: Identity and Access Management\nbillingModel:\n  pricingCategory: Subscription (Per User) + Optional Add-Ons\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: LastPass\n  ServiceCategory: Identity and Access Management\n  ProviderName: LastPass\n  PublisherName: LastPass US LP\n  InvoiceIssuerName: LastPass US LP\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_fee_per_user\n    description: >-\n      Recurring per-user subscription for the active business tier (Teams, Business,\n      Identity bundle) or the personal subscription line (Premium, Families).\n    unit: user_month\n    aggregation: sum\n    dimensions:\n  \
  \    - plan_tier\n      - billing_cycle\n  - name: mfa_addon_fee\n    description: >-\n      Per-user-per-month subscription for the MFA add-on layered on top of Teams or\n      Business.\n    unit: user_month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n  - name: storage\n    description: >-\n      Encrypted file storage consumed across vaults; bundled per-user GB included by\n      tier.\n    unit: GB\n    aggregation: max\n    dimensions:\n      - organization_id\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Enterprise API getuserdata, getsfdata, and getreport commands to track\n      user counts and login activity, and feed those into seat reconciliation. Map\n      directory connector / SCIM events to expected on/offboarding cadence.\n  - name: Allocation\n    description: >-\n      Map LastPass groups to business units. Use SCIM groups to enforce the mapping\n      so the per-user bill stays tied to HR truth.\n  - name: Optimization\n    description:\
  \ >-\n      Disable rather than delete inactive users to free seats while keeping audit\n      history. Compare the Identity bundle price against (Business + MFA add-on) to\n      pick the cheaper assembly. Avoid double-paying when an external IdP already\n      provides MFA.\n  - name: Accountability\n    description: >-\n      Assign an IT or security owner per LastPass company. Review seat utilisation\n      monthly via getuserdata exports and renegotiate add-on inclusion at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lastpass/refs/heads/main/finops/lastpass-finops.yml
sources:
- https://www.lastpass.com/pricing
- https://support.lastpass.com/help/use-the-lastpass-enterprise-api
specification: FinOps Framework
tags:
- Security
- Password Manager
- Vault
- Identity
- Enterprise
- FinOps
- FOCUS
---
