---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Adjustment
  pricingCategory: Free (regulated)
description: 'FOCUS-aligned FinOps shell for Elevance Health: CMS Interoperability FHIR APIs are free to consumers per regulation, so this artifact tracks the operational cost-of-serve rather than billed consumption. Meters describe FHIR call volume by endpoint to support internal cost accounting.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Adjustment
  InvoiceIssuerName: Elevance Health, Inc.
  ProviderName: Elevance Health
  PublisherName: Elevance Health, Inc.
  ServiceCategory: Healthcare Interoperability
  ServiceName: Elevance Health FHIR APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - resource
  - app
  name: fhir_requests
  unit: request
- aggregation: count
  dimensions:
  - api
  name: registered_apps
  unit: app
- aggregation: count
  dimensions:
  - api
  name: member_authorizations
  unit: authorization
name: Elevance Health Finops
provider_name: Elevance Health
provider_slug: elevance-health
publisher_name: Elevance Health, Inc.
service_category: Healthcare Interoperability
slug: elevance-health-finops
source_filename: elevance-health-finops.yml
source_heading: FinOps Profile
source_url: https://www.anthem.com/developers
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Elevance Health\nproviderId: elevance-health\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Healthcare\n  - FHIR\n  - Interoperability\ndescription: 'FOCUS-aligned FinOps shell for Elevance Health: CMS Interoperability FHIR APIs are free\n  to consumers per regulation, so this artifact tracks the operational cost-of-serve rather than billed\n  consumption. Meters describe FHIR call volume by endpoint to support internal cost accounting.'\nnotes: Elevance Health does not bill external consumers for CMS-mandated FHIR access. FOCUS mapping\n  here serves Elevance internal accounting (compute and infrastructure attribution) rather than external\n  invoice reconciliation.\nsources:\n  - https://www.anthem.com/developers\n  - https://www.cms.gov/Regulations-and-Guidance/Guidance/Interoperability/index\nalignedWith:\n\
  \  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Elevance Health, Inc.\nserviceCategory: Healthcare Interoperability\nbillingModel:\n  pricingCategory: Free (regulated)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Elevance Health FHIR APIs\n  ServiceCategory: Healthcare Interoperability\n  ProviderName: Elevance Health\n  PublisherName: Elevance Health, Inc.\n  InvoiceIssuerName: Elevance Health, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Adjustment\nmeters:\n  - name: fhir_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - resource\n      - app\n  - name: registered_apps\n    unit: app\n    aggregation: count\n    dimensions:\n      - api\n  - name: member_authorizations\n    unit: authorization\n   \
  \ aggregation: count\n    dimensions:\n      - api\nprinciples:\n  - name: Visibility\n    description: Track FHIR call volume per registered app; expose to Elevance compliance team for CMS\n      reporting.\n  - name: Allocation\n    description: Allocate gateway and FHIR backend infrastructure cost across Patient Access, Provider\n      Directory, Formulary, and Payer-to-Payer.\n  - name: Optimization\n    description: Cache public Provider Directory and Formulary responses; right-size FHIR cluster autoscaling\n      to actual traffic profile.\n  - name: Accountability\n    description: Interoperability program owner reviews call volume and gateway cost monthly; reports\n      compliance metrics to the CMS-mandated annual filing.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/elevance-health/refs/heads/main/finops/elevance-health-finops.yml
sources:
- https://www.anthem.com/developers
- https://www.cms.gov/Regulations-and-Guidance/Guidance/Interoperability/index
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Healthcare
- FHIR
- Interoperability
---
