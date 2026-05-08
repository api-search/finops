---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fullstory-server-api-openapi.yml
  format: yaml
  label: FullStory Server API
  slug: fullstory-server-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/openapi/fullstory-server-api-openapi.yml
- filename: fullstory-sessions-api-openapi.yml
  format: yaml
  label: FullStory Sessions API
  slug: fullstory-sessions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/openapi/fullstory-sessions-api-openapi.yml
- filename: fullstory-segments-export-api-openapi.yml
  format: yaml
  label: FullStory Segments Export API
  slug: fullstory-segments-export-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/openapi/fullstory-segments-export-api-openapi.yml
- filename: fullstory-webhooks-api-openapi.yml
  format: yaml
  label: FullStory Webhooks API
  slug: fullstory-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/openapi/fullstory-webhooks-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for FullStory. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: FullStory
  ProviderName: FullStory
  PublisherName: FullStory
  ServiceCategory: Analytics
  ServiceName: FullStory
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Fullstory Finops
provider_name: FullStory
provider_slug: fullstory
publisher_name: FullStory
service_category: Analytics
slug: fullstory-finops
source_filename: fullstory-finops.yml
source_heading: FinOps Profile
source_url: https://www.fullstory.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: FullStory\nproviderId: fullstory\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Analytics\n- Session Replay\n- Frontend\n- Behavioral\n- Monitoring\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for FullStory. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://www.fullstory.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: FullStory\nserviceCategory: Analytics\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: FullStory\n  ServiceCategory: Analytics\n  ProviderName: FullStory\n  PublisherName: FullStory\n  InvoiceIssuerName: FullStory\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/finops/fullstory-finops.yml
sources:
- https://www.fullstory.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Analytics
- Session Replay
- Frontend
- Behavioral
- Monitoring
- FinOps
- Cost Management
- FOCUS
---
