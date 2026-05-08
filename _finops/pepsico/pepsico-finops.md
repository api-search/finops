---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pepsico-pepsico-api-openapi.yml
  format: yaml
  label: PepsiCo API
  slug: pepsico-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pepsico/refs/heads/main/openapi/pepsico-pepsico-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: PepsiCo is not a software / API vendor; it is a food and beverage company. From a FinOps perspective, there is no metered API SKU. Any spend related to PepsiCo integration is the consuming partner's own infrastructure and middleware (EDI, integration platform) cost, plus any contracted integration fees.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  ProviderName: PepsiCo
  PublisherName: PepsiCo, Inc.
  ServiceCategory: B2B Integration
  ServiceName: PepsiCo Partner Integration
layout: finops
meters:
- aggregation: count
  description: Negotiated B2B / EDI integration relationship between PepsiCo and a partner. No per-unit metering published.
  dimensions:
  - partner_type
  - business_unit
  name: integration_contract
  unit: contract
name: Pepsico Finops
provider_name: PepsiCo
provider_slug: pepsico
publisher_name: PepsiCo, Inc.
service_category: B2B Integration
slug: pepsico-finops
source_filename: pepsico-finops.yml
source_heading: FinOps Profile
source_url: https://www.pepsico.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PepsiCo\nproviderId: pepsico\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - B2B\n  - Supply Chain\nnotes: PepsiCo does not sell APIs or platform services as a self-service product. There is no public\n  invoice surface to model. This artifact captures the FinOps shape only at the contract level for\n  partner / B2B integration spend.\ndescription: PepsiCo is not a software / API vendor; it is a food and beverage company. From a\n  FinOps perspective, there is no metered API SKU. Any spend related to PepsiCo integration is the\n  consuming partner's own infrastructure and middleware (EDI, integration platform) cost, plus any\n  contracted integration fees.\nsources:\n  - https://www.pepsico.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PepsiCo, Inc.\nserviceCategory: B2B Integration\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: PepsiCo Partner Integration\n  ServiceCategory: B2B Integration\n  ProviderName: PepsiCo\n  PublisherName: PepsiCo, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: integration_contract\n    description: Negotiated B2B / EDI integration relationship between PepsiCo and a partner. No\n      per-unit metering published.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - partner_type\n      - business_unit\nprinciples:\n  - name: Visibility\n    description: Track integration spend at the contract level; visibility into per-transaction cost\n      depends on what the partner agreement specifies.\n  - name: Allocation\n\
  \    description: Allocate the integration contract cost to the consuming line of business (retail,\n      foodservice, supply chain).\n  - name: Optimization\n    description: Consolidate redundant point-to-point integrations under a single managed file\n      transfer or EDI VAN to reduce middleware overhead.\n  - name: Accountability\n    description: The PepsiCo account owner on the partner side and the PepsiCo business unit\n      counterpart jointly own the integration relationship.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pepsico/refs/heads/main/finops/pepsico-finops.yml
sources:
- https://www.pepsico.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- B2B
- Supply Chain
---
