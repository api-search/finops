---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: national-renewable-energy-laboratory-openapi.yml
  format: yaml
  label: NREL Developer Network
  slug: nrel-developer-network
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/national-renewable-energy-laboratory/refs/heads/main/openapi/national-renewable-energy-laboratory-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories:
  - Usage
  pricingCategory: Free / Public Good
description: 'FOCUS-aligned FinOps for NREL APIs: free public-good developer network funded by the U.S. Department of Energy. No invoiced charges; the only meaningful FinOps signal is request volume per key against the 1,000/hour gateway cap.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (no invoicing)
  ProviderName: National Renewable Energy Laboratory
  PublisherName: Alliance for Sustainable Energy, LLC
  ServiceCategory: Open Data / Energy
  ServiceName: NREL Developer Network
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - api_key
  name: api_requests
  unit: request
- aggregation: count
  dimensions:
  - api_key
  - api
  name: ratelimit_blocks
  unit: event
- aggregation: sum
  dimensions:
  - source_ip
  - api
  name: demo_key_requests
  unit: request
name: National Renewable Energy Laboratory Finops
provider_name: National Renewable Energy Laboratory
provider_slug: national-renewable-energy-laboratory
publisher_name: Alliance for Sustainable Energy, LLC (operating NREL for the U.S. Department of Energy)
service_category: Open Data / Public Sector / Energy
slug: national-renewable-energy-laboratory-finops
source_filename: national-renewable-energy-laboratory-finops.yml
source_heading: FinOps Profile
source_url: https://developer.nlr.gov/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: National Renewable Energy Laboratory\nproviderId: national-renewable-energy-laboratory\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Government\n  - Energy\n  - Open Data\ndescription: 'FOCUS-aligned FinOps for NREL APIs: free public-good developer network funded by the U.S.\n  Department of Energy. No invoiced charges; the only meaningful FinOps signal is request volume per\n  key against the 1,000/hour gateway cap.'\nsources:\n  - https://developer.nlr.gov/\n  - https://developer.nlr.gov/docs/rate-limits/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Alliance for Sustainable Energy, LLC (operating NREL for the U.S. Department\
  \ of Energy)\nserviceCategory: Open Data / Public Sector / Energy\nbillingModel:\n  pricingCategory: Free / Public Good\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: NREL Developer Network\n  ServiceCategory: Open Data / Energy\n  ProviderName: National Renewable Energy Laboratory\n  PublisherName: Alliance for Sustainable Energy, LLC\n  InvoiceIssuerName: N/A (no invoicing)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - api_key\n  - name: ratelimit_blocks\n    unit: event\n    aggregation: count\n    dimensions:\n      - api_key\n      - api\n  - name: demo_key_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - source_ip\n      - api\nprinciples:\n  - name: Visibility\n    description: Inspect X-RateLimit-Limit and X-RateLimit-Remaining on every NREL API response; alert\n      consumers\
  \ approaching the 1,000/hour cap before they hit 429.\n  - name: Allocation\n    description: Issue a distinct NREL API key per consuming application or research workstream; aggregate\n      rate-limit telemetry by key for showback (no chargeback applies — there is no charge).\n  - name: Optimization\n    description: Cache slow-changing datasets (utility rates, alternative fuel stations) and pre-compute\n      PVWatts results when the inputs are stable; never use DEMO_KEY for production workloads.\n  - name: Accountability\n    description: Each consuming team owns its API key and migrates from developer.nrel.gov to developer.nlr.gov\n      before the May 2026 retirement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/national-renewable-energy-laboratory/refs/heads/main/finops/national-renewable-energy-laboratory-finops.yml
sources:
- https://developer.nlr.gov/
- https://developer.nlr.gov/docs/rate-limits/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Government
- Energy
- Open Data
---
