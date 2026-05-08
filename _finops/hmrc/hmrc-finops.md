---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hmrc-vat-mtd-openapi.yml
  format: yaml
  label: HMRC VAT (Making Tax Digital) API
  slug: hmrc-vat-mtd-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hmrc/refs/heads/main/openapi/hmrc-vat-mtd-openapi.yml
billing_model:
  billingCurrency: GBP
  billingFrequency: Not Applicable
  chargeCategories:
  - Adjustment
  chargeFrequency: Not Applicable
  notes: HMRC does not invoice for API access. Internal cost is consumer integration effort + dependent SaaS fees from the consuming software vendor.
  pricingCategory: Free / No Charge
description: FOCUS-aligned FinOps definition for HMRC. The HMRC Developer Hub APIs themselves are zero-cost to consumers; FinOps for HMRC therefore tracks the indirect cost of integration (rate-limit-driven design, software-recognition compliance, fraud-prevention overhead) rather than direct billing. ChargeCategory for HMRC API usage is effectively zero / not-billed.
focus_columns:
  BillingCurrency: GBP
  ChargeCategory: Adjustment
  InvoiceIssuerName: Not applicable (free service)
  PricingCategory: Free
  PricingUnit: request
  ProviderName: HMRC UK Tax Authority
  PublisherName: HM Revenue & Customs
  ServiceCategory: Government / Tax
  ServiceName: HMRC Developer Hub
layout: finops
meters:
- aggregation: sum
  description: Count of requests sent to HMRC APIs per registered application
  dimensions:
  - api
  - environment
  - application_id
  - tax_period
  - end_customer
  name: api_requests
  unit: request
- aggregation: sum
  description: Count of HTTP 429 / MESSAGE_THROTTLED_OUT responses, used as a leading indicator for design changes or rate-limit uplift requests
  dimensions:
  - api
  - application_id
  name: throttled_responses
  unit: response
- aggregation: sum
  description: Count of 503 SCHEDULED_MAINTENANCE / SERVER_ERROR responses
  dimensions:
  - api
  name: maintenance_events
  unit: event
- aggregation: max
  description: Indicator that the consuming product holds HMRC Recognised Software status for a given tax regime
  dimensions:
  - api
  - application_id
  name: recognised_software_status
  unit: status
name: Hmrc Finops
provider_name: HMRC UK Tax Authority
provider_slug: hmrc
publisher_name: HM Revenue & Customs
service_category: Government / Tax
slug: hmrc-finops
source_filename: hmrc-finops.yml
source_heading: FinOps Profile
source_url: https://developer.service.hmrc.gov.uk/api-documentation
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: HMRC UK Tax Authority\nproviderId: hmrc\npublisherName: HM Revenue & Customs\nserviceCategory: Government / Tax\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Government\n  - Making Tax Digital\n  - Regulatory\n  - Tax\n  - UK\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps definition for HMRC. The HMRC Developer Hub APIs themselves are zero-cost\n  to consumers; FinOps for HMRC therefore tracks the indirect cost of integration (rate-limit-driven design,\n  software-recognition compliance, fraud-prevention overhead) rather than direct billing. ChargeCategory\n  for HMRC API usage is effectively zero / not-billed.'\nsources:\n \
  \ - https://developer.service.hmrc.gov.uk/api-documentation\n  - https://developer.service.hmrc.gov.uk/api-documentation/docs/reference-guide\n  - https://developer.service.hmrc.gov.uk/api-documentation/docs/terms-of-use\nbillingModel:\n  pricingCategory: Free / No Charge\n  billingFrequency: Not Applicable\n  billingCurrency: GBP\n  chargeCategories:\n    - Adjustment\n  chargeFrequency: Not Applicable\n  notes: HMRC does not invoice for API access. Internal cost is consumer integration effort + dependent SaaS\n    fees from the consuming software vendor.\nfocusColumns:\n  ServiceName: HMRC Developer Hub\n  ServiceCategory: Government / Tax\n  ProviderName: HMRC UK Tax Authority\n  PublisherName: HM Revenue & Customs\n  InvoiceIssuerName: 'Not applicable (free service)'\n  PricingCategory: Free\n  PricingUnit: request\n  BillingCurrency: GBP\n  ChargeCategory: Adjustment\nprinciples:\n  - name: Visibility\n    description: Use the HMRC Developer Hub application dashboard to monitor request\
  \ volume and 429 rates\n      per registered application. Capture Request-Id correlation IDs and Gov-Client-* fraud-prevention\n      header values in your observability pipeline.\n  - name: Allocation\n    description: Allocate engineering and integration cost by HMRC API family (VAT MTD, Self Assessment,\n      PAYE, Customs Declarations, Corporation Tax). Tag traffic by tax-period and by the end-customer of\n      the consuming software so internal recharge to the relevant product line is possible.\n  - name: Optimization\n    description: HMRC penalises batching; design submission flows around real-time user actions to stay\n      under the 3 RPS per-application throttle. Cache reference data (rates, codes) where HMRC permits to\n      reduce gateway pressure. If sustained throughput is required, lodge a rate-limit-uplift request with\n      HMRC SDS rather than spawning multiple applications.\n  - name: Accountability\n    description: Assign a named owner per HMRC API integration\
  \ who is responsible for software-recognition\n      status, fraud-prevention header correctness, Terms-of-Use compliance, and incident response when HMRC\n      issues 503 / SCHEDULED_MAINTENANCE notices.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Onboarding Workloads\n      - Intersecting Disciplines\nmeters:\n  - name: api_requests\n    description: Count of requests sent to HMRC APIs per registered application\n\
  \    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - application_id\n      - tax_period\n      - end_customer\n  - name: throttled_responses\n    description: Count of HTTP 429 / MESSAGE_THROTTLED_OUT responses, used as a leading indicator for\n      design changes or rate-limit uplift requests\n    unit: response\n    aggregation: sum\n    dimensions:\n      - api\n      - application_id\n  - name: maintenance_events\n    description: Count of 503 SCHEDULED_MAINTENANCE / SERVER_ERROR responses\n    unit: event\n    aggregation: sum\n    dimensions:\n      - api\n  - name: recognised_software_status\n    description: Indicator that the consuming product holds HMRC Recognised Software status for a given\n      tax regime\n    unit: status\n    aggregation: max\n    dimensions:\n      - api\n      - application_id\napis:\n  - name: HMRC VAT (Making Tax Digital) API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Government\n\
  \      - Making Tax Digital\n      - REST\n      - Tax\n      - UK\n      - VAT\n    serviceName: HMRC VAT (Making Tax Digital) API\n    serviceCategory: Government / Tax\n  - name: HMRC Self Assessment API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Government\n      - Income Tax\n      - REST\n      - Self Assessment\n      - Tax\n      - UK\n    serviceName: HMRC Self Assessment API\n    serviceCategory: Government / Tax\n  - name: HMRC PAYE (Pay As You Earn) API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Government\n      - PAYE\n      - Payroll\n      - REST\n      - Tax\n      - UK\n    serviceName: HMRC PAYE (Pay As You Earn) API\n    serviceCategory: Government / Tax\n  - name: HMRC Customs Declarations API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Customs\n      - Excise\n      - Government\n      - REST\n      - Tax\n      - UK\n      - XML\n    serviceName: HMRC Customs Declarations API\n    serviceCategory:\
  \ Government / Tax\n  - name: HMRC Corporation Tax API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Business\n      - Corporation Tax\n      - Government\n      - REST\n      - Tax\n      - UK\n    serviceName: HMRC Corporation Tax API\n    serviceCategory: Government / Tax\nunitEconomics:\n  - name: Throttle Pressure\n    metric: throttled_responses / api_requests\n    target: '< 0.1%'\n  - name: Cost per HMRC Submission (consumer side)\n    metric: consumer_engineering_and_saas_cost / submissions\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hmrc/refs/heads/main/finops/hmrc-finops.yml
sources:
- https://developer.service.hmrc.gov.uk/api-documentation
- https://developer.service.hmrc.gov.uk/api-documentation/docs/reference-guide
- https://developer.service.hmrc.gov.uk/api-documentation/docs/terms-of-use
specification: FinOps Framework
tags:
- Government
- Making Tax Digital
- Regulatory
- Tax
- UK
- FinOps
- Cost Management
- FOCUS
---
