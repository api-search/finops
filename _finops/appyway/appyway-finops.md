---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: appyway-availability-realtime-api-openapi.yml
  format: yaml
  label: AppyWay Availability RealTime API
  slug: appyway-availability-realtime-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appyway/refs/heads/main/openapi/appyway-availability-realtime-api-openapi.yml
- filename: appyway-traffic-data-api-openapi.yml
  format: yaml
  label: AppyWay Traffic Data API
  slug: appyway-traffic-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appyway/refs/heads/main/openapi/appyway-traffic-data-api-openapi.yml
- filename: appyway-explorer-api-openapi.yml
  format: yaml
  label: AppyWay Explorer API
  slug: appyway-explorer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appyway/refs/heads/main/openapi/appyway-explorer-api-openapi.yml
- filename: appyway-platform-api-openapi.yml
  format: yaml
  label: AppyWay Platform API
  slug: appyway-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appyway/refs/heads/main/openapi/appyway-platform-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom / Contract
description: FOCUS-aligned FinOps placeholder for AppyWay. No public billing-model details, meters, or invoice schema are published; this artifact records the absence so consumers know to source commercial terms from the provider directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AppyWay Limited
  ProviderName: AppyWay
  PublisherName: AppyWay Limited
  ServiceCategory: Urban Mobility / Parking Data
  ServiceName: AppyWay
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line items once an invoice or usage schema is available.
  dimensions:
  - contract
  - consumer
  name: contract_usage
  unit: varies
name: Appyway Finops
provider_name: AppyWay
provider_slug: appyway
publisher_name: AppyWay Limited
service_category: Mobility Data
slug: appyway-finops
source_filename: appyway-finops.yml
source_heading: FinOps Profile
source_url: https://www.appyway.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AppyWay\nproviderId: appyway\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Parking\n- Traffic\n- Urban Mobility\n- Smart Cities\n- EV Charging\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for AppyWay. No public billing-model details, meters, or\n  invoice schema are published; this artifact records the absence so consumers know to source commercial\n  terms from the provider directly.\nnotes: AppyWay does not publish public pricing for its Availability, Traffic Data, Explorer, or Platform\n  APIs. Commercial access is arranged through direct sales — the docs portal is open but plan tiers, per-call\n  rates, and quotas are not disclosed.\nsources:\n- https://www.appyway.com\n- https://focus.finops.org/focus-specification/v1-3/\n- https://docs.appyway.com\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AppyWay Limited\nserviceCategory: Mobility Data\nbillingModel:\n  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: AppyWay\n  ServiceCategory: Urban Mobility / Parking Data\n  ProviderName: AppyWay\n  PublisherName: AppyWay Limited\n  InvoiceIssuerName: AppyWay Limited\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: contract_usage\n  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line\n    items once an invoice or usage schema is available.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - contract\n  - consumer\nprinciples:\n- name: Visibility\n  description: Because the provider does not publish\
  \ a usage API or self-serve billing dashboard, request\n    invoice copies and contract usage exports directly from the account team and load them into your own\n    FinOps tooling.\n- name: Allocation\n  description: Allocate spend by tagging invoice line items to consuming business units in your ERP /\n    FinOps store; no provider-side tagging surface is available.\n- name: Optimization\n  description: Optimization levers are commercial — renegotiate volume commitments, consolidate accounts,\n    or align contract scope with actual usage at renewal.\n- name: Accountability\n  description: Assign a contract owner who reviews invoices against the negotiated agreement, since usage\n    drift cannot be detected from a published meter feed.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/appyway/refs/heads/main/finops/appyway-finops.yml
sources:
- https://www.appyway.com
- https://focus.finops.org/focus-specification/v1-3/
- https://docs.appyway.com
specification: FinOps Framework
tags:
- Parking
- Traffic
- Urban Mobility
- Smart Cities
- EV Charging
- FinOps
- Cost Management
- FOCUS
---
