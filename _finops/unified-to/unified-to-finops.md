---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: unified-to-accounting-openapi.yaml
  format: yaml
  label: Unified.to Accounting API
  slug: accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-accounting-openapi.yaml
- filename: unified-to-marketing-openapi.yaml
  format: yaml
  label: Unified.to Advertising API
  slug: ads-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-marketing-openapi.yaml
- filename: unified-to-hr-talent-openapi.yaml
  format: yaml
  label: Unified.to Assessment API
  slug: assessment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-hr-talent-openapi.yaml
- filename: unified-to-ats-openapi.yaml
  format: yaml
  label: Unified.to ATS API
  slug: ats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-ats-openapi.yaml
- filename: unified-to-productivity-openapi.yaml
  format: yaml
  label: Unified.to Calendar & Meetings API
  slug: calendar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-productivity-openapi.yaml
- filename: unified-to-it-ops-openapi.yaml
  format: yaml
  label: Unified.to Call Center API
  slug: call-center-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-it-ops-openapi.yaml
- filename: unified-to-crm-openapi.yaml
  format: yaml
  label: Unified.to CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-crm-openapi.yaml
- filename: unified-to-commerce-openapi.yaml
  format: yaml
  label: Unified.to E-Commerce API
  slug: ecommerce-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-commerce-openapi.yaml
- filename: unified-to-hris-openapi.yaml
  format: yaml
  label: Unified.to HR & Directory API
  slug: hris-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-hris-openapi.yaml
- filename: unified-to-productivity-openapi.yaml
  format: yaml
  label: Unified.to Messaging API
  slug: messaging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-productivity-openapi.yaml
- filename: unified-to-it-ops-openapi.yaml
  format: yaml
  label: Unified.to Payments API
  slug: payment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-it-ops-openapi.yaml
- filename: unified-to-it-ops-openapi.yaml
  format: yaml
  label: Unified.to Ticketing API
  slug: ticketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-it-ops-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription with API Call Quota
description: FOCUS-aligned FinOps for Unified.to.
focus_columns:
  BillingCurrency: USD
  ProviderName: Unified.to
  PublisherName: Unified.to
  ServiceCategory: Unified API
  ServiceName: Unified.to
layout: finops
meters:
- aggregation: sum
  dimensions:
  - category
  - integration
  name: api_calls
  unit: call
- aggregation: max
  name: customer_connections
  unit: connection-month
- aggregation: sum
  name: subscription
  unit: month
name: Unified To Finops
provider_name: Unified.to
provider_slug: unified-to
publisher_name: Unified.to
service_category: Unified API
slug: unified-to-finops
source_filename: unified-to-finops.yml
source_heading: FinOps Profile
source_url: https://www.unified.to/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Unified.to\nproviderId: unified-to\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Unified API\ndescription: FOCUS-aligned FinOps for Unified.to.\nsources:\n  - https://www.unified.to/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Unified.to\nserviceCategory: Unified API\nbillingModel:\n  pricingCategory: Subscription with API Call Quota\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Unified.to\n  ServiceCategory: Unified API\n  ProviderName: Unified.to\n  PublisherName: Unified.to\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    unit: call\n    aggregation: sum\n    dimensions:\n\
  \      - category\n      - integration\n  - name: customer_connections\n    unit: connection-month\n    aggregation: max\n  - name: subscription\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Unified.to consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/finops/unified-to-finops.yml
sources:
- https://www.unified.to/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Unified API
---
