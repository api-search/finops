---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: chs-patient-access-api-openapi.yml
  format: yaml
  label: Community Health Systems Patient Access API
  slug: patient-access-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/community-health-systems/refs/heads/main/openapi/chs-patient-access-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Encounter
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Healthcare Services
description: 'FOCUS-aligned FinOps for Community Health Systems: a hospital operator without a commercial API surface. CHS pays vendors (EHR, RCM, payers) rather than billing API consumers. Meters here capture vendor invoice abstractions, not consumption-metered API revenue.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Community Health Systems, Inc.
  ProviderName: Community Health Systems
  PublisherName: Community Health Systems, Inc.
  ServiceCategory: Healthcare
  ServiceName: Community Health Systems
layout: finops
meters:
- aggregation: sum
  dimensions:
  - facility
  - service_line
  name: patient_encounters
  unit: encounter
- aggregation: sum
  name: ehr_subscription
  unit: month
- aggregation: sum
  name: rcm_services
  unit: claim
name: Community Health Systems Finops
provider_name: Community Health Systems
provider_slug: community-health-systems
publisher_name: Community Health Systems, Inc.
service_category: Healthcare
slug: community-health-systems-finops
source_filename: community-health-systems-finops.yml
source_heading: FinOps Profile
source_url: https://www.chs.net/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Community Health Systems\nproviderId: community-health-systems\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Healthcare\ndescription: 'FOCUS-aligned FinOps for Community Health Systems: a hospital operator without a commercial\n  API surface. CHS pays vendors (EHR, RCM, payers) rather than billing API consumers. Meters here capture\n  vendor invoice abstractions, not consumption-metered API revenue.'\nsources:\n  - https://www.chs.net/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Community Health Systems, Inc.\nserviceCategory: Healthcare\nbillingModel:\n  pricingCategory: Healthcare Services\n  billingFrequency: Per-Encounter\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Community Health Systems\n  ServiceCategory: Healthcare\n  ProviderName: Community Health Systems\n  PublisherName: Community Health Systems, Inc.\n  InvoiceIssuerName: Community Health Systems, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: patient_encounters\n    unit: encounter\n    aggregation: sum\n    dimensions:\n      - facility\n      - service_line\n  - name: ehr_subscription\n    unit: month\n    aggregation: sum\n  - name: rcm_services\n    unit: claim\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track EHR vendor consumption (storage, transactions) against contract; reconcile vendor\n      invoices monthly.\n  - name: Allocation\n    description: Tag IT spend to facility, service line, or revenue cycle function.\n  - name: Optimization\n    description: Consolidate vendor contracts across acquisitions; renegotiate\
  \ at renewal.\n  - name: Accountability\n    description: CIO/CFO own enterprise vendor relationships; facility CFOs own local IT chargeback.\nnotes: CHS is not an API publisher; meters here are invoice abstractions for the operator's IT spend.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/community-health-systems/refs/heads/main/finops/community-health-systems-finops.yml
sources:
- https://www.chs.net/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Healthcare
---
