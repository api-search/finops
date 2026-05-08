---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: snaplogic-public-apis-openapi.yml
  format: yaml
  label: SnapLogic Public APIs
  slug: snaplogic-public-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snaplogic/refs/heads/main/openapi/snaplogic-public-apis-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription (Contact Sales)
description: 'FOCUS-aligned FinOps placeholder for SnapLogic: pricing is contact-sales only, so meter units and FOCUS columns are scoped to what is publicly known about the Intelligent Integration Platform.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SnapLogic, Inc.
  ProviderName: SnapLogic
  PublisherName: SnapLogic, Inc.
  ServiceCategory: Integration Platform
  ServiceName: SnapLogic Intelligent Integration Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - environment
  - snaplex
  name: snap_executions
  unit: varies
- aggregation: count
  dimensions:
  - environment
  - project
  name: pipeline_runs
  unit: run
name: Snaplogic Finops
provider_name: SnapLogic
provider_slug: snaplogic
publisher_name: SnapLogic, Inc.
service_category: Integration Platform
slug: snaplogic-finops
source_filename: snaplogic-finops.yml
source_heading: FinOps Profile
source_url: https://www.snaplogic.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SnapLogic\nproviderId: snaplogic\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - iPaaS\n  - Integration\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for SnapLogic: pricing is contact-sales only, so meter\n  units and FOCUS columns are scoped to what is publicly known about the Intelligent Integration Platform.'\nsources:\n  - https://www.snaplogic.com/products\nnotes: SnapLogic does not publish a per-Snap or per-pipeline price list, so meter unit prices and FOCUS\n  PricingUnit values cannot be reconciled here. Update once a customer order form or public price sheet\n  is available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ SnapLogic, Inc.\nserviceCategory: Integration Platform\nbillingModel:\n  pricingCategory: Subscription (Contact Sales)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: SnapLogic Intelligent Integration Platform\n  ServiceCategory: Integration Platform\n  ProviderName: SnapLogic\n  PublisherName: SnapLogic, Inc.\n  InvoiceIssuerName: SnapLogic, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: snap_executions\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - environment\n      - snaplex\n  - name: pipeline_runs\n    unit: run\n    aggregation: count\n    dimensions:\n      - environment\n      - project\nprinciples:\n  - name: Visibility\n    description: Use SnapLogic Manager dashboards and the SnapLogic monitoring API to track Snap executions\n      and pipeline runs per project and environment.\n  - name: Allocation\n    description: Map SnapLogic projects, organizations, and Snaplex\
  \ nodes to internal cost centers; tag\n      pipelines so usage can be attributed back to the consuming team.\n  - name: Optimization\n    description: Right-size Snaplex node count, consolidate low-volume pipelines, and use scheduled vs.\n      ultra pipelines deliberately to control execution cost.\n  - name: Accountability\n    description: Identify a tenant administrator responsible for reconciling SnapLogic invoices against\n      monitored Snap execution volume each billing period.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/snaplogic/refs/heads/main/finops/snaplogic-finops.yml
sources:
- https://www.snaplogic.com/products
specification: FinOps Framework
tags:
- iPaaS
- Integration
- FinOps
- FOCUS
---
