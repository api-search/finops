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
  - Usage
  pricingCategory: No-Charge (Regulatory)
description: FOCUS-aligned FinOps view for Anthem's CMS-mandated FHIR APIs. There is no direct charge for the regulatory APIs; FinOps focus is on attributing internal compute, storage, and integration costs associated with serving Patient Access, Provider Directory, and Drug Formulary endpoints.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Elevance Health, Inc.
  ProviderName: Anthem
  PublisherName: Elevance Health, Inc.
  ServiceCategory: Healthcare / FHIR Interoperability
  ServiceName: Anthem FHIR APIs
layout: finops
meters:
- aggregation: sum
  description: Count of FHIR API requests served, partitioned by API and authorization mode
  dimensions:
  - api
  - resource_type
  - auth_mode
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned in FHIR responses
  dimensions:
  - api
  - resource_type
  name: data_egress
  unit: GB
- aggregation: sum
  description: Count of SMART on FHIR authorization grants
  dimensions:
  - app
  name: smart_authorizations
  unit: authorization
name: Anthem Finops
provider_name: Anthem
provider_slug: anthem
publisher_name: Elevance Health, Inc.
service_category: Healthcare / FHIR Interoperability
slug: anthem-finops
source_filename: anthem-finops.yml
source_heading: FinOps Profile
source_url: https://www.anthem.com/developer/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Anthem\nproviderId: anthem\npublisherName: Elevance Health, Inc.\nserviceCategory: Healthcare / FHIR Interoperability\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Healthcare\n  - FHIR\n  - Interoperability\ndescription: FOCUS-aligned FinOps view for Anthem's CMS-mandated FHIR APIs. There is no direct charge\n  for the regulatory APIs; FinOps focus is on attributing internal compute, storage, and integration costs\n  associated with serving Patient Access, Provider Directory, and Drug Formulary endpoints.\nnotes: No external billing model exists for these regulator-mandated APIs. FinOps is internal\
  \ cost-attribution\n  only.\nsources:\n  - https://www.anthem.com/developer/\nbillingModel:\n  pricingCategory: No-Charge (Regulatory)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Anthem FHIR APIs\n  ServiceCategory: Healthcare / FHIR Interoperability\n  ProviderName: Anthem\n  PublisherName: Elevance Health, Inc.\n  InvoiceIssuerName: Elevance Health, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of FHIR API requests served, partitioned by API and authorization mode\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - resource_type\n      - auth_mode\n  - name: data_egress\n    description: Bytes returned in FHIR responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - resource_type\n  - name: smart_authorizations\n    description: Count of SMART on FHIR authorization grants\n    unit: authorization\n\
  \    aggregation: sum\n    dimensions:\n      - app\nprinciples:\n  - name: Visibility\n    description: Surface FHIR endpoint usage by resource type and consuming application via internal observability;\n      member-level access events are auditable for HIPAA compliance.\n  - name: Allocation\n    description: Attribute infrastructure cost to the regulatory program (CMS-9115-F) and to the consuming\n      third-party app via registered client_id.\n  - name: Optimization\n    description: Use bulk-data export ($export) for large pulls instead of repeated point reads; cache\n      Provider Directory responses; deny pagination abuse.\n  - name: Accountability\n    description: Compliance and Interoperability program teams own SLAs and infrastructure spend; vendor\n      apps accountable for honoring rate limits and member-consent scopes.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n    X: apievangelist\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/anthem/refs/heads/main/finops/anthem-finops.yml
sources:
- https://www.anthem.com/developer/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Healthcare
- FHIR
- Interoperability
---
