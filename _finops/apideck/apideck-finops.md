---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: apideck-accounting-openapi.yml
  format: yaml
  label: Apideck Accounting API
  slug: accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/openapi/apideck-accounting-openapi.yml
- filename: apideck-crm-openapi.yml
  format: yaml
  label: Apideck CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/openapi/apideck-crm-openapi.yml
- filename: apideck-hris-openapi.yml
  format: yaml
  label: Apideck HRIS API
  slug: hris-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/openapi/apideck-hris-openapi.yml
- filename: ats.yml
  format: yaml
  label: Apideck ATS API
  slug: ats-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/ats.yml
- filename: apideck-file-storage-openapi.yml
  format: yaml
  label: Apideck File Storage API
  slug: file-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/openapi/apideck-file-storage-openapi.yml
- filename: ecommerce.yml
  format: yaml
  label: Apideck Ecommerce API
  slug: ecommerce-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/ecommerce.yml
- filename: pos.yml
  format: yaml
  label: Apideck POS API
  slug: pos-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/pos.yml
- filename: issue-tracking.yml
  format: yaml
  label: Apideck Issue Tracking API
  slug: issue-tracking-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/issue-tracking.yml
- filename: lead.yml
  format: yaml
  label: Apideck Lead API
  slug: lead-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/lead.yml
- filename: sms.yml
  format: yaml
  label: Apideck SMS API
  slug: sms-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/sms.yml
- filename: vault.yml
  format: yaml
  label: Apideck Vault API
  slug: vault-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/vault.yml
- filename: webhook.yml
  format: yaml
  label: Apideck Webhook API
  slug: webhook-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/webhook.yml
- filename: connector.yml
  format: yaml
  label: Apideck Connector API
  slug: connector-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/connector.yml
- filename: proxy.yml
  format: yaml
  label: Apideck Proxy API
  slug: proxy-api
  spec_type: OpenAPI
  url: https://specs.apideck.com/proxy.yml
billing_model:
  billingCurrency: EUR
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps view for Apideck. Charges are tier-based subscriptions denominated in EUR with the primary cost driver being Active Consumers (end-customers connecting third-party SaaS via Apideck) and number of Unified API categories enabled.
focus_columns:
  BillingCurrency: EUR
  ChargeCategory: Purchase
  InvoiceIssuerName: Apideck B.V.
  PricingCategory: Tiered Subscription
  ProviderName: Apideck
  PublisherName: Apideck B.V.
  ServiceCategory: Integrations / Unified API
  ServiceName: Apideck Unify
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription line for the active plan tier (Launch, Scale, Enterprise)
  dimensions:
  - plan_tier
  name: subscription_month
  unit: month
- aggregation: max
  description: Count of unique end-customer consumers (Active Consumers) using Apideck-mediated connections in the billing period; the primary tier sizing dimension.
  dimensions:
  - plan_tier
  - api_category
  name: active_consumers
  unit: consumer
- aggregation: max
  description: Number of Unified API categories enabled on the account (1 on Launch, up to 3 on Scale, unlimited on Enterprise).
  dimensions:
  - plan_tier
  name: unified_api_categories
  unit: category
- aggregation: sum
  description: Count of requests served through Apideck Unify and Proxy APIs (telemetry; not directly billed at Launch/Scale tiers).
  dimensions:
  - api_category
  - consumer
  - connector
  name: api_requests
  unit: request
- aggregation: sum
  description: Calls forwarded to downstream connectors (Salesforce, QuickBooks, HubSpot, etc.) for cost attribution against connector-specific quotas.
  dimensions:
  - connector
  - consumer
  name: connector_calls
  unit: request
name: Apideck Finops
provider_name: Apideck
provider_slug: apideck
publisher_name: Apideck B.V.
service_category: Integrations / Unified API
slug: apideck-finops
source_filename: apideck-finops.yml
source_heading: FinOps Profile
source_url: https://www.apideck.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Apideck\nproviderId: apideck\npublisherName: Apideck B.V.\nserviceCategory: Integrations / Unified API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Integrations\n  - Unified API\ndescription: FOCUS-aligned FinOps view for Apideck. Charges are tier-based subscriptions denominated in\n  EUR with the primary cost driver being Active Consumers (end-customers connecting third-party SaaS via\n  Apideck) and number of Unified API categories enabled.\nsources:\n  - https://www.apideck.com/pricing\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: EUR\n\
  \  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Apideck Unify\n  ServiceCategory: Integrations / Unified API\n  ProviderName: Apideck\n  PublisherName: Apideck B.V.\n  InvoiceIssuerName: Apideck B.V.\n  BillingCurrency: EUR\n  ChargeCategory: Purchase\n  PricingCategory: Tiered Subscription\nmeters:\n  - name: subscription_month\n    description: Monthly subscription line for the active plan tier (Launch, Scale, Enterprise)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n  - name: active_consumers\n    description: Count of unique end-customer consumers (Active Consumers) using Apideck-mediated connections\n      in the billing period; the primary tier sizing dimension.\n    unit: consumer\n    aggregation: max\n    dimensions:\n      - plan_tier\n      - api_category\n  - name: unified_api_categories\n    description: Number of Unified API categories enabled on the account (1 on Launch, up to 3 on Scale,\n\
  \      unlimited on Enterprise).\n    unit: category\n    aggregation: max\n    dimensions:\n      - plan_tier\n  - name: api_requests\n    description: Count of requests served through Apideck Unify and Proxy APIs (telemetry; not directly\n      billed at Launch/Scale tiers).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_category\n      - consumer\n      - connector\n  - name: connector_calls\n    description: Calls forwarded to downstream connectors (Salesforce, QuickBooks, HubSpot, etc.) for\n      cost attribution against connector-specific quotas.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - connector\n      - consumer\nprinciples:\n  - name: Visibility\n    description: Use the Apideck dashboard logs and Vault per-consumer usage views to attribute API call\n      counts and connector traffic per end-customer.\n  - name: Allocation\n    description: Tag spend by Active Consumer (end-customer), product line, and Unified API category.\n\
  \      Active Consumer count is the primary tier-sizing axis and should be reviewed monthly.\n  - name: Optimization\n    description: Right-size the plan against actual Active Consumers; consolidate to fewer Unified API\n      categories on Scale; switch to annual billing for the 10% discount; minimize Proxy API calls when\n      a Unified endpoint exists.\n  - name: Accountability\n    description: Integrations or Platform team owns the Apideck contract; product owners get showback\n      based on Active Consumers attributable to their product surface.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apideck/refs/heads/main/finops/apideck-finops.yml
sources:
- https://www.apideck.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Integrations
- Unified API
---
