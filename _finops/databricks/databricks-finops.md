---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: databricks-openapi.yml
  format: yaml
  label: Databricks Clusters API
  slug: clusters-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/openapi/databricks-openapi.yml
- filename: databricks-openapi.yml
  format: yaml
  label: Databricks Jobs API
  slug: jobs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/openapi/databricks-openapi.yml
- filename: databricks-openapi.yml
  format: yaml
  label: Databricks Workspace API
  slug: workspace-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/openapi/databricks-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: DBU-Based + Cloud Infrastructure
description: FOCUS-aligned FinOps for Databricks.
focus_columns:
  BillingCurrency: USD
  ProviderName: Databricks
  PublisherName: Databricks
  ServiceCategory: Data Lakehouse
  ServiceName: Databricks
layout: finops
meters:
- aggregation: sum
  dimensions:
  - workload_type
  - edition
  - cloud
  name: dbu_consumed
  unit: DBU
- aggregation: sum
  dimensions:
  - instance_type
  name: vm_hours
  unit: hour
- aggregation: max
  name: storage
  unit: GB-month
- aggregation: sum
  name: data_egress
  unit: GB
- aggregation: sum
  name: model_serving_endpoints
  unit: endpoint-hour
name: Databricks Finops
provider_name: Databricks
provider_slug: databricks
publisher_name: Databricks
service_category: Data Lakehouse
slug: databricks-finops
source_filename: databricks-finops.yml
source_heading: FinOps Profile
source_url: https://www.databricks.com/product/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Databricks\nproviderId: databricks\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Data Lakehouse\ndescription: FOCUS-aligned FinOps for Databricks.\nsources:\n  - https://www.databricks.com/product/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Databricks\nserviceCategory: Data Lakehouse\nbillingModel:\n  pricingCategory: DBU-Based + Cloud Infrastructure\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Databricks\n  ServiceCategory: Data Lakehouse\n  ProviderName: Databricks\n  PublisherName: Databricks\n  BillingCurrency: USD\nmeters:\n  - name: dbu_consumed\n    unit: DBU\n    aggregation:\
  \ sum\n    dimensions:\n      - workload_type\n      - edition\n      - cloud\n  - name: vm_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - instance_type\n  - name: storage\n    unit: GB-month\n    aggregation: max\n  - name: data_egress\n    unit: GB\n    aggregation: sum\n  - name: model_serving_endpoints\n    unit: endpoint-hour\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Databricks consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/finops/databricks-finops.yml
sources:
- https://www.databricks.com/product/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Lakehouse
---
