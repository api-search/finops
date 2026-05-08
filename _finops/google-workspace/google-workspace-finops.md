---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: admin-sdk-directory-api.yml
  format: yaml
  label: Admin SDK Directory API
  slug: admin-directory
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-workspace/refs/heads/main/openapi/admin-sdk-directory-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Google Workspace: per-user-per-month seat subscription with pooled storage, billed monthly or annually. Workspace REST APIs are bundled with the seat license at no per-call charge; cost is therefore measured in seats and storage, not in API calls.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Google LLC
  ProviderName: Google
  PublisherName: Google LLC
  ServiceCategory: Productivity / Collaboration SaaS
  ServiceName: Google Workspace
layout: finops
meters:
- aggregation: max
  description: Active Workspace seats by edition
  dimensions:
  - edition
  - org_unit
  - billing_account
  name: workspace_seats
  unit: seat
- aggregation: avg
  description: Pooled storage consumed across the domain
  dimensions:
  - org_unit
  - service
  name: pooled_storage
  unit: GB-month
- aggregation: avg
  description: Storage consumed by Meet recordings
  name: meet_recordings_storage
  unit: GB-month
- aggregation: avg
  description: Vault retention storage for Business Plus / Enterprise
  name: vault_retention
  unit: GB-month
- aggregation: sum
  description: Workspace API call volume (operational metric — not directly billed)
  dimensions:
  - api
  - org_unit
  name: api_requests
  unit: request
name: Google Workspace Finops
provider_name: Google Workspace
provider_slug: google-workspace
publisher_name: Google LLC
service_category: Productivity / Collaboration SaaS
slug: google-workspace-finops
source_filename: google-workspace-finops.yml
source_heading: FinOps Profile
source_url: https://workspace.google.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Workspace\nproviderId: google-workspace\npublisherName: Google LLC\nserviceCategory: Productivity / Collaboration SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\ntags:\n  - FinOps\n  - FOCUS\n  - Productivity\n  - Collaboration\n  - Email\n  - Storage\nreconciled: true\ndescription: 'FOCUS-aligned FinOps for Google Workspace: per-user-per-month seat subscription with\n  pooled storage, billed monthly or annually. Workspace REST APIs are bundled with the seat license at\n  no per-call charge; cost is therefore measured in seats and storage, not in API calls.'\nsources:\n  - https://workspace.google.com/pricing\n  - https://support.google.com/a/answer/7232932\n\
  billingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Google Workspace\n  ServiceCategory: Productivity / Collaboration SaaS\n  ProviderName: Google\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: workspace_seats\n    description: Active Workspace seats by edition\n    unit: seat\n    aggregation: max\n    dimensions:\n      - edition\n      - org_unit\n      - billing_account\n  - name: pooled_storage\n    description: Pooled storage consumed across the domain\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - org_unit\n      - service\n  - name: meet_recordings_storage\n    description: Storage consumed by Meet recordings\n    unit: GB-month\n    aggregation: avg\n  - name: vault_retention\n    description: Vault\
  \ retention storage for Business Plus / Enterprise\n    unit: GB-month\n    aggregation: avg\n  - name: api_requests\n    description: Workspace API call volume (operational metric — not directly billed)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - org_unit\nprinciples:\n  - name: Visibility\n    description: Use the Admin SDK Reports API (or BigQuery audit log export) and the Workspace\n      Admin Console billing report to see seat counts, storage consumption, and API call patterns.\n  - name: Allocation\n    description: Place users in Organizational Units mapped to cost centers; assign editions per OU\n      so seat charges roll up to the right business owner.\n  - name: Optimization\n    description: Right-size editions per OU (Business Standard for general staff, Plus for\n      compliance-heavy roles); reclaim seats from inactive accounts; archive Vault data on retention\n      policy; purge stale Drive shared drives.\n  - name: Accountability\n\
  \    description: Designate a Workspace billing owner per division; review monthly Admin Console\n      reports for seat / storage growth vs. forecast and catch rogue automation hitting API quotas.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-workspace/refs/heads/main/finops/google-workspace-finops.yml
sources:
- https://workspace.google.com/pricing
- https://support.google.com/a/answer/7232932
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Productivity
- Collaboration
- Email
- Storage
---
