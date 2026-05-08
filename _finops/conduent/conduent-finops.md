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
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Services Contract
description: 'FOCUS-aligned FinOps for Conduent: services-bundled enterprise BPO contract; API consumption is not separately billed but is governed by the master services agreement.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Conduent Business Services, LLC
  ProviderName: Conduent
  PublisherName: Conduent Business Services, LLC
  ServiceCategory: Business Process Services
  ServiceName: Conduent
layout: finops
meters:
- aggregation: max
  description: Conduent enterprise services / BPO contract value
  dimensions:
  - product
  - tenant
  name: services_contract
  unit: month
- aggregation: sum
  description: Internal-only meter for chargeback within the customer organization. Not billed externally.
  dimensions:
  - api
  - consumer_app
  name: api_calls_internal
  unit: request
name: Conduent Finops
provider_name: Conduent
provider_slug: conduent
publisher_name: Conduent Business Services, LLC
service_category: Business Process Services
slug: conduent-finops
source_filename: conduent-finops.yml
source_heading: FinOps Profile
source_url: https://www.conduent.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Conduent\nproviderId: conduent\npublisherName: Conduent Business Services, LLC\nserviceCategory: Business Process Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Business Process Services\n  - Technology\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Conduent: services-bundled enterprise BPO contract; API consumption\n  is not separately billed but is governed by the master services agreement.'\nnotes: Conduent is a BPO services company; API access is bundled into the broader services contract.\n  Per-call billing is not exposed.\nsources:\n  - https://www.conduent.com\nbillingModel:\n  pricingCategory:\
  \ Enterprise Services Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Conduent\n  ServiceCategory: Business Process Services\n  ProviderName: Conduent\n  PublisherName: Conduent Business Services, LLC\n  InvoiceIssuerName: Conduent Business Services, LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: services_contract\n    description: Conduent enterprise services / BPO contract value\n    unit: month\n    aggregation: max\n    dimensions:\n      - product\n      - tenant\n  - name: api_calls_internal\n    description: Internal-only meter for chargeback within the customer organization. Not billed externally.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - consumer_app\nprinciples:\n  - name: Visibility\n    description: Track API usage internally via consumer application credentials; consult the Conduent\n      account\
  \ team for usage reporting tied to the services contract.\n  - name: Allocation\n    description: Allocate the bundled services contract across business units using the underlying business-process\n      activity (transactions, cases, calls handled).\n  - name: Optimization\n    description: Optimize through scope refinement on the services contract — review unused integrations\n      and module activation at renewal.\n  - name: Accountability\n    description: Operations / vendor-management owners typically hold the Conduent contract; integration\n      owners are accountable for staying within negotiated API capacity.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/conduent/refs/heads/main/finops/conduent-finops.yml
sources:
- https://www.conduent.com
specification: FinOps Framework
tags:
- Business Process Services
- Technology
- FinOps
- FOCUS
---
