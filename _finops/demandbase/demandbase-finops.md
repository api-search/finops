---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: demandbase-api-openapi.yml
  format: yaml
  label: Demandbase API
  slug: demandbase-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-api-openapi.yml
- filename: demandbase-real-time-identification-openapi.yml
  format: yaml
  label: Demandbase Real-Time Identification API
  slug: demandbase-real-time-identification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-real-time-identification-openapi.yml
- filename: demandbase-advertising-openapi.yml
  format: yaml
  label: Demandbase Advertising API
  slug: demandbase-advertising-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-advertising-openapi.yml
- filename: demandbase-engagement-openapi.yml
  format: yaml
  label: Demandbase Engagement API
  slug: demandbase-engagement-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-engagement-openapi.yml
- filename: demandbase-account-list-openapi.yml
  format: yaml
  label: Demandbase Account List API
  slug: demandbase-account-list-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-account-list-openapi.yml
- filename: demandbase-b2b-data-openapi.yml
  format: yaml
  label: Demandbase B2B Data API
  slug: demandbase-b2b-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-b2b-data-openapi.yml
- filename: demandbase-ip-openapi.yml
  format: yaml
  label: Demandbase IP API
  slug: demandbase-ip-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-ip-openapi.yml
- filename: demandbase-admin-openapi.yml
  format: yaml
  label: Demandbase Admin API
  slug: demandbase-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-admin-openapi.yml
- filename: demandbase-data-export-openapi.yml
  format: yaml
  label: Demandbase Data Export API
  slug: demandbase-data-export-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-data-export-openapi.yml
- filename: demandbase-data-import-openapi.yml
  format: yaml
  label: Demandbase Data Import API
  slug: demandbase-data-import-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/openapi/demandbase-data-import-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: SaaS Subscription (Platform Fee + Per-User) + Media Pass-Through
description: 'FOCUS-aligned FinOps for Demandbase: SaaS subscription with platform fee plus per-user fee per package, plus media-spend pass-through for the Advertising product line.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Demandbase, Inc.
  PricingCategory: Subscription
  PricingUnit: seat
  ProviderName: Demandbase
  PublisherName: Demandbase, Inc.
  ServiceCategory: B2B Marketing / Sales Intelligence
  ServiceName: Demandbase
layout: finops
meters:
- aggregation: sum
  description: Annual platform fee per Demandbase package
  dimensions:
  - subscription
  - package
  name: platform_fee
  unit: month
- aggregation: max
  description: Active platform users
  dimensions:
  - subscription
  - package
  name: user_seats
  unit: seat
- aggregation: sum
  description: Advertising media spend running through Demandbase Advertising
  dimensions:
  - campaign
  - audience
  name: media_spend
  unit: USD
- aggregation: sum
  description: Demandbase Data records consumed via export / import / enrichment
  dimensions:
  - subscription
  name: data_license
  unit: record
name: Demandbase Finops
provider_name: Demandbase
provider_slug: demandbase
publisher_name: Demandbase, Inc.
service_category: B2B Marketing / Sales Intelligence
slug: demandbase-finops
source_filename: demandbase-finops.yml
source_heading: FinOps Profile
source_url: https://www.demandbase.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Demandbase\nproviderId: demandbase\npublisherName: Demandbase, Inc.\nserviceCategory: B2B Marketing / Sales Intelligence\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: 'Demandbase pricing is platform-fee + per-user with custom-quoted package totals (Demandbase One,\n  Advertising, Data) confirmed at https://www.demandbase.com/pricing/. FinOps shape is SaaS subscription;\n  advertising spend is a separate pass-through. Reconcile against platform invoice when available.'\ntags:\n  - Account-Based Marketing\n  - Advertising\n  - B2B Marketing\n  - Data\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Demandbase: SaaS subscription with platform fee plus\
  \ per-user fee\n  per package, plus media-spend pass-through for the Advertising product line.'\nsources:\n  - https://www.demandbase.com/pricing/\n  - https://developer.demandbase.com/\nprinciples:\n  - name: Visibility\n    description: Track Demandbase platform spend per package (One / Advertising / Data) and per-seat counts\n      via the customer admin console; reconcile media spend separately for advertising campaigns.\n  - name: Allocation\n    description: Allocate platform spend across go-to-market teams (sales, marketing) based on seat ownership;\n      allocate ad spend by campaign to brand or product owners.\n  - name: Optimization\n    description: Right-size active platform seats quarterly, prune inactive users, consolidate ad campaigns\n      and audiences, and audit data export / import volume to avoid over-provisioning data licenses.\n  - name: Accountability\n    description: Marketing operations owns platform-fee renewal; advertising owns media spend; data ops\n    \
  \  owns data-license consumption. Establish a quarterly review against contract entitlements.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: SaaS Subscription (Platform Fee + Per-User) + Media Pass-Through\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName:\
  \ Demandbase\n  ServiceCategory: B2B Marketing / Sales Intelligence\n  ProviderName: Demandbase\n  PublisherName: Demandbase, Inc.\n  InvoiceIssuerName: Demandbase, Inc.\n  PricingCategory: Subscription\n  PricingUnit: seat\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: platform_fee\n    description: Annual platform fee per Demandbase package\n    unit: month\n    aggregation: sum\n    dimensions:\n      - subscription\n      - package\n  - name: user_seats\n    description: Active platform users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - subscription\n      - package\n  - name: media_spend\n    description: Advertising media spend running through Demandbase Advertising\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - campaign\n      - audience\n  - name: data_license\n    description: Demandbase Data records consumed via export / import / enrichment\n    unit: record\n    aggregation: sum\n    dimensions:\n      - subscription\n\
  apis:\n  - name: Demandbase Real-Time Identification API\n    baseURL: https://api.company-target.com\n    tags:\n      - Identification\n      - IP Intelligence\n      - Real-Time\n      - Visitor Tracking\n    serviceName: Demandbase Real-Time Identification API\n    serviceCategory: API\n  - name: Demandbase Advertising API\n    baseURL: https://api.demandbase.com/advertising\n    tags:\n      - ABM\n      - Advertising\n      - Audiences\n      - Campaigns\n    serviceName: Demandbase Advertising API\n    serviceCategory: API\n  - name: Demandbase Engagement API\n    baseURL: https://api.demandbase.com/engagement\n    tags:\n      - Account Insights\n      - Activity Tracking\n      - Analytics\n      - Engagement\n    serviceName: Demandbase Engagement API\n    serviceCategory: API\n  - name: Demandbase Account List API\n    baseURL: https://api.demandbase.com/accounts\n    tags:\n      - Account Lists\n      - CRM Sync\n      - List Management\n      - Target Accounts\n    serviceName:\
  \ Demandbase Account List API\n    serviceCategory: API\n  - name: Demandbase B2B Data API\n    baseURL: https://api.demandbase.com\n    tags:\n      - B2B Data\n      - Company Search\n      - Contact Discovery\n      - Data Enrichment\n      - Firmographics\n    serviceName: Demandbase B2B Data API\n    serviceCategory: API\n  - name: Demandbase IP API\n    baseURL: https://api.demandbase.com\n    tags:\n      - Company Identification\n      - Firmographics\n      - IP Intelligence\n      - Real-Time\n      - Visitor Identification\n    serviceName: Demandbase IP API\n    serviceCategory: API\n  - name: Demandbase Admin API\n    baseURL: https://api.demandbase.com\n    tags:\n      - Administration\n      - API Keys\n      - Platform Management\n      - User Management\n    serviceName: Demandbase Admin API\n    serviceCategory: API\n  - name: Demandbase Data Export API\n    baseURL: https://api.demandbase.com\n    tags:\n      - Accounts\n      - Analytics\n      - Bulk Export\n   \
  \   - Data Export\n      - Reporting\n    serviceName: Demandbase Data Export API\n    serviceCategory: API\n  - name: Demandbase Data Import API\n    baseURL: https://api.demandbase.com\n    tags:\n      - Accounts\n      - Bulk Import\n      - CSV\n      - Data Import\n      - Data Ingestion\n    serviceName: Demandbase Data Import API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Platform Seat\n    metric: platform_fee_total / user_seats\n    target: TBD\n  - name: Cost per Targeted Account\n    metric: platform_fee_total / target_accounts\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.demandbase.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/demandbase/refs/heads/main/finops/demandbase-finops.yml
sources:
- https://www.demandbase.com/pricing/
- https://developer.demandbase.com/
specification: FinOps Framework
tags:
- Account-Based Marketing
- Advertising
- B2B Marketing
- Data
- FinOps
- FOCUS
---
