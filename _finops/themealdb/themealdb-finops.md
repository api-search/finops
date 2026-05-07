---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: themealdb-openapi.yml
  format: yaml
  label: TheMealDB API
  slug: themealdb
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/themealdb/refs/heads/main/openapi/themealdb-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Free / Donation-Funded
description: FOCUS-aligned FinOps for TheMealDB.
focus_columns:
  BillingCurrency: USD
  ProviderName: TheMealDB
  PublisherName: TheMealDB
  ServiceCategory: Recipes / Open Data
  ServiceName: TheMealDB
layout: finops
meters:
- aggregation: sum
  name: api_calls
  unit: call
name: Themealdb Finops
provider_name: TheMealDB
provider_slug: themealdb
publisher_name: TheMealDB
service_category: Recipes / Open Data
slug: themealdb-finops
source_filename: themealdb-finops.yml
source_heading: FinOps Profile
source_url: https://www.themealdb.com/api.php
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TheMealDB\nproviderId: themealdb\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Recipes / Open Data\ndescription: FOCUS-aligned FinOps for TheMealDB.\nsources:\n  - https://www.themealdb.com/api.php\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TheMealDB\nserviceCategory: Recipes / Open Data\nbillingModel:\n  pricingCategory: Free / Donation-Funded\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: TheMealDB\n  ServiceCategory: Recipes / Open Data\n  ProviderName: TheMealDB\n  PublisherName: TheMealDB\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    unit: call\n    aggregation: sum\n\
  principles:\n  - name: Visibility\n    description: Track TheMealDB consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/themealdb/refs/heads/main/finops/themealdb-finops.yml
sources:
- https://www.themealdb.com/api.php
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Recipes / Open Data
---
