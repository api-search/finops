---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: varian-aria-fhir-openapi.yml
  format: yaml
  label: ARIA FHIR API
  slug: aria-fhir-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/varian-medical-systems/refs/heads/main/openapi/varian-aria-fhir-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Bundled with Clinical-System License
description: 'FinOps shape for Varian Medical Systems: APIs run on premises inside customer hospital deployments of Aria/Eclipse/Velocity. Cost is bundled into the clinical-system license and maintenance contract rather than billed per API call.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Siemens Healthineers
  ProviderName: Varian Medical Systems
  PublisherName: Varian Medical Systems (Siemens Healthineers)
  ServiceCategory: Healthcare
  ServiceName: Varian Medical Systems
layout: finops
meters:
- aggregation: count
  description: API access provisioned under the Varian Developer Program; not metered as a developer billing line
  name: contracted_access
  unit: varies
name: Varian Medical Systems Finops
provider_name: Varian Medical Systems
provider_slug: varian-medical-systems
publisher_name: Varian Medical Systems (Siemens Healthineers)
service_category: Healthcare
slug: varian-medical-systems-finops
source_filename: varian-medical-systems-finops.yml
source_heading: FinOps Profile
source_url: https://cancercare.siemens-healthineers.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Varian Medical Systems\nproviderId: varian-medical-systems\npublisherName: Varian Medical Systems (Siemens Healthineers)\nserviceCategory: Healthcare\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - Oncology\n  - Medical Devices\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for Varian Medical Systems: APIs run on premises inside customer hospital deployments of Aria/Eclipse/Velocity. Cost is bundled into the clinical-system license and maintenance contract rather than billed per API call.'\nsources:\n  - https://cancercare.siemens-healthineers.com/\nnotes: No public usage-based billing surface for\
  \ Varian APIs. Costs flow through the Aria/Eclipse license, hardware, and maintenance contracts; FinOps does not apply as a per-call cost model.\nbillingModel:\n  pricingCategory: Bundled with Clinical-System License\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Varian Medical Systems\n  ServiceCategory: Healthcare\n  ProviderName: Varian Medical Systems\n  PublisherName: Varian Medical Systems (Siemens Healthineers)\n  InvoiceIssuerName: Siemens Healthineers\n  BillingCurrency: USD\nmeters:\n  - name: contracted_access\n    description: API access provisioned under the Varian Developer Program; not metered as a developer billing line\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Usage is observable at the customer's on-prem deployment via Aria/Eclipse logs; Varian does not provide a vendor-side usage dashboard.\n  - name: Allocation\n    description: Cost is\
  \ allocated through the radiation oncology department's capital and maintenance budget, not via API meters.\n  - name: Optimization\n    description: Optimization happens at the integration design level (HL7/FHIR scope, scheduled batch syncs, on-prem capacity planning) rather than per-call cost.\n  - name: Accountability\n    description: Owned by the hospital's radiation oncology IT team and the integration partner under the Developer Program agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/varian-medical-systems/refs/heads/main/finops/varian-medical-systems-finops.yml
sources:
- https://cancercare.siemens-healthineers.com/
specification: FinOps Framework
tags:
- Healthcare
- Oncology
- Medical Devices
- FinOps
- FOCUS
---
