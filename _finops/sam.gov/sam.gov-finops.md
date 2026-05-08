---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sam-gov-location-services-openapi.yml
  format: yaml
  label: SAM.gov Public Location Services API
  slug: location-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sam.gov/refs/heads/main/openapi/sam-gov-location-services-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories:
  - Usage
  pricingCategory: Free / No Charge
description: FOCUS-aligned FinOps artifact for SAM.gov. Pricing is gated; meters and principles describe the expected billing surface. SAM.gov is a free public federal API operated by GSA. There is no fee. Specific per-day request limits vary by user role (federal, non-federal, general) and are not published as concrete numbers on the public docs; users must contact GSA via fsd.gov for the applicable threshold.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: U.S. General Services Administration
  ProviderName: SAM.gov
  PublisherName: U.S. General Services Administration
  ServiceCategory: Federal Government / Procurement Data
  ServiceName: SAM.gov
  ServiceSubcategory: Government Open Data
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - user_role
  name: api_requests
  unit: request
name: Sam.Gov Finops
provider_name: SAM.gov
provider_slug: sam.gov
publisher_name: U.S. General Services Administration
service_category: Federal Government / Procurement Data
slug: sam.gov-finops
source_filename: sam.gov-finops.yml
source_heading: FinOps Profile
source_url: https://open.gsa.gov/api/get-opportunities-public-api/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAM.gov\nproviderId: sam.gov\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Contracts\n- Entity Management\n- Federal Government\n- GSA\n- Procurement\n- FinOps\n- FOCUS\ndescription: FOCUS-aligned FinOps artifact for SAM.gov. Pricing is gated; meters and principles describe\n  the expected billing surface. SAM.gov is a free public federal API operated by GSA. There is no fee.\n  Specific per-day request limits vary by user role (federal, non-federal, general) and are not published\n  as concrete numbers on the public docs; users must contact GSA via fsd.gov for the applicable threshold.\nsources:\n- https://open.gsa.gov/api/get-opportunities-public-api/\n- https://focus.finops.org/focus-specification/v1-3/\n- https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: U.S. General Services Administration\nserviceCategory: Federal Government / Procurement Data\nbillingModel:\n  pricingCategory: Free / No Charge\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\nfocusColumns:\n  ServiceName: SAM.gov\n  ServiceCategory: Federal Government / Procurement Data\n  ServiceSubcategory: Government Open Data\n  ProviderName: SAM.gov\n  PublisherName: U.S. General Services Administration\n  InvoiceIssuerName: U.S. General Services Administration\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_requests\n  unit: request\n  aggregation: sum\n  dimensions:\n  - endpoint\n  - user_role\nprinciples:\n- name: Visibility\n  description: There is no cost to consume; track per-endpoint daily request counts against the role-based\n    quota documented at open.gsa.gov.\n- name: Allocation\n  description:\
  \ Allocate by SAM.gov API key per consuming application; tag downstream spend (e.g. ETL compute,\n    storage) by data product.\n- name: Optimization\n  description: Cache opportunities and entity records aggressively, page with the max 1,000 records per\n    request, and use delta queries via posted_from/posted_to filters to avoid full re-scans.\n- name: Accountability\n  description: 'Owner: data-engineering team responsible for the SAM.gov ingest job. Quota breaches are\n    operational issues, not financial.'\nnotes: SAM.gov is a free public federal API operated by GSA. There is no fee. Specific per-day request\n  limits vary by user role (federal, non-federal, general) and are not published as concrete numbers on\n  the public docs; users must contact GSA via fsd.gov for the applicable threshold.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sam.gov/refs/heads/main/finops/sam.gov-finops.yml
sources:
- https://open.gsa.gov/api/get-opportunities-public-api/
- https://focus.finops.org/focus-specification/v1-3/
- https://www.finops.org/framework/
specification: FinOps Framework
tags:
- Contracts
- Entity Management
- Federal Government
- GSA
- Procurement
- FinOps
- FOCUS
---
