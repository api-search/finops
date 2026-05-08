---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: csg-forte-rest-openapi.yml
  format: yaml
  label: CSG Forte REST API
  slug: csg-forte-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/csg/refs/heads/main/openapi/csg-forte-rest-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Enterprise Contract + Take Rate
description: 'FOCUS-aligned FinOps for CSG Systems: enterprise BSS/OSS subscriptions plus Forte per-transaction payments processing; pricing is custom-negotiated and not publicly disclosed.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CSG Systems International, Inc.
  PricingCategory: Custom Contract
  ProviderName: CSG Systems
  PublisherName: CSG Systems International, Inc.
  ServiceCategory: Billing & Revenue Management
  ServiceName: CSG Systems
layout: finops
meters:
- aggregation: sum
  description: Card payment transactions processed via CSG Forte
  dimensions:
  - merchant_id
  - card_brand
  - currency
  name: forte_card_transactions
  unit: transaction
- aggregation: sum
  description: ACH transactions processed via CSG Forte
  dimensions:
  - merchant_id
  name: forte_ach_transactions
  unit: transaction
- aggregation: max
  description: Billed subscribers / accounts on Singleview / ACP
  dimensions:
  - tenant
  - product
  name: singleview_subscribers
  unit: subscriber-month
- aggregation: sum
  description: API calls against CSG APIs (not separately billed; observed for capacity)
  dimensions:
  - api
  - tenant
  name: api_requests
  unit: request
name: Csg Finops
provider_name: CSG Systems
provider_slug: csg
publisher_name: CSG Systems International, Inc.
service_category: Billing & Revenue Management
slug: csg-finops
source_filename: csg-finops.yml
source_heading: FinOps Profile
source_url: https://www.csgi.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CSG Systems\nproviderId: csg\npublisherName: CSG Systems International, Inc.\nserviceCategory: Billing & Revenue Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Billing\n  - Customer Engagement\n  - Payments\n  - Revenue Management\n  - Telecom\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for CSG Systems: enterprise BSS/OSS subscriptions plus Forte per-transaction\n  payments processing; pricing is custom-negotiated and not publicly disclosed.'\nsources:\n  - https://www.csgi.com/products/\nnotes: No public pricing. Treat meters as descriptive; reconcile per-transaction rates and seat fees\n\
  \  from the active CSG contract.\nprinciples:\n  - name: Visibility\n    description: Use the CSG partner / merchant portal for transaction-level reporting; reconcile against\n      the monthly statement and Forte settlement files.\n  - name: Allocation\n    description: Tag Forte transactions with merchant_id / division and Singleview line items with cost\n      center to attribute spend.\n  - name: Optimization\n    description: Negotiate volume tiers at renewal; route ACH-eligible payments away from card rails;\n      consolidate billing tenants where possible.\n  - name: Accountability\n    description: Finance and Telecom-ops jointly own the CSG contract; review monthly invoices for take-rate\n      drift and seat utilization.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n\
  \  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\nbillingModel:\n  pricingCategory: Enterprise Contract + Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CSG Systems\n  ServiceCategory: Billing & Revenue Management\n  ProviderName: CSG Systems\n  PublisherName: CSG Systems International, Inc.\n  InvoiceIssuerName: CSG Systems International, Inc.\n  PricingCategory: Custom Contract\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: forte_card_transactions\n    description: Card payment transactions processed via CSG Forte\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - card_brand\n      - currency\n  - name: forte_ach_transactions\n\
  \    description: ACH transactions processed via CSG Forte\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_id\n  - name: singleview_subscribers\n    description: Billed subscribers / accounts on Singleview / ACP\n    unit: subscriber-month\n    aggregation: max\n    dimensions:\n      - tenant\n      - product\n  - name: api_requests\n    description: API calls against CSG APIs (not separately billed; observed for capacity)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\napis:\n  - name: CSG Forte REST API\n    baseURL: https://api.forte.net/v3\n    tags:\n      - ACH\n      - Billing\n      - Credit Card\n      - Payments\n      - PCI\n      - REST\n    serviceName: CSG Forte REST API\n    serviceCategory: API\n  - name: CSG Forte.js\n    baseURL: https://api.forte.net\n    tags:\n      - JavaScript\n      - Payments\n      - SDK\n      - Web\n    serviceName: CSG Forte.js\n    serviceCategory: API\n  - name: CSG\
  \ Forte React Native SDK\n    baseURL: https://api.forte.net\n    tags:\n      - Mobile\n      - Payments\n      - React Native\n      - SDK\n    serviceName: CSG Forte React Native SDK\n    serviceCategory: API\n  - name: CSG Singleview Billing API\n    baseURL: https://api.csgi.com\n    tags:\n      - Billing\n      - BSS\n      - Revenue Management\n      - SOAP\n      - Telecom\n    serviceName: CSG Singleview Billing API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Transaction\n    metric: billed_cost / (forte_card_transactions + forte_ach_transactions)\n    target: TBD\n  - name: Cost per Subscriber\n    metric: billed_cost / singleview_subscribers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/csg/refs/heads/main/finops/csg-finops.yml
sources:
- https://www.csgi.com/products/
specification: FinOps Framework
tags:
- Billing
- Customer Engagement
- Payments
- Revenue Management
- Telecom
- FinOps
- FOCUS
---
