---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pg-and-e-share-my-data-api-openapi.yml
  format: yaml
  label: PG&E Share My Data API
  slug: share-my-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pg-and-e/refs/heads/main/openapi/pg-and-e-share-my-data-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Tariff
  chargeCategories:
  - Purchase
  pricingCategory: Regulated Tariff
description: FOCUS-aligned FinOps placeholder for PG&E. PG&E is a regulated electric and gas utility whose primary API surface is the Share My Data / Green Button platform. Any fees are tariff- and regulator-driven rather than a self-service price book. No metered SKU is publicly modellable.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Pacific Gas and Electric Company
  ProviderName: PG&E
  PublisherName: Pacific Gas and Electric Company
  RegionId: US-CA
  ServiceCategory: Utilities Data
  ServiceName: PG&E Share My Data
  ServiceSubcategory: Energy Usage Data
layout: finops
meters:
- aggregation: count
  description: Registered third-party Share My Data integration with PG&E. Subject to CPUC tariffs / fees; not metered per-call.
  dimensions:
  - third_party
  name: third_party_registration
  unit: registration
- aggregation: count
  description: Customer-authorized data subscription under a registered third party.
  dimensions:
  - third_party
  - service_type
  name: customer_authorization
  unit: customer_consent
name: Pg And E Finops
provider_name: pg-and-e
provider_slug: pg-and-e
publisher_name: Pacific Gas and Electric Company
service_category: Utilities Data
slug: pg-and-e-finops
source_filename: pg-and-e-finops.yml
source_heading: FinOps Profile
source_url: https://www.pge.com/en/partners-and-suppliers/data-requests-research-and-academics/share-my-data.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: pg-and-e\nproviderId: pg-and-e\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Energy\n  - Utilities\n  - Share My Data\n  - Green Button\nnotes: PG&E's Share My Data is a regulated B2B data-sharing program rather than a commercial API\n  product. There is no published per-call price book to model. This artifact captures the FinOps\n  shape only at the third-party registration level.\ndescription: FOCUS-aligned FinOps placeholder for PG&E. PG&E is a regulated electric and gas utility\n  whose primary API surface is the Share My Data / Green Button platform. Any fees are tariff- and\n  regulator-driven rather than a self-service price book. No metered SKU is publicly modellable.\nsources:\n  - https://www.pge.com/en/partners-and-suppliers/data-requests-research-and-academics/share-my-data.html\nalignedWith:\n\
  \  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Pacific Gas and Electric Company\nserviceCategory: Utilities Data\nbillingModel:\n  pricingCategory: Regulated Tariff\n  billingFrequency: Per-Tariff\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: PG&E Share My Data\n  ServiceCategory: Utilities Data\n  ServiceSubcategory: Energy Usage Data\n  ProviderName: PG&E\n  PublisherName: Pacific Gas and Electric Company\n  InvoiceIssuerName: Pacific Gas and Electric Company\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  RegionId: 'US-CA'\nmeters:\n  - name: third_party_registration\n    description: Registered third-party Share My Data integration with PG&E. Subject to CPUC\n      tariffs / fees; not metered per-call.\n    unit: registration\n    aggregation: count\n    dimensions:\n\
  \      - third_party\n  - name: customer_authorization\n    description: Customer-authorized data subscription under a registered third party.\n    unit: customer_consent\n    aggregation: count\n    dimensions:\n      - third_party\n      - service_type\nprinciples:\n  - name: Visibility\n    description: Track Share My Data subscriptions and customer authorizations via the third-party\n      portal; reconcile any tariff fees with PG&E billing.\n  - name: Allocation\n    description: Allocate any tariff fee to the consuming line of business (energy program, demand\n      response, research / academic); track per customer subscription where authorization is\n      granted.\n  - name: Optimization\n    description: Use Green Button daily / hourly batch retrieval rather than high-frequency\n      polling; cache historical usage locally to minimize repeat retrievals.\n  - name: Accountability\n    description: Third-party-side program owner and PG&E business contact jointly own the\n    \
  \  registration lifecycle and tariff compliance.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pg-and-e/refs/heads/main/finops/pg-and-e-finops.yml
sources:
- https://www.pge.com/en/partners-and-suppliers/data-requests-research-and-academics/share-my-data.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Energy
- Utilities
- Share My Data
- Green Button
---
