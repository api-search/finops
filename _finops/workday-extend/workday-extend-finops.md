---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Workday Extend REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.workday.com/extend/openapi.json
- filename: workday-extend-orchestration-openapi.yml
  format: yaml
  label: Workday Orchestration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-extend/refs/heads/main/openapi/workday-extend-orchestration-openapi.yml
- filename: workday-extend-custom-objects-openapi.yml
  format: yaml
  label: Workday Custom Objects API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-extend/refs/heads/main/openapi/workday-extend-custom-objects-openapi.yml
- filename: workday-extend-graph-api-openapi.yml
  format: yaml
  label: Workday Graph API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-extend/refs/heads/main/openapi/workday-extend-graph-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps stub for Workday Extend. Extend is sold as an add-on platform entitlement to existing Workday tenants; there is no public per-app-call price and no public usage API, so meters describe contractual entitlement rather than runtime telemetry.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: Low-Code Platform
  ServiceName: Workday Extend
layout: finops
meters:
- aggregation: max
  description: Annual Workday Extend platform entitlement attached to the parent Workday tenant subscription.
  dimensions:
  - tenant
  name: extend_entitlement
  unit: month
- aggregation: max
  description: Count of Extend apps deployed against the tenant; tracked by Workday for entitlement governance rather than per-app billing.
  dimensions:
  - tenant
  - app
  name: extend_apps_in_use
  unit: app
name: Workday Extend Finops
provider_name: Workday Extend
provider_slug: workday-extend
publisher_name: Workday, Inc.
service_category: Low-Code Platform
slug: workday-extend-finops
source_filename: workday-extend-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/enterprise-resource-planning.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Extend\nproviderId: workday-extend\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Low-Code\n  - Custom Applications\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for Workday Extend. Extend is sold as an add-on platform entitlement to existing Workday tenants; there is no public per-app-call price and no public usage API, so meters describe contractual entitlement rather than runtime telemetry.\nsources:\n  - https://www.workday.com/en-us/enterprise-resource-planning.html\nnotes: No public pricing or usage API exists. Scaffold api_request and compute meters have been removed.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Workday, Inc.\nserviceCategory: Low-Code Platform\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Extend\n  ServiceCategory: Low-Code Platform\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: extend_entitlement\n    description: Annual Workday Extend platform entitlement attached to the parent Workday tenant subscription.\n    unit: month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: extend_apps_in_use\n    description: Count of Extend apps deployed against the tenant; tracked by Workday for entitlement governance rather than per-app billing.\n    unit: app\n    aggregation: max\n    dimensions:\n      - tenant\n      - app\nprinciples:\n  - name: Visibility\n    description: Track Extend value by maintaining an inventory of deployed Extend apps and their\
  \ owners; raw API call telemetry is not exposed externally, so cost-justification relies on app-level adoption metrics.\n  - name: Allocation\n    description: Allocate the Extend entitlement back to the product or business unit that requested each app; charge incremental development effort to the sponsoring team.\n  - name: Optimization\n    description: Retire unused Extend apps before renewal, consolidate overlapping ones, and prefer configuring native Workday capability before building custom Extend apps to avoid duplicative platform spend.\n  - name: Accountability\n    description: A platform owner inside the Workday Center of Excellence should approve new Extend app builds, review utilization quarterly, and consolidate the Extend SKU into the broader Workday renewal conversation.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-extend/refs/heads/main/finops/workday-extend-finops.yml
sources:
- https://www.workday.com/en-us/enterprise-resource-planning.html
specification: FinOps Framework
tags:
- Low-Code
- Custom Applications
- FinOps
- FOCUS
---
