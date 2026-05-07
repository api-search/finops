---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fastly-services-openapi.yml
  format: yaml
  label: Fastly Services API
  slug: services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-services-openapi.yml
- filename: fastly-purging-openapi.yml
  format: yaml
  label: Fastly Purging API
  slug: purging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-purging-openapi.yml
- filename: fastly-logging-openapi.yml
  format: yaml
  label: Fastly Real-Time Logging API
  slug: logging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-logging-openapi.yml
- filename: fastly-metrics-and-stats-openapi.yml
  format: yaml
  label: Fastly Metrics and Stats API
  slug: metrics-and-stats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-metrics-and-stats-openapi.yml
- filename: fastly-tls-openapi.yml
  format: yaml
  label: Fastly TLS API
  slug: tls-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-tls-openapi.yml
- filename: fastly-vcl-services-openapi.yml
  format: yaml
  label: Fastly VCL Services API
  slug: vcl-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-vcl-services-openapi.yml
- filename: fastly-account-openapi.yml
  format: yaml
  label: Fastly Account API
  slug: account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-account-openapi.yml
- filename: fastly-authentication-tokens-openapi.yml
  format: yaml
  label: Fastly Authentication Tokens API
  slug: authentication-tokens-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-authentication-tokens-openapi.yml
- filename: fastly-acls-openapi.yml
  format: yaml
  label: Fastly Access Control Lists API
  slug: acls-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-acls-openapi.yml
- filename: fastly-dictionaries-openapi.yml
  format: yaml
  label: Fastly Edge Dictionaries API
  slug: dictionaries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-dictionaries-openapi.yml
- filename: fastly-compute-openapi.yml
  format: yaml
  label: Fastly Compute API
  slug: compute-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-compute-openapi.yml
- filename: fastly-waf-openapi.yml
  format: yaml
  label: Fastly Next-Gen WAF API
  slug: waf-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-waf-openapi.yml
- filename: fastly-domain-management-openapi.yml
  format: yaml
  label: Fastly Domain Management API
  slug: domain-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-domain-management-openapi.yml
- filename: fastly-products-openapi.yml
  format: yaml
  label: Fastly Products API
  slug: products-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-products-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Usage-Based with Volume Discounts
description: FOCUS-aligned FinOps for Fastly.
focus_columns:
  BillingCurrency: USD
  ProviderName: Fastly
  PublisherName: Fastly
  ServiceCategory: Edge Network
  ServiceName: Fastly
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  name: bandwidth_delivered
  unit: GB
- aggregation: sum
  dimensions:
  - region
  name: requests_delivered
  unit: request
- aggregation: sum
  name: compute_requests
  unit: request
- aggregation: sum
  name: compute_vcpu_ms
  unit: ms
- aggregation: max
  name: object_storage
  unit: GB-month
- aggregation: sum
  name: image_optimization_requests
  unit: request
name: Fastly Finops
provider_name: fastly
provider_slug: fastly
publisher_name: Fastly
service_category: Edge Network
slug: fastly-finops
source_filename: fastly-finops.yml
source_heading: FinOps Profile
source_url: https://www.fastly.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Fastly\nproviderId: fastly\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Edge Network\ndescription: FOCUS-aligned FinOps for Fastly.\nsources:\n  - https://www.fastly.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fastly\nserviceCategory: Edge Network\nbillingModel:\n  pricingCategory: Usage-Based with Volume Discounts\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Fastly\n  ServiceCategory: Edge Network\n  ProviderName: Fastly\n  PublisherName: Fastly\n  BillingCurrency: USD\nmeters:\n  - name: bandwidth_delivered\n    unit: GB\n    aggregation: sum\n    dimensions:\n      -\
  \ region\n  - name: requests_delivered\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n  - name: compute_requests\n    unit: request\n    aggregation: sum\n  - name: compute_vcpu_ms\n    unit: ms\n    aggregation: sum\n  - name: object_storage\n    unit: GB-month\n    aggregation: max\n  - name: image_optimization_requests\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Fastly consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size tier; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/finops/fastly-finops.yml
sources:
- https://www.fastly.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Edge Network
---
