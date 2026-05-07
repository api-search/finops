---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: coresignal-multi-source-company-api-openapi.yml
  format: yaml
  label: Coresignal Multi-source Company API
  slug: multi-source-company-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-company-api-openapi.yml
- filename: coresignal-multi-source-employee-api-openapi.yml
  format: yaml
  label: Coresignal Multi-source Employee API
  slug: multi-source-employee-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-employee-api-openapi.yml
- filename: coresignal-multi-source-jobs-api-openapi.yml
  format: yaml
  label: Coresignal Multi-source Jobs API
  slug: multi-source-jobs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-jobs-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription + Credit Consumption
description: FOCUS-aligned FinOps for Coresignal - monthly subscription minimum plus credit-metered consumption (Collect and Search credits) with tiered per-record pricing. Datasets product is custom-priced and billed per contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Coresignal, UAB
  PricingCategory: Usage-Based
  ProviderName: Coresignal
  PublisherName: Coresignal, UAB
  ServiceCategory: B2B Data API
  ServiceName: Coresignal
layout: finops
meters:
- aggregation: sum
  description: Collect (GET / Bulk Collect) credits consumed against the plan allotment
  dimensions:
  - api
  - endpoint
  - api_key
  - plan
  name: collect_credits
  unit: credit
- aggregation: sum
  description: Search (POST) credits consumed against the plan allotment
  dimensions:
  - api
  - endpoint
  - api_key
  - plan
  name: search_credits
  unit: credit
- aggregation: sum
  description: Records returned to the consumer (basis for per-record pricing)
  dimensions:
  - api
  - record_type
  - api_key
  name: records_returned
  unit: record
- aggregation: max
  description: Monthly subscription minimum charge
  dimensions:
  - plan
  - billing_term
  name: subscription_fee
  unit: month
- aggregation: max
  description: Dataset (companies / employees / jobs) license fee
  dimensions:
  - dataset
  - delivery_cadence
  name: dataset_license
  unit: month
name: Coresignal Finops
provider_name: Coresignal
provider_slug: coresignal
publisher_name: Coresignal, UAB
service_category: B2B Data API
slug: coresignal-finops
source_filename: coresignal-finops.yml
source_heading: FinOps Profile
source_url: https://coresignal.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Coresignal\nproviderId: coresignal\npublisherName: Coresignal, UAB\nserviceCategory: B2B Data API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - B2B Data\n  - Companies\n  - Data as a Service\n  - Employees\n  - Job Postings\n  - Sales Intelligence\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Coresignal - monthly subscription minimum plus credit-metered\n  consumption (Collect and Search credits) with tiered per-record pricing. Datasets product is custom-priced\n  and billed per contract.\nsources:\n  - https://coresignal.com/pricing/\n  - https://docs.coresignal.com/api-introduction/rate-limits\n\
  \  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription + Credit Consumption\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Coresignal\n  ServiceCategory: B2B Data API\n  ProviderName: Coresignal\n  PublisherName: Coresignal, UAB\n  InvoiceIssuerName: Coresignal, UAB\n  PricingCategory: Usage-Based\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: collect_credits\n    description: Collect (GET / Bulk Collect) credits consumed against the plan allotment\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - api_key\n      - plan\n  - name: search_credits\n    description: Search (POST) credits consumed against the plan allotment\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - api_key\n      - plan\n  - name: records_returned\n    description: Records returned to the consumer (basis for per-record pricing)\n    unit: record\n    aggregation: sum\n    dimensions:\n      - api\n      - record_type\n      - api_key\n  - name: subscription_fee\n    description: Monthly subscription minimum charge\n    unit: month\n    aggregation: max\n    dimensions:\n      - plan\n      - billing_term\n  - name: dataset_license\n    description: Dataset (companies / employees / jobs) license fee\n    unit: month\n    aggregation: max\n    dimensions:\n      - dataset\n      - delivery_cadence\nprinciples:\n  - name: Visibility\n    description: Monitor per-API-key Collect and Search credit consumption from the Coresignal dashboard\n      against the monthly allotment. Track per-record pricing tier breakpoints to forecast unit cost\n      as volume grows.\n  - name: Allocation\n    description: Issue separate API keys per consuming team, environment, or downstream product\
  \ so\n      credit consumption can be allocated. Tag retrieved records by use case (lead-gen, talent intelligence,\n      enrichment) to attribute cost to revenue-generating workflows.\n  - name: Optimization\n    description: Use Search to filter precisely before issuing Collect calls; prefer Bulk Collect for\n      ingest workloads (higher rate-limit budget at 27 rps); cache and dedupe records to avoid re-billing\n      for the same entity; size monthly commit at the next price-tier breakpoint to lower per-record\n      cost; consider annual prepay for the published 20% discount.\n  - name: Accountability\n    description: Designate an owner per API key with a monthly credit budget. Alert on burn-rate to\n      avoid hitting the credit cap mid-month, and review actual records-returned vs. committed plan\n      tier each renewal cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/finops/coresignal-finops.yml
sources:
- https://coresignal.com/pricing/
- https://docs.coresignal.com/api-introduction/rate-limits
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- B2B Data
- Companies
- Data as a Service
- Employees
- Job Postings
- Sales Intelligence
- FinOps
- Cost Management
- FOCUS
---
