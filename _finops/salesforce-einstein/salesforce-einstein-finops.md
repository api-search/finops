---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Einstein Vision API
  slug: ''
  spec_type: OpenAPI
  url: https://api.einstein.ai/v2/vision/openapi.json
- filename: openapi.json
  format: json
  label: Einstein Language API
  slug: ''
  spec_type: OpenAPI
  url: https://api.einstein.ai/v2/language/openapi.json
- filename: salesforce-einstein-prediction-builder-openapi.yml
  format: yaml
  label: Einstein Prediction Builder API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/openapi/salesforce-einstein-prediction-builder-openapi.yml
- filename: salesforce-einstein-discovery-openapi.yml
  format: yaml
  label: Einstein Discovery API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/openapi/salesforce-einstein-discovery-openapi.yml
- filename: salesforce-einstein-bots-openapi.yml
  format: yaml
  label: Einstein Bots API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/openapi/salesforce-einstein-bots-openapi.yml
- filename: salesforce-einstein-gpt-openapi.yml
  format: yaml
  label: Einstein GPT API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/openapi/salesforce-einstein-gpt-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription Add-On / Contact Sales
description: 'FOCUS-aligned FinOps shape for Salesforce Einstein: AI add-ons priced per Salesforce edition / Cloud / seat with generative features additionally bounded by per-add-on request budgets. The financial unit is the licensed user; the binding constraint for generative use cases is the Einstein generative request quota.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Salesforce, Inc.
  ProviderName: Salesforce
  PublisherName: Salesforce, Inc.
  ServiceCategory: AI / CRM
  ServiceName: Salesforce Einstein
layout: finops
meters:
- aggregation: max
  dimensions:
  - addon
  - cloud
  name: einstein_seats
  unit: seat
- aggregation: sum
  dimensions:
  - feature
  - org
  name: generative_requests
  unit: request
- aggregation: sum
  dimensions:
  - model
  - org
  name: predictions
  unit: prediction
name: Salesforce Einstein Finops
provider_name: Salesforce Einstein
provider_slug: salesforce-einstein
publisher_name: Salesforce, Inc.
service_category: AI / CRM
slug: salesforce-einstein-finops
source_filename: salesforce-einstein-finops.yml
source_heading: FinOps Profile
source_url: https://www.salesforce.com/products/einstein-ai-solutions/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Salesforce Einstein\nproviderId: salesforce-einstein\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - CRM\n  - AI\n  - Salesforce\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Salesforce Einstein: AI add-ons priced per Salesforce edition\n  / Cloud / seat with generative features additionally bounded by per-add-on request budgets. The financial\n  unit is the licensed user; the binding constraint for generative use cases is the Einstein generative\n  request quota.'\nsources:\n  - https://www.salesforce.com/products/einstein-ai-solutions/pricing/\n  - https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm\nnotes: Public pricing pages were not retrievable; concrete Einstein add-on prices and generative quotas\n\
  \  could not be verified for this run.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Salesforce, Inc.\nserviceCategory: AI / CRM\nbillingModel:\n  pricingCategory: Subscription Add-On / Contact Sales\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Salesforce Einstein\n  ServiceCategory: AI / CRM\n  ProviderName: Salesforce\n  PublisherName: Salesforce, Inc.\n  InvoiceIssuerName: Salesforce, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: einstein_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - addon\n      - cloud\n  - name: generative_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - feature\n      - org\n  - name: predictions\n    unit: prediction\n    aggregation: sum\n\
  \    dimensions:\n      - model\n      - org\nprinciples:\n  - name: Visibility\n    description: Track generative request consumption via the Einstein admin console and Trust Layer audit\n      logs; track core API consumption via API Usage Last 7 Days; correlate with seat-level adoption metrics.\n  - name: Allocation\n    description: Allocate Einstein add-on cost by Cloud and business unit; tag Copilot / Prompt Builder\n      generations by feature and use case so high-cost prompts can be attributed back to their owning\n      product.\n  - name: Optimization\n    description: Tune prompt templates for token efficiency; cache deterministic outputs where Trust Layer\n      policy allows; right-size add-on seats at renewal; retire low-adoption Einstein features rather\n      than auto-renewing.\n  - name: Accountability\n    description: Salesforce CoE / AI lead owns Einstein adoption with finance; product owners are accountable\n      for the Copilot / Prompt Builder workflows their\
  \ teams introduce. Surface generative quota burn\n      relative to budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-einstein/refs/heads/main/finops/salesforce-einstein-finops.yml
sources:
- https://www.salesforce.com/products/einstein-ai-solutions/pricing/
- https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm
specification: FinOps Framework
tags:
- CRM
- AI
- Salesforce
- FinOps
- FOCUS
---
