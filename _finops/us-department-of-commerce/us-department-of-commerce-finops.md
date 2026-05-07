---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: commerce-gov-api-openapi.yml
  format: yaml
  label: Commerce.gov API
  slug: commercegov-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/us-department-of-commerce/refs/heads/main/openapi/commerce-gov-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories: []
  pricingCategory: Free Public Service
description: 'FinOps shape for U.S. Department of Commerce APIs: free public data services accessed through api.data.gov. There is no commercial billing surface; FinOps focuses on quota stewardship rather than dollar cost.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: U.S. Department of Commerce
  ProviderName: U.S. Department of Commerce
  PublisherName: U.S. Department of Commerce
  ServiceCategory: Government Open Data
  ServiceName: US Department of Commerce APIs
layout: finops
meters:
- aggregation: sum
  description: Requests counted against the api.data.gov per-key hourly rate-limit budget
  dimensions:
  - api_key
  - bureau
  name: api_requests
  unit: request
- aggregation: max
  description: Remaining requests in the current rolling hour, surfaced via X-RateLimit-Remaining
  name: rate_limit_remaining
  unit: request
name: Us Department Of Commerce Finops
provider_name: US Department of Commerce
provider_slug: us-department-of-commerce
publisher_name: U.S. Department of Commerce
service_category: Government Open Data
slug: us-department-of-commerce-finops
source_filename: us-department-of-commerce-finops.yml
source_heading: FinOps Profile
source_url: https://api.data.gov/docs/developer-manual/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: US Department of Commerce\nproviderId: us-department-of-commerce\npublisherName: U.S. Department of Commerce\nserviceCategory: Government Open Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Federal Government\n  - Open Data\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for U.S. Department of Commerce APIs: free public data services accessed through api.data.gov. There is no commercial billing surface; FinOps focuses on quota stewardship rather than dollar cost.'\nsources:\n  - https://api.data.gov/docs/developer-manual/\n  - https://api.data.gov/about/\nbillingModel:\n  pricingCategory: Free Public Service\n\
  \  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: US Department of Commerce APIs\n  ServiceCategory: Government Open Data\n  ProviderName: U.S. Department of Commerce\n  PublisherName: U.S. Department of Commerce\n  InvoiceIssuerName: U.S. Department of Commerce\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Requests counted against the api.data.gov per-key hourly rate-limit budget\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - bureau\n  - name: rate_limit_remaining\n    description: Remaining requests in the current rolling hour, surfaced via X-RateLimit-Remaining\n    unit: request\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track consumption via X-RateLimit-Limit and X-RateLimit-Remaining response headers from api.data.gov; there is no usage dashboard since the service is free.\n  - name: Allocation\n    description:\
  \ Allocate by issuing distinct api.data.gov API keys per team, application, or environment so request budgets are attributable.\n  - name: Optimization\n    description: Cache responses on the consumer side and request a higher per-key rate limit from api.data.gov before adding parallel keys; consider Census/NOAA bulk download endpoints when iteration over an API would burn the hourly budget.\n  - name: Accountability\n    description: Owner is the application team holding the api.data.gov key; consumers should monitor 429 OVER_RATE_LIMIT errors and review whether higher limits are warranted.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/us-department-of-commerce/refs/heads/main/finops/us-department-of-commerce-finops.yml
sources:
- https://api.data.gov/docs/developer-manual/
- https://api.data.gov/about/
specification: FinOps Framework
tags:
- Federal Government
- Open Data
- FinOps
- FOCUS
---
