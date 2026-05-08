---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Partner Contract
description: 'FOCUS-aligned FinOps for CVS Health: payer-mandated patient-access FHIR is no-cost; partner integrations (HL7 / NCPDP / EDI / FHIR) are contractual. Spend rolls up to the underlying healthcare product (PBM, plan, pharmacy), not API metering.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CVS Health Corporation
  PricingCategory: Partner Contract
  ProviderName: CVS Health
  PublisherName: CVS Health Corporation
  ServiceCategory: Healthcare
  ServiceName: CVS Health
layout: finops
meters:
- aggregation: sum
  description: FHIR API calls under patient-access / partner agreements
  dimensions:
  - app
  - resource_type
  name: fhir_requests
  unit: request
- aggregation: sum
  description: EDI healthcare transactions (270/271/834/835/837)
  dimensions:
  - partner
  - transaction_type
  name: edi_transactions
  unit: transaction
- aggregation: sum
  description: Pharmacy claim transactions via NCPDP
  dimensions:
  - partner
  - line_of_business
  name: ncpdp_claims
  unit: claim
- aggregation: sum
  description: API calls against CVS Health partner endpoints (not separately billed; observed for capacity)
  dimensions:
  - api
  - partner
  name: api_requests
  unit: request
name: Cvs Health Finops
provider_name: CVS Health
provider_slug: cvs-health
publisher_name: CVS Health Corporation
service_category: Healthcare
slug: cvs-health-finops
source_filename: cvs-health-finops.yml
source_heading: FinOps Profile
source_url: https://www.cvshealth.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CVS Health\nproviderId: cvs-health\npublisherName: CVS Health Corporation\nserviceCategory: Healthcare\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - Pharmacy\n  - Health Insurance\n  - FHIR\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for CVS Health: payer-mandated patient-access FHIR is no-cost; partner\n  integrations (HL7 / NCPDP / EDI / FHIR) are contractual. Spend rolls up to the underlying healthcare\n  product (PBM, plan, pharmacy), not API metering.'\nsources:\n  - https://www.cvshealth.com/\nnotes: No public API pricing. Reconcile against partner integration agreements for B2B\
  \ costs.\nprinciples:\n  - name: Visibility\n    description: Use partner-portal usage reports and EDI / NCPDP transaction logs to track integration\n      activity; correlate with the relevant pharmacy / payer cost center.\n  - name: Allocation\n    description: Allocate to the consuming line of business (Pharmacy, Aetna, Caremark, MinuteClinic,\n      Oak Street) via partner_id and integration_type tags.\n  - name: Optimization\n    description: Consolidate duplicate partner endpoints; prefer FHIR over EDI where supported; reuse\n      tokens within their lifetime to reduce auth overhead.\n  - name: Accountability\n    description: Health-IT integration and compliance teams jointly own partner integrations; review\n      quarterly for HIPAA, CMS rule, and 21st Century Cures Act compliance.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n \
  \     - Budgeting\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\nbillingModel:\n  pricingCategory: Partner Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CVS Health\n  ServiceCategory: Healthcare\n  ProviderName: CVS Health\n  PublisherName: CVS Health Corporation\n  InvoiceIssuerName: CVS Health Corporation\n  PricingCategory: Partner Contract\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: fhir_requests\n    description: FHIR API calls under patient-access / partner agreements\n    unit: request\n    aggregation: sum\n    dimensions:\n      - app\n      - resource_type\n  - name: edi_transactions\n    description: EDI healthcare transactions (270/271/834/835/837)\n    unit: transaction\n\
  \    aggregation: sum\n    dimensions:\n      - partner\n      - transaction_type\n  - name: ncpdp_claims\n    description: Pharmacy claim transactions via NCPDP\n    unit: claim\n    aggregation: sum\n    dimensions:\n      - partner\n      - line_of_business\n  - name: api_requests\n    description: API calls against CVS Health partner endpoints (not separately billed; observed for\n      capacity)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - partner\napis:\n  - name: CVS Health Partner Integrations\n    baseURL: ''\n    tags:\n      - EDI\n      - FHIR\n      - Healthcare\n      - HL7\n      - NCPDP\n      - Partner Integration\n      - Pharmacy\n    serviceName: CVS Health Partner Integrations\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per FHIR Request\n    metric: billed_cost / fhir_requests\n    target: TBD\n  - name: Cost per EDI Transaction\n    metric: billed_cost / edi_transactions\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n\
  \    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cvs-health/refs/heads/main/finops/cvs-health-finops.yml
sources:
- https://www.cvshealth.com/
specification: FinOps Framework
tags:
- Healthcare
- Pharmacy
- Health Insurance
- FHIR
- FinOps
- FOCUS
---
