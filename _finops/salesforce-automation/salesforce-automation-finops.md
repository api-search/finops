---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-rest-api-openapi.json
  format: json
  label: Salesforce REST API
  slug: salesforce-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-rest-api-openapi.json
- filename: salesforce-bulk-api-openapi.json
  format: json
  label: Salesforce Bulk API 2.0
  slug: salesforce-bulk-api-20
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-bulk-api-openapi.json
- filename: salesforce-streaming-api-openapi.json
  format: json
  label: Salesforce Streaming API
  slug: salesforce-streaming-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-streaming-api-openapi.json
- filename: salesforce-platform-events-api-openapi.json
  format: json
  label: Salesforce Platform Events API
  slug: salesforce-platform-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-platform-events-api-openapi.json
- filename: salesforce-analytics-api-openapi.json
  format: json
  label: Salesforce Analytics API
  slug: salesforce-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-analytics-api-openapi.json
- filename: salesforce-tooling-api-openapi.json
  format: json
  label: Salesforce Tooling API
  slug: salesforce-tooling-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-tooling-api-openapi.json
- filename: salesforce-connect-rest-api-openapi.json
  format: json
  label: Salesforce Connect REST API
  slug: salesforce-connect-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-connect-rest-api-openapi.json
- filename: salesforce-change-data-capture-api-openapi.json
  format: json
  label: Salesforce Change Data Capture API
  slug: salesforce-change-data-capture-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-change-data-capture-api-openapi.json
- filename: salesforce-invocable-actions-api-openapi.json
  format: json
  label: Salesforce Invocable Actions API
  slug: salesforce-invocable-actions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-invocable-actions-api-openapi.json
- filename: salesforce-composite-api-openapi.json
  format: json
  label: Salesforce Composite API
  slug: salesforce-composite-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-composite-api-openapi.json
- filename: salesforce-apex-rest-api-openapi.json
  format: json
  label: Salesforce Apex REST API
  slug: salesforce-apex-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-apex-rest-api-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription / Contact Sales
description: 'FOCUS-aligned FinOps shape for Salesforce-driven automation: edition-based per-user-per-month subscription with API consumption bounded by a per-org 24-hour allowance and Apex governor limits. The financial unit of consumption is the licensed user, not the API request, though API headroom can become the binding constraint for automation-heavy orgs.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Salesforce, Inc.
  ProviderName: Salesforce
  PublisherName: Salesforce, Inc.
  ServiceCategory: CRM
  ServiceName: Salesforce
layout: finops
meters:
- aggregation: max
  dimensions:
  - edition
  - cloud
  name: licensed_users
  unit: seat
- aggregation: sum
  dimensions:
  - org
  - api_family
  name: api_requests_24h
  unit: request
- aggregation: sum
  dimensions:
  - org
  - class
  name: apex_executions
  unit: transaction
name: Salesforce Automation Finops
provider_name: Salesforce Automation
provider_slug: salesforce-automation
publisher_name: Salesforce, Inc.
service_category: CRM / Automation
slug: salesforce-automation-finops
source_filename: salesforce-automation-finops.yml
source_heading: FinOps Profile
source_url: https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Salesforce Automation\nproviderId: salesforce-automation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - CRM\n  - Automation\n  - B2B\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Salesforce-driven automation: edition-based per-user-per-month\n  subscription with API consumption bounded by a per-org 24-hour allowance and Apex governor limits. The\n  financial unit of consumption is the licensed user, not the API request, though API headroom can become\n  the binding constraint for automation-heavy orgs.'\nsources:\n  - https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/\n  - https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm\nnotes: Per-edition prices and per-edition API allowance\
  \ numbers were not retrievable for this run. The\n  FinOps shape below describes the structure rather than fabricated dollar values.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Salesforce, Inc.\nserviceCategory: CRM / Automation\nbillingModel:\n  pricingCategory: Subscription / Contact Sales\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Salesforce\n  ServiceCategory: CRM\n  ProviderName: Salesforce\n  PublisherName: Salesforce, Inc.\n  InvoiceIssuerName: Salesforce, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: licensed_users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - edition\n      - cloud\n  - name: api_requests_24h\n    unit: request\n    aggregation: sum\n    dimensions:\n      - org\n \
  \     - api_family\n  - name: apex_executions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - org\n      - class\nprinciples:\n  - name: Visibility\n    description: Use the API Usage Last 7 Days report and System Overview page in Setup to track per-org\n      API consumption against the 24-hour allowance; correlate with Apex CPU and DML governor metrics\n      via Event Monitoring.\n  - name: Allocation\n    description: Allocate seat cost by org and business unit; allocate API headroom cost back to the integrations\n      and Flow / Apex automations consuming the bucket so noisy integrations don't crowd out user-facing\n      flows.\n  - name: Optimization\n    description: Move bulk loads to Bulk API; bulkify Apex; consolidate poll-based integrations onto Pub/Sub\n      / Streaming; avoid per-record automation that fans out into callouts; right-size license counts\n      and editions at renewal.\n  - name: Accountability\n    description: Salesforce admin / CoE\
  \ owns license + API consumption with finance. Surface API usage\n      headroom to integration owners; trigger reviews when sustained 24-hour consumption exceeds an internal\n      threshold (commonly 60-70% of allowance).\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/finops/salesforce-automation-finops.yml
sources:
- https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/
- https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm
specification: FinOps Framework
tags:
- CRM
- Automation
- B2B
- FinOps
- FOCUS
---
