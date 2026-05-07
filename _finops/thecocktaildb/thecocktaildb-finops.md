---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: thecocktaildb-openapi.yml
  format: yaml
  label: TheCocktailDB API
  slug: thecocktaildb
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thecocktaildb/refs/heads/main/openapi/thecocktaildb-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Free / Donation-Funded
description: FOCUS-aligned FinOps for TheCocktailDB.
focus_columns:
  BillingCurrency: USD
  ProviderName: TheCocktailDB
  PublisherName: TheCocktailDB
  ServiceCategory: Recipes / Open Data
  ServiceName: TheCocktailDB
layout: finops
meters:
- aggregation: sum
  name: api_calls
  unit: call
name: Thecocktaildb Finops
provider_name: TheCocktailDB
provider_slug: thecocktaildb
publisher_name: TheCocktailDB
service_category: Recipes / Open Data
slug: thecocktaildb-finops
source_filename: thecocktaildb-finops.yml
source_heading: FinOps Profile
source_url: https://www.thecocktaildb.com/api.php
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TheCocktailDB\nproviderId: thecocktaildb\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Recipes / Open Data\ndescription: FOCUS-aligned FinOps for TheCocktailDB.\nsources:\n  - https://www.thecocktaildb.com/api.php\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TheCocktailDB\nserviceCategory: Recipes / Open Data\nbillingModel:\n  pricingCategory: Free / Donation-Funded\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: TheCocktailDB\n  ServiceCategory: Recipes / Open Data\n  ProviderName: TheCocktailDB\n  PublisherName: TheCocktailDB\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n   \
  \ unit: call\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track TheCocktailDB consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/thecocktaildb/refs/heads/main/finops/thecocktaildb-finops.yml
sources:
- https://www.thecocktaildb.com/api.php
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Recipes / Open Data
---
