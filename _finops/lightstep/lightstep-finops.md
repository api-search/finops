---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi
  format: yaml
  label: Lightstep API
  slug: lightstep-api
  spec_type: OpenAPI
  url: https://docs.lightstep.com/openapi
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom Enterprise (ServiceNow)
description: FOCUS-aligned FinOps for Lightstep.
focus_columns:
  BillingCurrency: USD
  ProviderName: Lightstep
  PublisherName: Lightstep
  ServiceCategory: Observability
  ServiceName: Lightstep
layout: finops
meters:
- aggregation: sum
  name: spans_ingested
  unit: span
- aggregation: sum
  name: metrics_datapoints
  unit: datapoint
- aggregation: max
  name: user_seats
  unit: seat-month
name: Lightstep Finops
provider_name: Lightstep
provider_slug: lightstep
publisher_name: Lightstep
service_category: Observability
slug: lightstep-finops
source_filename: lightstep-finops.yml
source_heading: FinOps Profile
source_url: https://lightstep.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lightstep\nproviderId: lightstep\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability\ndescription: FOCUS-aligned FinOps for Lightstep.\nsources:\n  - https://lightstep.com/\n  - https://www.servicenow.com/products/observability.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lightstep\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Custom Enterprise (ServiceNow)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Lightstep\n  ServiceCategory: Observability\n  ProviderName: Lightstep\n  PublisherName: Lightstep\n  BillingCurrency: USD\nmeters:\n  - name: spans_ingested\n\
  \    unit: span\n    aggregation: sum\n  - name: metrics_datapoints\n    unit: datapoint\n    aggregation: sum\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Lightstep consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lightstep/refs/heads/main/finops/lightstep-finops.yml
sources:
- https://lightstep.com/
- https://www.servicenow.com/products/observability.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability
---
