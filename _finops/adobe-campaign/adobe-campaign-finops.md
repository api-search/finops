---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-campaign-standard-openapi-original.yml
  format: yaml
  label: Adobe Campaign Standard API
  slug: standard-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-campaign/refs/heads/main/openapi/adobe-campaign-standard-openapi-original.yml
- filename: adobe-campaign-classic-openapi-original.yml
  format: yaml
  label: Adobe Campaign Classic API
  slug: classic-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-campaign/refs/heads/main/openapi/adobe-campaign-classic-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: 'FOCUS-aligned FinOps shape for Adobe Campaign: enterprise contract licensing keyed to active profile count, channels enabled, and annual message-volume commit. API access is included.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Marketing Automation
  ServiceName: Adobe Campaign
layout: finops
meters:
- aggregation: max
  description: Marketable profiles tracked against the contracted profile commit
  dimensions:
  - segment
  - region
  name: active_profiles
  unit: profile-month
- aggregation: sum
  description: Outbound messages across all channels (email, SMS, push, direct mail)
  dimensions:
  - channel
  - campaign
  name: messages_sent
  unit: message
- aggregation: sum
  description: Campaign workflow runs (used for capacity planning, not billed separately)
  name: workflow_executions
  unit: execution
name: Adobe Campaign Finops
provider_name: Adobe Campaign
provider_slug: adobe-campaign
publisher_name: Adobe Inc.
service_category: Marketing Automation
slug: adobe-campaign-finops
source_filename: adobe-campaign-finops.yml
source_heading: FinOps Profile
source_url: https://business.adobe.com/products/campaign/adobe-campaign.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Campaign\nproviderId: adobe-campaign\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Marketing\n  - Campaign Management\nnotes: >-\n  Adobe Campaign pricing is contract-specific. FinOps levers focus on profile\n  hygiene, channel mix optimization, and message-volume forecasting against\n  the annual commit.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe Campaign: enterprise contract\n  licensing keyed to active profile count, channels enabled, and annual\n  message-volume commit. API access is included.\nsources:\n  - https://business.adobe.com/products/campaign/adobe-campaign.html\n  - https://developer.adobe.com/campaign-standard-apis/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\nserviceCategory: Marketing Automation\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Adobe Campaign\n  ServiceCategory: Marketing Automation\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: active_profiles\n    description: Marketable profiles tracked against the contracted profile commit\n    unit: profile-month\n    aggregation: max\n    dimensions:\n      - segment\n      - region\n  - name: messages_sent\n    description: Outbound messages across all channels (email, SMS, push, direct mail)\n    unit: message\n    aggregation: sum\n    dimensions:\n      - channel\n      - campaign\n  - name: workflow_executions\n    description: Campaign workflow\
  \ runs (used for capacity planning, not billed separately)\n    unit: execution\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Adobe Campaign Reporting workspace and the message-volume\n      dashboard to track consumption against the contracted commit.\n  - name: Allocation\n    description: >-\n      Tag campaigns and workflows with brand / business-unit metadata so\n      message volume rolls up to the consuming team.\n  - name: Optimization\n    description: >-\n      Suppress dormant profiles to reduce profile commit; consolidate\n      send-time-optimization windows; deduplicate cross-channel pressure\n      and reduce send frequency to lower volume against commit.\n  - name: Accountability\n    description: >-\n      Marketing Ops owns the active-profile and message-volume commit;\n      Adobe TAM runs quarterly business reviews against the contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-campaign/refs/heads/main/finops/adobe-campaign-finops.yml
sources:
- https://business.adobe.com/products/campaign/adobe-campaign.html
- https://developer.adobe.com/campaign-standard-apis/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Marketing
- Campaign Management
---
