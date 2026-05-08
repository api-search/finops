---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: department-of-homeland-security-openapi.yml
  format: yaml
  label: OpenFEMA API
  slug: openfema-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/department-of-homeland-security/refs/heads/main/openapi/department-of-homeland-security-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Department of Homeland Security API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Department of Homeland Security
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Department of Homeland Security
  PublisherName: Department of Homeland Security
  ServiceCategory: Developer Tools / API
  ServiceName: Department of Homeland Security
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Department Of Homeland Security Finops
provider_name: Department of Homeland Security
provider_slug: department-of-homeland-security
publisher_name: Department of Homeland Security
service_category: API
slug: department-of-homeland-security-finops
source_filename: department-of-homeland-security-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Department of Homeland Security\nproviderId: department-of-homeland-security\npublisherName: Department of Homeland Security\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - CISA\n  - Cybersecurity\n  - Disaster\n  - Federal Government\n  - FEMA\n  - Homeland Security\n  - Immigration\n  - NTAS\n  - Open Data\n  - USCIS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Department of Homeland Security API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption\
  \ costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Department of Homeland Security\n  ServiceCategory: Developer Tools / API\n  ProviderName: Department of Homeland Security\n  PublisherName: Department of Homeland Security\n  InvoiceIssuerName: Department of Homeland Security\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit:\
  \ request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: OpenFEMA API\n    baseURL: https://www.fema.gov/api/open\n    tags:\n      - Disaster\n      - FEMA\n      - Hazard Mitigation\n      - Public Assistance\n    serviceName: OpenFEMA API\n    serviceCategory: API\n  - name: USCIS Case Status API\n    baseURL: https://api.uscis.gov\n    tags:\n      - Case Status\n      - Immigration\n      - USCIS\n    serviceName: USCIS Case Status API\n    serviceCategory: API\n  - name: USCIS FOIA Request and Status\
  \ API\n    baseURL: https://api.uscis.gov\n    tags:\n      - FOIA\n      - Immigration\n      - USCIS\n    serviceName: USCIS FOIA Request and Status API\n    serviceCategory: API\n  - name: CISA Known Exploited Vulnerabilities Catalog Feed\n    baseURL: https://www.cisa.gov/sites/default/files/feeds\n    tags:\n      - CISA\n      - CVE\n      - Cybersecurity\n      - KEV\n      - Vulnerabilities\n    serviceName: CISA Known Exploited Vulnerabilities Catalog Feed\n    serviceCategory: API\n  - name: National Terrorism Advisory System Feed\n    baseURL: https://www.dhs.gov\n    tags:\n      - Alerts\n      - NTAS\n      - Terrorism\n      - XML\n    serviceName: National Terrorism Advisory System Feed\n    serviceCategory: API\n  - name: DHS Open Data Catalog\n    baseURL: https://catalog.data.gov/api/3\n    tags:\n      - CKAN\n      - Datasets\n      - Open Data\n    serviceName: DHS Open Data Catalog\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric:\
  \ billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/department-of-homeland-security/refs/heads/main/finops/department-of-homeland-security-finops.yml
sources: []
specification: FinOps Framework
tags:
- CISA
- Cybersecurity
- Disaster
- Federal Government
- FEMA
- Homeland Security
- Immigration
- NTAS
- Open Data
- USCIS
- FinOps
- Cost Management
- FOCUS
---
