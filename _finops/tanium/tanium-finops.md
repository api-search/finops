---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tanium-platform-rest-api-openapi.yml
  format: yaml
  label: Tanium Platform REST API
  slug: platform-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tanium/refs/heads/main/openapi/tanium-platform-rest-api-openapi.yml
- filename: tanium-threat-response-api-openapi.yml
  format: yaml
  label: Tanium Threat Response API
  slug: threat-response-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tanium/refs/heads/main/openapi/tanium-threat-response-api-openapi.yml
- filename: tanium-connect-api-openapi.yml
  format: yaml
  label: Tanium Connect API
  slug: connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tanium/refs/heads/main/openapi/tanium-connect-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Custom / Contact Sales
description: FinOps placeholder for Tanium. Subscription is sized by endpoint count and selected modules; no public per-meter rate card is published.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tanium Inc.
  ProviderName: Tanium
  PublisherName: Tanium Inc.
  ServiceCategory: Endpoint Management
  ServiceName: Tanium
layout: finops
meters:
- aggregation: max
  dimensions:
  - module
  name: endpoint_subscription
  unit: endpoint
name: Tanium Finops
provider_name: Tanium
provider_slug: tanium
publisher_name: Tanium Inc.
service_category: Endpoint Management
slug: tanium-finops
source_filename: tanium-finops.yml
source_heading: FinOps Profile
source_url: https://www.tanium.com/products/tanium-platform/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tanium\nproviderId: tanium\npublisherName: Tanium Inc.\nserviceCategory: Endpoint Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Endpoint Management\n  - Security\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Tanium. Subscription is sized by endpoint count and selected\n  modules; no public per-meter rate card is published.\nsources:\n  - https://www.tanium.com/products/tanium-platform/\nnotes: No public billing surface. Meter list reflects the dominant unit of consumption (endpoints)\n  but exact rate is not publicly disclosed.\nbillingModel:\n  pricingCategory: Custom / Contact Sales\n  billingFrequency:\
  \ Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Tanium\n  ServiceCategory: Endpoint Management\n  ProviderName: Tanium\n  PublisherName: Tanium Inc.\n  InvoiceIssuerName: Tanium Inc.\n  BillingCurrency: USD\nmeters:\n  - name: endpoint_subscription\n    unit: endpoint\n    aggregation: max\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n    description: Endpoint and module consumption is visible in the Tanium console; cost-side\n      visibility lives in the customer's procurement records against the Tanium subscription\n      invoice.\n  - name: Allocation\n    description: Allocation is performed by tagging endpoints to business units inside Tanium and\n      reconciling against the subscription line items.\n  - name: Optimization\n    description: Optimization levers include module right-sizing, retiring unused modules at renewal,\n      and consolidating endpoint coverage.\n  - name: Accountability\n    description:\
  \ Accountability sits with the security or endpoint operations team that owns the\n      Tanium subscription.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tanium/refs/heads/main/finops/tanium-finops.yml
sources:
- https://www.tanium.com/products/tanium-platform/
specification: FinOps Framework
tags:
- Endpoint Management
- Security
- FinOps
- FOCUS
---
