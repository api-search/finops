---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Consumption-Based (MAR)
description: FOCUS-aligned FinOps for Fivetran.
focus_columns:
  BillingCurrency: USD
  ProviderName: Fivetran
  PublisherName: Fivetran
  ServiceCategory: Data Integration
  ServiceName: Fivetran
layout: finops
meters:
- aggregation: sum
  dimensions:
  - connector
  - destination
  name: monthly_active_rows
  unit: row
- aggregation: sum
  name: transformation_runs
  unit: run
- aggregation: max
  name: active_connectors
  unit: connector-month
name: Fivetran Finops
provider_name: Fivetran
provider_slug: fivetran
publisher_name: Fivetran
service_category: Data Integration
slug: fivetran-finops
source_filename: fivetran-finops.yml
source_heading: FinOps Profile
source_url: https://www.fivetran.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Fivetran\nproviderId: fivetran\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Data Integration\ndescription: FOCUS-aligned FinOps for Fivetran.\nsources:\n  - https://www.fivetran.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fivetran\nserviceCategory: Data Integration\nbillingModel:\n  pricingCategory: Consumption-Based (MAR)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Fivetran\n  ServiceCategory: Data Integration\n  ProviderName: Fivetran\n  PublisherName: Fivetran\n  BillingCurrency: USD\nmeters:\n  - name: monthly_active_rows\n    unit: row\n    aggregation: sum\n    dimensions:\n\
  \      - connector\n      - destination\n  - name: transformation_runs\n    unit: run\n    aggregation: sum\n  - name: active_connectors\n    unit: connector-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Fivetran consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size tier; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fivetran/refs/heads/main/finops/fivetran-finops.yml
sources:
- https://www.fivetran.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Integration
---
