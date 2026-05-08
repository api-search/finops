---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rapidapi-rest-platform-api-openapi.yml
  format: yaml
  label: RapidAPI REST Platform API
  slug: rapidapi-rest-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rapidapi/refs/heads/main/openapi/rapidapi-rest-platform-api-openapi.yml
- filename: rapidapi-graphql-platform-api-openapi.yml
  format: yaml
  label: RapidAPI GraphQL Platform API
  slug: rapidapi-graphql-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rapidapi/refs/heads/main/openapi/rapidapi-graphql-platform-api-openapi.yml
- filename: rapidapi-hub-api-openapi.yml
  format: yaml
  label: RapidAPI Hub API
  slug: rapidapi-hub-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rapidapi/refs/heads/main/openapi/rapidapi-hub-api-openapi.yml
- filename: rapidapi-testing-api-openapi.yml
  format: yaml
  label: RapidAPI Testing API
  slug: rapidapi-testing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rapidapi/refs/heads/main/openapi/rapidapi-testing-api-openapi.yml
- filename: rapidapi-studio-api-openapi.yml
  format: yaml
  label: RapidAPI Studio API
  slug: rapidapi-studio-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rapidapi/refs/heads/main/openapi/rapidapi-studio-api-openapi.yml
- filename: rapidapi-gateway-api-openapi.yml
  format: yaml
  label: RapidAPI Gateway API
  slug: rapidapi-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rapidapi/refs/heads/main/openapi/rapidapi-gateway-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for RapidAPI Enterprise Hub. Commercial terms are negotiated; no public price list, so meters and unit economics below are placeholders to be confirmed at contract time.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: RapidAPI (Nokia)
  ProviderName: RapidAPI
  PublisherName: RapidAPI (Nokia)
  ServiceCategory: API Management
  ServiceName: RapidAPI Enterprise Hub
layout: finops
meters:
- aggregation: sum
  description: Annual contract fee for RapidAPI Enterprise Hub
  name: enterprise_subscription
  unit: contract
name: Rapidapi Finops
provider_name: RapidAPI
provider_slug: rapidapi
publisher_name: RapidAPI (Nokia)
service_category: API Management
slug: rapidapi-finops
source_filename: rapidapi-finops.yml
source_heading: FinOps Profile
source_url: https://rapidapi.com/products/enterprise-hub
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: RapidAPI\nproviderId: rapidapi\npublisherName: RapidAPI (Nokia)\nserviceCategory: API Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - API Marketplace\n  - API Management\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for RapidAPI Enterprise Hub. Commercial terms are negotiated;\n  no public price list, so meters and unit economics below are placeholders to be confirmed at\n  contract time.\nsources:\n  - https://rapidapi.com/products/enterprise-hub\nnotes: RapidAPI Enterprise Hub is contact-sales; no usage/billing API is publicly documented for\n  reconciliation, so meter list is intentionally\
  \ minimal and FOCUS columns reflect the assumed\n  enterprise contract structure rather than a fetched billing surface.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: RapidAPI Enterprise Hub\n  ServiceCategory: API Management\n  ProviderName: RapidAPI\n  PublisherName: RapidAPI (Nokia)\n  InvoiceIssuerName: RapidAPI (Nokia)\n  BillingCurrency: USD\nmeters:\n  - name: enterprise_subscription\n    description: Annual contract fee for RapidAPI Enterprise Hub\n    unit: contract\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Until a contract is signed, no usage telemetry is exposed; once provisioned,\n      Enterprise Hub admins can pull traffic analytics from the in-product dashboard.\n  - name: Allocation\n    description: Allocate by API key and consumer team within the Enterprise Hub admin console.\n  - name: Optimization\n    description:\
  \ Negotiate volume tiers, on-prem vs SaaS, and hub consolidation at renewal; no\n      public discount schedule.\n  - name: Accountability\n    description: Procurement and platform team co-own the Enterprise Hub contract; cost is fixed\n      annual rather than usage-driven.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rapidapi/refs/heads/main/finops/rapidapi-finops.yml
sources:
- https://rapidapi.com/products/enterprise-hub
specification: FinOps Framework
tags:
- API Marketplace
- API Management
- FinOps
- FOCUS
---
