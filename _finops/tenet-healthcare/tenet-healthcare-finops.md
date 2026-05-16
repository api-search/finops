---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tenet-healthcare-fhir-openapi.yml
  format: yaml
  label: Tenet Health Patient Portal API
  slug: tenet-health-patient-portal-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tenet-healthcare/refs/heads/main/openapi/tenet-healthcare-fhir-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps scaffold for Tenet Healthcare. Tenet is a hospital operator, not an API or SaaS vendor; there are no usage meters, public price list, or invoiced API charges to map to FOCUS columns.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tenet Healthcare Corporation
  ProviderName: Tenet Healthcare
  PublisherName: Tenet Healthcare Corporation
  ServiceCategory: Healthcare
  ServiceName: Tenet Healthcare
layout: finops
meters:
- aggregation: sum
  dimensions:
  - partner_id
  name: partner_integration_charges
  unit: varies
name: Tenet Healthcare Finops
provider_name: Tenet Healthcare
provider_slug: tenet-healthcare
publisher_name: Tenet Healthcare Corporation
service_category: Healthcare
slug: tenet-healthcare-finops
source_filename: tenet-healthcare-finops.yml
source_heading: FinOps Profile
source_url: https://www.tenethealth.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tenet Healthcare\nproviderId: tenet-healthcare\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Healthcare\ndescription: >-\n  FOCUS-aligned FinOps scaffold for Tenet Healthcare. Tenet is a hospital operator, not an API or SaaS\n  vendor; there are no usage meters, public price list, or invoiced API charges to map to FOCUS columns.\nsources:\n  - https://www.tenethealth.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: >-\n  Tenet does not invoice API or SaaS consumption to external developers; any cross-partner financial flows\n  occur under partner-specific contracts. This artifact remains a placeholder.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Tenet Healthcare Corporation\nserviceCategory: Healthcare\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Tenet Healthcare\n  ServiceCategory: Healthcare\n  ProviderName: Tenet Healthcare\n  PublisherName: Tenet Healthcare Corporation\n  InvoiceIssuerName: Tenet Healthcare Corporation\n  BillingCurrency: USD\nmeters:\n  - name: partner_integration_charges\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - partner_id\nprinciples:\n  - name: Visibility\n    description: No external usage telemetry exists; visibility is internal to Tenet IT and any partner\n      data-exchange settlements.\n  - name: Allocation\n    description: Allocation, where applicable, is per partner integration agreement rather than per API\n      consumer.\n  - name: Optimization\n    description: Cost levers are property of Tenet's internal IT and revenue-cycle\
  \ programs, not exposed\n      externally.\n  - name: Accountability\n    description: Tenet IT and partnerships organization owns any inter-organization integration costs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tenet-healthcare/refs/heads/main/finops/tenet-healthcare-finops.yml
sources:
- https://www.tenethealth.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Healthcare
---
