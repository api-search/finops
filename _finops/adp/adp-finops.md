---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adp-workers-openapi.yml
  format: yaml
  label: ADP Workers API
  slug: adp-workers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adp/refs/heads/main/openapi/adp-workers-openapi.yml
- filename: adp-payroll-openapi.yml
  format: yaml
  label: ADP Payroll API
  slug: adp-payroll-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adp/refs/heads/main/openapi/adp-payroll-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for ADP: contract-based partner pricing for HCM, payroll, and benefits APIs.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ADP, Inc.
  ProviderName: ADP
  PublisherName: ADP, Inc.
  ServiceCategory: Human Capital Management
  ServiceName: ADP
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - environment
  - partner
  name: api_requests
  unit: request
- aggregation: max
  dimensions:
  - client
  - country
  name: active_workers
  unit: worker
- aggregation: sum
  dimensions:
  - client
  - country
  name: payroll_runs
  unit: run
- aggregation: sum
  dimensions:
  - product
  name: subscription_fees
  unit: month
name: Adp Finops
provider_name: ADP
provider_slug: adp
publisher_name: ADP, Inc.
service_category: Human Capital Management
slug: adp-finops
source_filename: adp-finops.yml
source_heading: FinOps Profile
source_url: https://developers.adp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ADP\nproviderId: adp\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: ADP API pricing is custom and contract-based. FinOps mapping is approximate; actual\n  invoice line items depend on the negotiated agreement.\ntags:\n  - FinOps\n  - FOCUS\n  - HCM\n  - Payroll\n  - HR\ndescription: 'FOCUS-aligned FinOps for ADP: contract-based partner pricing for HCM, payroll, and\n  benefits APIs.'\nsources:\n  - https://developers.adp.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ADP, Inc.\nserviceCategory: Human Capital Management\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    -\
  \ Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: ADP\n  ServiceCategory: Human Capital Management\n  ProviderName: ADP\n  PublisherName: ADP, Inc.\n  InvoiceIssuerName: ADP, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - partner\n  - name: active_workers\n    unit: worker\n    aggregation: max\n    dimensions:\n      - client\n      - country\n  - name: payroll_runs\n    unit: run\n    aggregation: sum\n    dimensions:\n      - client\n      - country\n  - name: subscription_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Use ADP partner reports and the contracted usage API to track per-client request\n      and worker counts.\n  - name: Allocation\n    description: Tag API calls with the end-client identifier and the consuming product to support\n      partner chargeback.\n\
  \  - name: Optimization\n    description: Cache reference data; batch worker reads; consult ADP account team about volume\n      tier renegotiation.\n  - name: Accountability\n    description: Reconcile monthly ADP invoices against contracted minimums and active-worker counts;\n      assign budget owner per ADP product.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adp/refs/heads/main/finops/adp-finops.yml
sources:
- https://developers.adp.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- HCM
- Payroll
- HR
---
