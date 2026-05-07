---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: airtable-airtable-api-openapi.yml
  format: yaml
  label: Airtable API
  slug: airtable-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-airtable-api-openapi.yml
- filename: airtable-metadata-api-openapi.yml
  format: yaml
  label: Airtable Metadata API
  slug: airtable-metadata-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-metadata-api-openapi.yml
- filename: airtable-enterprise-api-openapi.yml
  format: yaml
  label: Airtable Enterprise API
  slug: airtable-enterprise-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-enterprise-api-openapi.yml
- filename: airtable-scim-api-openapi.yml
  format: yaml
  label: Airtable SCIM API
  slug: airtable-scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-scim-api-openapi.yml
- filename: airtable-audit-logs-api-openapi.yml
  format: yaml
  label: Airtable Audit Logs API
  slug: airtable-audit-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-audit-logs-api-openapi.yml
- filename: airtable-shares-api-openapi.yml
  format: yaml
  label: Airtable Shares API
  slug: airtable-shares-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-shares-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for Airtable.
focus_columns:
  BillingCurrency: USD
  ProviderName: Airtable
  PublisherName: Airtable
  ServiceCategory: Low-Code Database
  ServiceName: Airtable
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  - workspace
  name: user_seats
  unit: seat-month
- aggregation: max
  name: bases
  unit: base-month
- aggregation: max
  name: records_total
  unit: record
- aggregation: sum
  name: automations_runs
  unit: run
name: Airtable Finops
provider_name: Airtable
provider_slug: airtable
publisher_name: Airtable
service_category: Low-Code Database
slug: airtable-finops
source_filename: airtable-finops.yml
source_heading: FinOps Profile
source_url: https://www.airtable.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Airtable\nproviderId: airtable\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Low-Code Database\ndescription: FOCUS-aligned FinOps for Airtable.\nsources:\n  - https://www.airtable.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Airtable\nserviceCategory: Low-Code Database\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Airtable\n  ServiceCategory: Low-Code Database\n  ProviderName: Airtable\n  PublisherName: Airtable\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n\
  \      - plan\n      - workspace\n  - name: bases\n    unit: base-month\n    aggregation: max\n  - name: records_total\n    unit: record\n    aggregation: max\n  - name: automations_runs\n    unit: run\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Airtable consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/finops/airtable-finops.yml
sources:
- https://www.airtable.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Low-Code Database
---
