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
  pricingCategory: Free (Regulator-Mandated)
description: FOCUS-aligned FinOps for Centene's public FHIR interoperability APIs. The APIs themselves are free (CMS-mandated read access); FinOps reporting therefore tracks the consumer-side cost of integrating — engineering effort, supporting cloud infrastructure, and SMART-on-FHIR app maintenance — rather than per-call invoice lines.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Centene Corporation
  ProviderName: Centene
  PublisherName: Centene Corporation
  ServiceCategory: Healthcare Interoperability
  ServiceName: Centene FHIR Interoperability APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - application
  - resource_type
  name: patient_access_requests
  unit: request
- aggregation: sum
  dimensions:
  - resource_type
  name: provider_directory_requests
  unit: request
- aggregation: sum
  dimensions:
  - payer
  - resource_type
  name: pdex_rtr_requests
  unit: request
- aggregation: count
  name: registered_applications
  unit: application
name: Centene Finops
provider_name: Centene
provider_slug: centene
publisher_name: Centene Corporation
service_category: Healthcare Interoperability
slug: centene-finops
source_filename: centene-finops.yml
source_heading: FinOps Profile
source_url: https://partners.centene.com/apis
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Centene\nproviderId: centene\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - FHIR\n  - CMS Interoperability\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Centene''s public FHIR interoperability APIs. The APIs themselves\n  are free (CMS-mandated read access); FinOps reporting therefore tracks the consumer-side cost of integrating\n  — engineering effort, supporting cloud infrastructure, and SMART-on-FHIR app maintenance — rather\n  than per-call invoice lines.'\nnotes: APIs are free to authorized developers; meters track consumption for capacity planning and consumer-side\n  cost-of-integration reporting.\nsources:\n  - https://partners.centene.com/apis\n  - https://partners.centene.com/applicationDeveloper\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Centene Corporation\nserviceCategory: Healthcare Interoperability\nbillingModel:\n  pricingCategory: Free (Regulator-Mandated)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Centene FHIR Interoperability APIs\n  ServiceCategory: Healthcare Interoperability\n  ProviderName: Centene\n  PublisherName: Centene Corporation\n  InvoiceIssuerName: Centene Corporation\n  BillingCurrency: USD\nmeters:\n  - name: patient_access_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - application\n      - resource_type\n  - name: provider_directory_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - resource_type\n  - name: pdex_rtr_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - payer\n      - resource_type\n  - name: registered_applications\n\
  \    unit: application\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Track per-application Patient Access call volume from the partner portal; correlate\n      with the consuming app's downstream cloud spend (compute, storage of cached FHIR resources) to\n      see total cost-of-integration.\n  - name: Allocation\n    description: Tag the consuming application's cloud workload with its Centene partner-portal client\n      identifier so the consumer-side cost is attributable to the same product.\n  - name: Optimization\n    description: Cache Provider Directory at the documented refresh cadence rather than polling per request;\n      use SMART-on-FHIR refresh tokens to avoid repeated full auth flows.\n  - name: Accountability\n    description: Compliance / interoperability lead owns the Centene partner-portal relationship; product\n      engineering owns SMART-on-FHIR app uptime; finance reports the integration's cost-of-service even\n      though Centene\
  \ does not invoice for it.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/centene/refs/heads/main/finops/centene-finops.yml
sources:
- https://partners.centene.com/apis
- https://partners.centene.com/applicationDeveloper
specification: FinOps Framework
tags:
- Healthcare
- FHIR
- CMS Interoperability
- FinOps
- FOCUS
---
