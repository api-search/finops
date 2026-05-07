---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: copper-developer-api-openapi.yml
  format: yaml
  label: Copper Developer API
  slug: developer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/copper/refs/heads/main/openapi/copper-developer-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription (Tiered Contacts)
description: FOCUS-aligned FinOps for Copper.
focus_columns:
  BillingCurrency: USD
  ProviderName: Copper
  PublisherName: Copper
  ServiceCategory: CRM
  ServiceName: Copper
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: max
  name: contacts
  unit: contact
- aggregation: sum
  name: workflow_executions
  unit: execution
name: Copper Finops
provider_name: Copper
provider_slug: copper
publisher_name: Copper
service_category: CRM
slug: copper-finops
source_filename: copper-finops.yml
source_heading: FinOps Profile
source_url: https://www.copper.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Copper\nproviderId: copper\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - CRM\ndescription: FOCUS-aligned FinOps for Copper.\nsources:\n  - https://www.copper.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Copper\nserviceCategory: CRM\nbillingModel:\n  pricingCategory: Per-User Subscription (Tiered Contacts)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Copper\n  ServiceCategory: CRM\n  ProviderName: Copper\n  PublisherName: Copper\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n  - name: contacts\n\
  \    unit: contact\n    aggregation: max\n  - name: workflow_executions\n    unit: execution\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Copper consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/copper/refs/heads/main/finops/copper-finops.yml
sources:
- https://www.copper.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- CRM
---
