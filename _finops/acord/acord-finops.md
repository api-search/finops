---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: acord-ngds-openapi.yml
  format: yaml
  label: ACORD Next-Generation Digital Standards (NGDS) API
  slug: acord-ngds-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acord/refs/heads/main/openapi/acord-ngds-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Membership + Optional Services
description: FOCUS-aligned FinOps scaffold for ACORD. ACORD invoices member organizations for annual membership and, separately, for ACORD Solutions Group services. There are no per-API metered charges because ACORD publishes standards rather than operating an API.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: ACORD Corporation
  ProviderName: ACORD
  PublisherName: ACORD Corporation
  ServiceCategory: Insurance Standards / Data Exchange
  ServiceName: ACORD
layout: finops
meters:
- aggregation: sum
  description: ACORD annual membership dues, scaled to organization type and revenue.
  dimensions:
  - organization_type
  - revenue_band
  name: annual_membership
  unit: year
- aggregation: sum
  description: Project-based billing from ACORD Solutions Group (data services, reinsurance services, onboarding services).
  dimensions:
  - service_line
  name: acord_solutions_group_service
  unit: project
- aggregation: sum
  description: Per-certification fee (e.g. AL3, ACORD certification programs).
  dimensions:
  - program
  name: certification_fee
  unit: certification
name: Acord Finops
provider_name: ACORD
provider_slug: acord
publisher_name: ACORD Corporation
service_category: Insurance Standards / Data Exchange
slug: acord-finops
source_filename: acord-finops.yml
source_heading: FinOps Profile
source_url: https://www.acord.org/standards-architecture/acord-data-standards
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: ACORD\nproviderId: acord\npublisherName: ACORD Corporation\nserviceCategory: Insurance Standards / Data Exchange\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - ACORD\n  - Insurance\n  - Standards\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for ACORD. ACORD invoices member organizations for annual\n  membership and, separately, for ACORD Solutions Group services. There are no per-API metered charges\n  because ACORD publishes standards rather than operating an API.\nsources:\n  - https://www.acord.org/standards-architecture/acord-data-standards\n  - https://www.acord.org/about-acord/membership\n\
  notes: ACORD does not publish public dues; FinOps shape below describes the typical line items a member\n  organization would see — annual membership and optional Solutions Group / certification fees.\nbillingModel:\n  pricingCategory: Membership + Optional Services\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: ACORD\n  ServiceCategory: Insurance Standards / Data Exchange\n  ProviderName: ACORD\n  PublisherName: ACORD Corporation\n  InvoiceIssuerName: ACORD Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: annual_membership\n    description: ACORD annual membership dues, scaled to organization type and revenue.\n    unit: year\n    aggregation: sum\n    dimensions:\n      - organization_type\n      - revenue_band\n  - name: acord_solutions_group_service\n    description: Project-based billing from ACORD Solutions Group (data services, reinsurance services,\n      onboarding services).\n\
  \    unit: project\n    aggregation: sum\n    dimensions:\n      - service_line\n  - name: certification_fee\n    description: Per-certification fee (e.g. AL3, ACORD certification programs).\n    unit: certification\n    aggregation: sum\n    dimensions:\n      - program\nprinciples:\n  - name: Visibility\n    description: Track ACORD line items from the membership invoice and any ACORD Solutions Group statements\n      of work; there is no usage API.\n  - name: Allocation\n    description: Allocate membership cost to the standards / architecture function; allocate Solutions\n      Group projects to the line of business that sponsored the engagement (claims, policy, reinsurance).\n  - name: Optimization\n    description: Optimization is governance — ensuring the organization adopts ACORD versions consistently\n      so investments in standard implementations don't fragment.\n  - name: Accountability\n    description: Standards / data-architecture leadership owns the membership relationship;\
  \ project owners\n      own Solutions Group spend.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/acord/refs/heads/main/finops/acord-finops.yml
sources:
- https://www.acord.org/standards-architecture/acord-data-standards
- https://www.acord.org/about-acord/membership
specification: FinOps Framework
tags:
- ACORD
- Insurance
- Standards
- FinOps
- FOCUS
---
