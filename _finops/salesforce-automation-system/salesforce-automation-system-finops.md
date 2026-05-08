---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-automation-flow-openapi.yml
  format: yaml
  label: Salesforce Flow Automation API
  slug: salesforce-flow-automation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation-system/refs/heads/main/openapi/salesforce-automation-flow-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription / Contact Sales
description: 'FOCUS-aligned FinOps shape for the Salesforce Automation System: Flow / Process / Approval / Workflow consumption is bundled into the org''s edition subscription. The financial unit is the licensed user; the binding API constraint is the per-org 24-hour request allowance.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Salesforce, Inc.
  ProviderName: Salesforce
  PublisherName: Salesforce, Inc.
  ServiceCategory: CRM / Automation
  ServiceName: Salesforce Automation System
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
  - flow
  name: flow_interviews
  unit: invocation
- aggregation: sum
  dimensions:
  - org
  - class
  name: apex_executions
  unit: transaction
name: Salesforce Automation System Finops
provider_name: Salesforce Automation System
provider_slug: salesforce-automation-system
publisher_name: Salesforce, Inc.
service_category: CRM / Automation
slug: salesforce-automation-system-finops
source_filename: salesforce-automation-system-finops.yml
source_heading: FinOps Profile
source_url: https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Salesforce Automation System\nproviderId: salesforce-automation-system\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - CRM\n  - Automation\n  - Salesforce\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for the Salesforce Automation System: Flow / Process / Approval\n  / Workflow consumption is bundled into the org''s edition subscription. The financial unit is the licensed\n  user; the binding API constraint is the per-org 24-hour request allowance.'\nsources:\n  - https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/\n  - https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm\nnotes: Per-edition prices and per-edition API allowance numbers were not retrievable for this run. The\n  shape below\
  \ describes structure, not fabricated dollar values.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Salesforce, Inc.\nserviceCategory: CRM / Automation\nbillingModel:\n  pricingCategory: Subscription / Contact Sales\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Salesforce Automation System\n  ServiceCategory: CRM / Automation\n  ProviderName: Salesforce\n  PublisherName: Salesforce, Inc.\n  InvoiceIssuerName: Salesforce, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: licensed_users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - edition\n      - cloud\n  - name: api_requests_24h\n    unit: request\n    aggregation: sum\n    dimensions:\n      - org\n      - api_family\n  - name: flow_interviews\n   \
  \ unit: invocation\n    aggregation: sum\n    dimensions:\n      - org\n      - flow\n  - name: apex_executions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - org\n      - class\nprinciples:\n  - name: Visibility\n    description: Track per-org API consumption via API Usage Last 7 Days, System Overview, and Event Monitoring.\n      Track flow interviews via Flow analytics in Setup; correlate with Apex governor metrics.\n  - name: Allocation\n    description: Allocate seat cost by org / business unit; allocate API headroom and Flow execution cost\n      back to the integrations and automations driving consumption so noisy automations don't crowd out\n      user-facing flows.\n  - name: Optimization\n    description: Migrate Process Builder / Workflow Rules to Flow; bulkify Flow + Apex; collapse per-record\n      callouts; route high-volume data through Bulk API; right-size editions at renewal; retire unused\n      flows.\n  - name: Accountability\n    description:\
  \ Salesforce CoE / admin owns license + API consumption with finance; integration owners\n      are accountable for their share of the 24-hour bucket. Set internal alerting at 60-70% of allowance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation-system/refs/heads/main/finops/salesforce-automation-system-finops.yml
sources:
- https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/
- https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm
specification: FinOps Framework
tags:
- CRM
- Automation
- Salesforce
- FinOps
- FOCUS
---
