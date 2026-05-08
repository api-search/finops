---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-openapi.yml
  format: yaml
  label: Salesforce REST API
  slug: salesforce-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-openapi.yml
- filename: salesforce-bulk-api-2-openapi.yml
  format: yaml
  label: Salesforce Bulk API 2.0
  slug: salesforce-bulk-api-2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-bulk-api-2-openapi.yml
- filename: salesforce-streaming-asyncapi.yml
  format: yaml
  label: Salesforce Streaming API
  slug: salesforce-streaming-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/asyncapi/salesforce-streaming-asyncapi.yml
- filename: salesforce-platform-events-asyncapi.yml
  format: yaml
  label: Salesforce Platform Events API
  slug: salesforce-platform-events-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/asyncapi/salesforce-platform-events-asyncapi.yml
- filename: salesforce-change-data-capture-asyncapi.yml
  format: yaml
  label: Salesforce Change Data Capture API
  slug: salesforce-change-data-capture-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/asyncapi/salesforce-change-data-capture-asyncapi.yml
- filename: salesforce-ui-api-openapi.yml
  format: yaml
  label: Salesforce UI API
  slug: salesforce-ui-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-ui-api-openapi.yml
- filename: salesforce-marketing-cloud-rest-openapi.yml
  format: yaml
  label: Salesforce Marketing Cloud REST API
  slug: salesforce-marketing-cloud-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-marketing-cloud-rest-openapi.yml
- filename: salesforce-openapi.yml
  format: yaml
  label: Salesforce
  slug: salesforce-salesforce
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for Salesforce.
focus_columns:
  BillingCurrency: USD
  ProviderName: Salesforce
  PublisherName: Salesforce, Inc.
  ServiceCategory: CRM
  ServiceName: Salesforce
layout: finops
meters:
- aggregation: max
  dimensions:
  - edition
  - user_type
  name: user_licenses
  unit: license-month
- aggregation: max
  name: data_storage
  unit: MB
- aggregation: max
  name: file_storage
  unit: MB
- aggregation: sum
  dimensions:
  - api_type
  - user
  name: api_calls
  unit: call
- aggregation: sum
  name: platform_events
  unit: event
- aggregation: sum
  name: data_cloud_credits
  unit: credit
- aggregation: sum
  name: einstein_predictions
  unit: prediction
name: Salesforce Finops
provider_name: Salesforce
provider_slug: salesforce
publisher_name: Salesforce, Inc.
service_category: CRM
slug: salesforce-finops
source_filename: salesforce-finops.yml
source_heading: FinOps Profile
source_url: https://www.salesforce.com/sales/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Salesforce\nproviderId: salesforce\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - CRM\ndescription: FOCUS-aligned FinOps for Salesforce.\nsources:\n  - https://www.salesforce.com/sales/pricing/\n  - https://www.salesforce.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Salesforce, Inc.\nserviceCategory: CRM\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Salesforce\n  ServiceCategory: CRM\n  ProviderName: Salesforce\n  PublisherName: Salesforce, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: user_licenses\n    unit: license-month\n\
  \    aggregation: max\n    dimensions:\n      - edition\n      - user_type\n  - name: data_storage\n    unit: MB\n    aggregation: max\n  - name: file_storage\n    unit: MB\n    aggregation: max\n  - name: api_calls\n    unit: call\n    aggregation: sum\n    dimensions:\n      - api_type\n      - user\n  - name: platform_events\n    unit: event\n    aggregation: sum\n  - name: data_cloud_credits\n    unit: credit\n    aggregation: sum\n  - name: einstein_predictions\n    unit: prediction\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Setup > Company Information for license usage; Event Monitoring for API attribution.\n  - name: Allocation\n    description: Use Profile/Permission Set assignment to track license type by team.\n  - name: Optimization\n    description: Convert unused full users to Platform/Identity licenses; consolidate sandboxes.\n  - name: Accountability\n    description: Quarterly license audit; renegotiate at renewal based on observed active-user\
  \ count.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/finops/salesforce-finops.yml
sources:
- https://www.salesforce.com/sales/pricing/
- https://www.salesforce.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- CRM
---
