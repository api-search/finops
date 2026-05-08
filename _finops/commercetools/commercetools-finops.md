---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: commercetools-http-api-openapi.yml
  format: yaml
  label: Commercetools HTTP API
  slug: http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commercetools/refs/heads/main/openapi/commercetools-http-api-openapi.yml
- filename: commercetools-import-api-openapi.yml
  format: yaml
  label: Commercetools Import API
  slug: import-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commercetools/refs/heads/main/openapi/commercetools-import-api-openapi.yml
- filename: commercetools-change-history-api-openapi.yml
  format: yaml
  label: Commercetools Change History API
  slug: change-history-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commercetools/refs/heads/main/openapi/commercetools-change-history-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom Subscription (Editions)
description: FOCUS-aligned FinOps for commercetools.
focus_columns:
  BillingCurrency: USD
  ProviderName: commercetools
  PublisherName: commercetools
  ServiceCategory: Composable Commerce
  ServiceName: commercetools
layout: finops
meters:
- aggregation: sum
  name: api_calls
  unit: call
- aggregation: max
  name: stored_skus
  unit: sku-month
- aggregation: sum
  name: orders
  unit: order
- aggregation: sum
  name: gmv
  unit: USD
- aggregation: sum
  name: audit_log_events
  unit: event
name: Commercetools Finops
provider_name: commercetools
provider_slug: commercetools
publisher_name: commercetools
service_category: Composable Commerce
slug: commercetools-finops
source_filename: commercetools-finops.yml
source_heading: FinOps Profile
source_url: https://commercetools.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: commercetools\nproviderId: commercetools\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Composable Commerce\ndescription: FOCUS-aligned FinOps for commercetools.\nsources:\n  - https://commercetools.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: commercetools\nserviceCategory: Composable Commerce\nbillingModel:\n  pricingCategory: Custom Subscription (Editions)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: commercetools\n  ServiceCategory: Composable Commerce\n  ProviderName: commercetools\n  PublisherName: commercetools\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n\
  \    unit: call\n    aggregation: sum\n  - name: stored_skus\n    unit: sku-month\n    aggregation: max\n  - name: orders\n    unit: order\n    aggregation: sum\n  - name: gmv\n    unit: USD\n    aggregation: sum\n  - name: audit_log_events\n    unit: event\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track commercetools consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/commercetools/refs/heads/main/finops/commercetools-finops.yml
sources:
- https://commercetools.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Composable Commerce
---
