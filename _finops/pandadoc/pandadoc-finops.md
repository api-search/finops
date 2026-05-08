---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pandadoc-rest-api-openapi.yml
  format: yaml
  label: PandaDoc REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pandadoc/refs/heads/main/openapi/pandadoc-rest-api-openapi.yml
- filename: pandadoc-rest-api-openapi.yml
  format: yaml
  label: PandaDoc Document Generation API
  slug: document-generation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pandadoc/refs/heads/main/openapi/pandadoc-rest-api-openapi.yml
- filename: pandadoc-rest-api-openapi.yml
  format: yaml
  label: PandaDoc E-Signature API
  slug: e-signature-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pandadoc/refs/heads/main/openapi/pandadoc-rest-api-openapi.yml
- filename: pandadoc-rest-api-openapi.yml
  format: yaml
  label: PandaDoc Embedded Editing API
  slug: embedded-editing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pandadoc/refs/heads/main/openapi/pandadoc-rest-api-openapi.yml
- filename: pandadoc-rest-api-openapi.yml
  format: yaml
  label: PandaDoc Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pandadoc/refs/heads/main/openapi/pandadoc-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription (Per-Seat or Document-Quota)
description: FOCUS-aligned FinOps for PandaDoc.
focus_columns:
  BillingCurrency: USD
  ProviderName: PandaDoc
  PublisherName: PandaDoc
  ServiceCategory: E-Signature / Documents
  ServiceName: PandaDoc
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: documents_created
  unit: document
- aggregation: sum
  name: signature_requests
  unit: request
name: Pandadoc Finops
provider_name: PandaDoc
provider_slug: pandadoc
publisher_name: PandaDoc
service_category: E-Signature / Documents
slug: pandadoc-finops
source_filename: pandadoc-finops.yml
source_heading: FinOps Profile
source_url: https://www.pandadoc.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PandaDoc\nproviderId: pandadoc\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - E-Signature / Documents\ndescription: FOCUS-aligned FinOps for PandaDoc.\nsources:\n  - https://www.pandadoc.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PandaDoc\nserviceCategory: E-Signature / Documents\nbillingModel:\n  pricingCategory: Subscription (Per-Seat or Document-Quota)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: PandaDoc\n  ServiceCategory: E-Signature / Documents\n  ProviderName: PandaDoc\n  PublisherName: PandaDoc\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n\
  \    aggregation: max\n    dimensions:\n      - plan\n  - name: documents_created\n    unit: document\n    aggregation: sum\n  - name: signature_requests\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track PandaDoc consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pandadoc/refs/heads/main/finops/pandadoc-finops.yml
sources:
- https://www.pandadoc.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- E-Signature / Documents
---
