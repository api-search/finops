---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps shell for Allscripts / Veradigm: regulated FHIR API access is free per ONC / Cures Act mandate; commercial Unity API and Veradigm Developer Program access is contract-based with custom terms. Reconcile meter rates against the negotiated developer-program or health-system contract.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Veradigm Inc.
  ProviderName: Veradigm
  PublisherName: Veradigm Inc.
  ServiceCategory: Electronic Health Records
  ServiceName: Allscripts / Veradigm Healthcare APIs
layout: finops
meters:
- aggregation: sum
  description: Annual partner / developer-program subscription
  dimensions:
  - product
  - tier
  name: developer_program_subscription
  unit: contract-year
- aggregation: sum
  description: Annual health-system EHR subscription bundling API access
  dimensions:
  - product
  - facility
  name: ehr_subscription
  unit: contract-year
- aggregation: sum
  description: API call volume (where contractually metered for high-volume integrations)
  dimensions:
  - api
  - tenant
  name: api_calls
  unit: request
- aggregation: sum
  description: Regulated FHIR API call volume (no charge under ONC mandate)
  dimensions:
  - resource
  - tenant
  name: fhir_calls
  unit: request
name: Allscripts Healthcare Solutions Finops
provider_name: Allscripts Healthcare Solutions
provider_slug: allscripts-healthcare-solutions
publisher_name: Veradigm Inc.
service_category: Electronic Health Records
slug: allscripts-healthcare-solutions-finops
source_filename: allscripts-healthcare-solutions-finops.yml
source_heading: FinOps Profile
source_url: https://veradigm.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Allscripts Healthcare Solutions\nproviderId: allscripts-healthcare-solutions\npublisherName: Veradigm Inc.\nserviceCategory: Electronic Health Records\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare IT\n  - EHR\n  - Clinical\n  - FHIR\n  - Veradigm\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shell for Allscripts / Veradigm: regulated FHIR API access is free per\n  ONC / Cures Act mandate; commercial Unity API and Veradigm Developer Program access is contract-based\n  with custom terms. Reconcile meter rates against the negotiated developer-program or health-system contract.'\nsources:\n  - https://veradigm.com\n\
  \  - https://developer.veradigm.com\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Allscripts / Veradigm Healthcare APIs\n  ServiceCategory: Electronic Health Records\n  ProviderName: Veradigm\n  PublisherName: Veradigm Inc.\n  InvoiceIssuerName: Veradigm Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: developer_program_subscription\n    description: Annual partner / developer-program subscription\n    unit: contract-year\n    aggregation: sum\n    dimensions:\n      - product\n      - tier\n  - name: ehr_subscription\n    description: Annual health-system EHR subscription bundling API access\n    unit: contract-year\n    aggregation: sum\n    dimensions:\n      - product\n      - facility\n  - name: api_calls\n    description: API call volume (where contractually\
  \ metered for high-volume integrations)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\n  - name: fhir_calls\n    description: Regulated FHIR API call volume (no charge under ONC mandate)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - resource\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Track Veradigm partner/program invoices and tenant utilization through Veradigm customer\n      portals; correlate API usage to specific clinical workflows.\n  - name: Allocation\n    description: Allocate Veradigm spend to clinical product lines (ambulatory / acute / patient engagement)\n      and to ISV-partner integrations.\n  - name: Optimization\n    description: Consolidate redundant ISV integrations during contract renewals; align Unity vs FHIR usage\n      to lowest-cost path; lean on regulated free FHIR access where feature parity exists.\n  - name: Accountability\n    description: Owned by health-system CIO /\
  \ IT or the ISV's product owner; reviewed against clinical\n      KPIs (note completion time, claims throughput, patient access).\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/allscripts-healthcare-solutions/refs/heads/main/finops/allscripts-healthcare-solutions-finops.yml
sources:
- https://veradigm.com
- https://developer.veradigm.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Healthcare IT
- EHR
- Clinical
- FHIR
- Veradigm
- FinOps
- FOCUS
---
