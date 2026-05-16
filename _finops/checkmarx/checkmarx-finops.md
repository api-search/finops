---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: 34965-8158-rest-api.html
  format: yaml
  label: Checkmarx SAST API
  slug: checkmarx-sast-api
  spec_type: OpenAPI
  url: https://checkmarx.com/resource/documents/en/34965-8158-rest-api.html
- filename: checkmarx-sca-openapi.yml
  format: yaml
  label: Checkmarx SCA API
  slug: checkmarx-sca-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkmarx/refs/heads/main/openapi/checkmarx-sca-openapi.yml
- filename: checkmarx-one-openapi.yml
  format: yaml
  label: Checkmarx One API
  slug: checkmarx-one-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkmarx/refs/heads/main/openapi/checkmarx-one-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps framing for Checkmarx One: tiered enterprise subscriptions priced by tenant tier, scanner coverage, contributing developer counts, and scan volume; pricing is custom-quoted and not publicly listed.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Checkmarx Ltd.
  ProviderName: Checkmarx
  PublisherName: Checkmarx Ltd.
  ServiceCategory: Application Security
  ServiceName: Checkmarx One
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  name: tenant_subscription
  unit: tenant-year
- aggregation: max
  name: contributing_developers
  unit: developer
- aggregation: max
  name: projects_scanned
  unit: project
- aggregation: sum
  dimensions:
  - engine
  name: scans_executed
  unit: scan
- aggregation: sum
  dimensions:
  - engine
  name: lines_of_code
  unit: LOC
name: Checkmarx Finops
provider_name: Checkmarx
provider_slug: checkmarx
publisher_name: Checkmarx Ltd.
service_category: Application Security
slug: checkmarx-finops
source_filename: checkmarx-finops.yml
source_heading: FinOps Profile
source_url: https://checkmarx.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Checkmarx\nproviderId: checkmarx\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Application Security\n  - DevSecOps\ndescription: 'FOCUS-aligned FinOps framing for Checkmarx One: tiered enterprise subscriptions priced\n  by tenant tier, scanner coverage, contributing developer counts, and scan volume; pricing is custom-quoted\n  and not publicly listed.'\nnotes: Per-call API pricing is not separately metered; cost driven by subscription tier plus contributing-developer\n  / project counts.\nsources:\n  - https://checkmarx.com/pricing/\n  - https://checkmarx.com/product/checkmarx-one/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Checkmarx Ltd.\nserviceCategory: Application Security\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Checkmarx One\n  ServiceCategory: Application Security\n  ProviderName: Checkmarx\n  PublisherName: Checkmarx Ltd.\n  InvoiceIssuerName: Checkmarx Ltd.\n  BillingCurrency: USD\nmeters:\n  - name: tenant_subscription\n    unit: tenant-year\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: contributing_developers\n    unit: developer\n    aggregation: max\n  - name: projects_scanned\n    unit: project\n    aggregation: max\n  - name: scans_executed\n    unit: scan\n    aggregation: sum\n    dimensions:\n      - engine\n  - name: lines_of_code\n    unit: LOC\n    aggregation: sum\n    dimensions:\n      - engine\nprinciples:\n  - name: Visibility\n    description: Use the Checkmarx One admin console and the\
  \ REST analytics endpoints for scan volume,\n      contributing-developer counts, and engine breakdowns; reconcile against contract entitlements.\n  - name: Allocation\n    description: Tag projects and applications with team / business-unit metadata; allocate subscription\n      cost by contributing-developer attribution.\n  - name: Optimization\n    description: Tune scan triggers (incremental scans, PR-only) to reduce runaway scan volume; right-size\n      tier to actual scanner usage and prune unused engines.\n  - name: Accountability\n    description: AppSec / DevSecOps team owns the Checkmarx subscription; review developer attribution\n      and scan volume monthly to forecast renewal sizing.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkmarx/refs/heads/main/finops/checkmarx-finops.yml
sources:
- https://checkmarx.com/pricing/
- https://checkmarx.com/product/checkmarx-one/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Application Security
- DevSecOps
---
