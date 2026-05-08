---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: unitedhealth-optum-api-openapi.yml
  format: yaml
  label: UnitedHealth Group Optum API
  slug: optum-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unitedhealth/refs/heads/main/openapi/unitedhealth-optum-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: UnitedHealth Group does not expose a metered API billing surface. CMS Patient Access FHIR endpoints are free under regulatory mandate; commercial integrations are contracted through Optum / UnitedHealthcare. FinOps maps to enterprise contracts and downstream healthcare spend rather than per-call pricing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: UnitedHealth Group, Inc.
  ProviderName: UnitedHealth Group
  PublisherName: UnitedHealth Group, Inc.
  ServiceCategory: Healthcare
  ServiceName: UnitedHealth Group APIs
layout: finops
meters:
- aggregation: sum
  description: Optum / UHC commercial integration agreement (eligibility, claims, prior auth, network).
  name: contract
  unit: varies
- aggregation: count
  description: Registered Patient Access FHIR apps; not directly billed but tracked for conformance.
  name: patient_access_apps
  unit: app
name: Unitedhealth Finops
provider_name: UnitedHealth Group
provider_slug: unitedhealth
publisher_name: UnitedHealth Group, Inc.
service_category: Healthcare
slug: unitedhealth-finops
source_filename: unitedhealth-finops.yml
source_heading: FinOps Profile
source_url: https://developer.uhc.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: UnitedHealth Group\nproviderId: unitedhealth\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - FHIR\n  - FinOps\n  - FOCUS\n  - B2B\ndescription: UnitedHealth Group does not expose a metered API billing surface. CMS Patient Access\n  FHIR endpoints are free under regulatory mandate; commercial integrations are contracted through\n  Optum / UnitedHealthcare. FinOps maps to enterprise contracts and downstream healthcare spend rather\n  than per-call pricing.\nsources:\n  - https://developer.uhc.com\n  - https://developer.optum.com\nnotes: No public usage-based API billing exists. This artifact captures the contractual surface;\n  underlying claims, eligibility, and provider-network economics live in the broader UnitedHealth\n  payer business, not at the API layer.\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: UnitedHealth Group, Inc.\nserviceCategory: Healthcare\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: UnitedHealth Group APIs\n  ServiceCategory: Healthcare\n  ProviderName: UnitedHealth Group\n  PublisherName: UnitedHealth Group, Inc.\n  InvoiceIssuerName: UnitedHealth Group, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract\n    description: Optum / UHC commercial integration agreement (eligibility, claims, prior auth, network).\n    unit: varies\n    aggregation: sum\n  - name: patient_access_apps\n    description: Registered Patient Access FHIR apps; not directly billed but tracked for conformance.\n    unit: app\n    aggregation: count\nprinciples:\n\
  \  - name: Visibility\n    description: API consumption is not separately metered. Track FHIR / commercial call volume against\n      the integration contract and member-consent records.\n  - name: Allocation\n    description: Allocate UnitedHealth integration cost to the line-of-business sponsoring the integration\n      (clinical, claims operations, member experience) rather than per-call.\n  - name: Optimization\n    description: Optimize at the contract level - reduce redundant eligibility lookups, consolidate\n      claims-status polling, prefer FHIR bulk export over per-resource calls where supported.\n  - name: Accountability\n    description: Assign ownership to the team holding the Optum / UHC commercial relationship; review\n      partner usage against contracted volumes and conformance metrics.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unitedhealth/refs/heads/main/finops/unitedhealth-finops.yml
sources:
- https://developer.uhc.com
- https://developer.optum.com
specification: FinOps Framework
tags:
- Healthcare
- FHIR
- FinOps
- FOCUS
- B2B
---
