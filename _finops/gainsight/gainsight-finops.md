---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: gainsight-rest-api-openapi.yml
  format: yaml
  label: Gainsight REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-rest-api-openapi.yml
- filename: gainsight-px-api-openapi.yml
  format: yaml
  label: Gainsight PX API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-px-api-openapi.yml
- filename: gainsight-cs-company-api-openapi.yml
  format: yaml
  label: Gainsight CS Company API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-company-api-openapi.yml
- filename: gainsight-cs-person-api-openapi.yml
  format: yaml
  label: Gainsight CS Person API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-person-api-openapi.yml
- filename: gainsight-cs-custom-object-api-openapi.yml
  format: yaml
  label: Gainsight CS Custom Object API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-custom-object-api-openapi.yml
- filename: gainsight-cs-cta-api-openapi.yml
  format: yaml
  label: Gainsight CS CTA API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-cta-api-openapi.yml
- filename: gainsight-cs-timeline-api-openapi.yml
  format: yaml
  label: Gainsight CS Timeline API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-timeline-api-openapi.yml
- filename: gainsight-cs-success-plan-api-openapi.yml
  format: yaml
  label: Gainsight CS Success Plan API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-success-plan-api-openapi.yml
- filename: gainsight-cs-data-management-api-openapi.yml
  format: yaml
  label: Gainsight CS Data Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-data-management-api-openapi.yml
- filename: gainsight-cs-bulk-api-openapi.yml
  format: yaml
  label: Gainsight CS Bulk API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-bulk-api-openapi.yml
- filename: gainsight-cs-events-api-openapi.yml
  format: yaml
  label: Gainsight CS Events API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-events-api-openapi.yml
- filename: gainsight-cs-user-management-api-openapi.yml
  format: yaml
  label: Gainsight CS User Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-user-management-api-openapi.yml
- filename: gainsight-cs-customer-goals-api-openapi.yml
  format: yaml
  label: Gainsight CS Customer Goals API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-customer-goals-api-openapi.yml
- filename: gainsight-cs-renewal-center-api-openapi.yml
  format: yaml
  label: Gainsight CS Renewal Center API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-renewal-center-api-openapi.yml
- filename: gainsight-cs-task-and-playbook-api-openapi.yml
  format: yaml
  label: Gainsight CS Task and Playbook API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-task-and-playbook-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom Per-User Subscription
description: FOCUS-aligned FinOps for Gainsight.
focus_columns:
  BillingCurrency: USD
  ProviderName: Gainsight
  PublisherName: Gainsight
  ServiceCategory: Customer Success
  ServiceName: Gainsight
layout: finops
meters:
- aggregation: max
  name: full_users
  unit: user-month
- aggregation: max
  name: viewer_users
  unit: user-month
- aggregation: max
  name: customers_managed
  unit: customer-month
- aggregation: sum
  name: ai_automations
  unit: execution
name: Gainsight Finops
provider_name: Gainsight
provider_slug: gainsight
publisher_name: Gainsight
service_category: Customer Success
slug: gainsight-finops
source_filename: gainsight-finops.yml
source_heading: FinOps Profile
source_url: https://www.gainsight.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Gainsight\nproviderId: gainsight\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Customer Success\ndescription: FOCUS-aligned FinOps for Gainsight.\nsources:\n  - https://www.gainsight.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Gainsight\nserviceCategory: Customer Success\nbillingModel:\n  pricingCategory: Custom Per-User Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Gainsight\n  ServiceCategory: Customer Success\n  ProviderName: Gainsight\n  PublisherName: Gainsight\n  BillingCurrency: USD\nmeters:\n  - name: full_users\n    unit: user-month\n    aggregation:\
  \ max\n  - name: viewer_users\n    unit: user-month\n    aggregation: max\n  - name: customers_managed\n    unit: customer-month\n    aggregation: max\n  - name: ai_automations\n    unit: execution\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Gainsight consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/finops/gainsight-finops.yml
sources:
- https://www.gainsight.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Customer Success
---
