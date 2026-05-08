---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: customer-io-track-api-openapi.yml
  format: yaml
  label: Customer.io Track API
  slug: track-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/customer-io/refs/heads/main/openapi/customer-io-track-api-openapi.yml
- filename: customer-io-app-api-openapi.yml
  format: yaml
  label: Customer.io App API
  slug: app-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/customer-io/refs/heads/main/openapi/customer-io-app-api-openapi.yml
- filename: customer-io-pipelines-api-openapi.yml
  format: yaml
  label: Customer.io Pipelines API
  slug: pipelines-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/customer-io/refs/heads/main/openapi/customer-io-pipelines-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Tiered Subscription + Usage Overage
description: 'FOCUS-aligned FinOps for Customer.io: tiered platform subscription with quotas on profiles and monthly emails, plus per-profile, per-1K-email, and per-100K-AI-credit overages.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Peaberry Software, Inc.
  PricingCategory: Subscription
  PricingUnit: workspace-month
  ProviderName: Customer.io
  PublisherName: Peaberry Software, Inc.
  ServiceCategory: Marketing Automation
  ServiceName: Customer.io
layout: finops
meters:
- aggregation: sum
  description: Monthly platform fee per workspace tied to plan tier
  dimensions:
  - plan
  - workspace
  name: platform_subscription
  unit: month
- aggregation: max
  description: People + objects stored in the workspace
  dimensions:
  - workspace
  - object_type
  name: profiles
  unit: profile
- aggregation: sum
  description: Outbound email sends across campaigns, broadcasts, and transactional sends
  dimensions:
  - workspace
  - campaign
  - channel
  name: emails_sent
  unit: email
- aggregation: sum
  description: AI Agent credits consumed
  dimensions:
  - workspace
  - skill
  name: ai_credits
  unit: credit
- aggregation: sum
  description: API calls against Track / App / Pipelines (not separately billed; observed for capacity)
  dimensions:
  - api
  - endpoint
  - workspace
  name: api_requests
  unit: request
name: Customer Io Finops
provider_name: Customer.io
provider_slug: customer-io
publisher_name: Peaberry Software, Inc.
service_category: Marketing Automation
slug: customer-io-finops
source_filename: customer-io-finops.yml
source_heading: FinOps Profile
source_url: https://customer.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Customer.io\nproviderId: customer-io\npublisherName: Peaberry Software, Inc.\nserviceCategory: Marketing Automation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Customer Data Platform\n  - Marketing Automation\n  - Messaging\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Customer.io: tiered platform subscription with quotas on profiles\n  and monthly emails, plus per-profile, per-1K-email, and per-100K-AI-credit overages.'\nsources:\n  - https://customer.io/pricing/\n  - https://docs.customer.io/api/\nprinciples:\n  - name: Visibility\n    description: Use the Customer.io workspace\
  \ usage dashboard, billing screen, and Pipelines audit log\n      to track profile counts, sent emails, and AI credit consumption against plan quotas.\n  - name: Allocation\n    description: Use workspaces, segments, and campaign tags to attribute messaging spend to product\n      lines, geographies, and lifecycle stages.\n  - name: Optimization\n    description: Suppress dormant profiles to stay under the 5,000-profile Essentials cap; use Pipelines\n      / CDP to dedupe before identify; route low-value sends through cheaper channels rather than email\n      overage; right-size AI credit packs.\n  - name: Accountability\n    description: Marketing-ops owns the monthly true-up against profile and email quotas; engineering\n      owns ingestion correctness so overage is real consumption rather than duplicate identify calls.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n\
  \  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Customer.io\n  ServiceCategory: Marketing Automation\n  ProviderName: Customer.io\n  PublisherName: Peaberry Software, Inc.\n  InvoiceIssuerName: Peaberry Software, Inc.\n  PricingCategory: Subscription\n  PricingUnit: workspace-month\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: platform_subscription\n    description:\
  \ Monthly platform fee per workspace tied to plan tier\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - workspace\n  - name: profiles\n    description: People + objects stored in the workspace\n    unit: profile\n    aggregation: max\n    dimensions:\n      - workspace\n      - object_type\n  - name: emails_sent\n    description: Outbound email sends across campaigns, broadcasts, and transactional sends\n    unit: email\n    aggregation: sum\n    dimensions:\n      - workspace\n      - campaign\n      - channel\n  - name: ai_credits\n    description: AI Agent credits consumed\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - workspace\n      - skill\n  - name: api_requests\n    description: API calls against Track / App / Pipelines (not separately billed; observed for capacity)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - workspace\napis:\n  - name: Customer.io Track API\n    baseURL: https://track.customer.io\n\
  \    tags:\n      - Behavioral Data\n      - Customer Data\n      - Event Tracking\n      - Marketing Automation\n      - Messaging\n    serviceName: Customer.io Track API\n    serviceCategory: API\n  - name: Customer.io App API\n    baseURL: https://api.customer.io\n    tags:\n      - Broadcasts\n      - Campaigns\n      - Marketing Automation\n      - Messaging\n      - Segments\n      - Transactional Email\n    serviceName: Customer.io App API\n    serviceCategory: API\n  - name: Customer.io Pipelines API\n    baseURL: https://cdp.customer.io\n    tags:\n      - CDP\n      - Customer Data Platform\n      - Data Ingestion\n      - Marketing Automation\n      - Messaging\n    serviceName: Customer.io Pipelines API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Profile\n    metric: billed_cost / profiles\n    target: TBD\n  - name: Cost per 1K Emails\n    metric: billed_cost / (emails_sent / 1000)\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/customer-io/refs/heads/main/finops/customer-io-finops.yml
sources:
- https://customer.io/pricing/
- https://docs.customer.io/api/
specification: FinOps Framework
tags:
- Customer Data Platform
- Marketing Automation
- Messaging
- FinOps
- Cost Management
- FOCUS
---
