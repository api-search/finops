---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: chainlens-openapi.yml
  format: yaml
  label: Chainlens Blockchain Explorer API
  slug: chainlens-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chainlens/refs/heads/main/openapi/chainlens-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Free / Donation-Funded
description: FOCUS-aligned FinOps for Chainlens.
focus_columns:
  BillingCurrency: USD
  ProviderName: Chainlens
  PublisherName: Chainlens
  ServiceCategory: Blockchain Analytics
  ServiceName: Chainlens
layout: finops
meters:
- aggregation: sum
  name: api_calls
  unit: call
name: Chainlens Finops
provider_name: Chainlens
provider_slug: chainlens
publisher_name: Chainlens
service_category: Blockchain Analytics
slug: chainlens-finops
source_filename: chainlens-finops.yml
source_heading: FinOps Profile
source_url: https://chainlens.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Chainlens\nproviderId: chainlens\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Blockchain Analytics\ndescription: FOCUS-aligned FinOps for Chainlens.\nsources:\n  - https://chainlens.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Chainlens\nserviceCategory: Blockchain Analytics\nbillingModel:\n  pricingCategory: Free / Donation-Funded\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Chainlens\n  ServiceCategory: Blockchain Analytics\n  ProviderName: Chainlens\n  PublisherName: Chainlens\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    unit: call\n    aggregation: sum\nprinciples:\n\
  \  - name: Visibility\n    description: Track Chainlens consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chainlens/refs/heads/main/finops/chainlens-finops.yml
sources:
- https://chainlens.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Blockchain Analytics
---
