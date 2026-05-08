---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cisa-kev-openapi.yml
  format: yaml
  label: CISA Known Exploited Vulnerabilities (KEV) Catalog
  slug: kev
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cybersecurity-and-infrastructure-security-agency/refs/heads/main/openapi/cisa-kev-openapi.yml
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
description: FinOps framework definition for the Cybersecurity and Infrastructure Security Agency API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cybersecurity and Infrastructure Security Agency
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cybersecurity and Infrastructure Security Agency
  PublisherName: Cybersecurity and Infrastructure Security Agency
  ServiceCategory: Developer Tools / API
  ServiceName: Cybersecurity and Infrastructure Security Agency
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
name: Cybersecurity And Infrastructure Security Agency Finops
provider_name: Cybersecurity and Infrastructure Security Agency
provider_slug: cybersecurity-and-infrastructure-security-agency
publisher_name: Cybersecurity and Infrastructure Security Agency
service_category: API
slug: cybersecurity-and-infrastructure-security-agency-finops
source_filename: cybersecurity-and-infrastructure-security-agency-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cybersecurity and Infrastructure Security Agency\nproviderId: cybersecurity-and-infrastructure-security-agency\npublisherName: Cybersecurity and Infrastructure Security Agency\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Advisories\n  - AIS\n  - Binding Operational Directive\n  - CSAF\n  - CVE\n  - CWE\n  - Cybersecurity\n  - Federal Government\n  - Government\n  - ICS-CERT\n  - Information Sharing\n  - KEV\n  - Known Exploited Vulnerabilities\n  - Risk Management\n  - Security\n  - STIX\n  - TAXII\n  - Threat Intelligence\n  - Vulnerability Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cybersecurity\
  \ and Infrastructure Security Agency API\n  surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics\n  reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business\
  \ Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cybersecurity and Infrastructure Security Agency\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cybersecurity and Infrastructure Security Agency\n  PublisherName:\
  \ Cybersecurity and Infrastructure Security Agency\n  InvoiceIssuerName: Cybersecurity and Infrastructure Security Agency\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CISA Known Exploited Vulnerabilities (KEV) Catalog\n    baseURL: https://www.cisa.gov\n    tags:\n      - BOD 22-01\n      - CVE\n      -\
  \ CWE\n      - Federal Government\n      - JSON Feed\n      - KEV\n      - Vulnerability Management\n    serviceName: CISA Known Exploited Vulnerabilities (KEV) Catalog\n    serviceCategory: API\n  - name: CISA Automated Indicator Sharing (AIS) TAXII Server\n    baseURL: ''\n    tags:\n      - AIS\n      - Information Sharing\n      - STIX\n      - TAXII\n      - Threat Intelligence\n    serviceName: CISA Automated Indicator Sharing (AIS) TAXII Server\n    serviceCategory: API\n  - name: CISA Cybersecurity Advisories\n    baseURL: ''\n    tags:\n      - Advisories\n      - CSAF\n      - ICS-CERT\n      - Threat Intelligence\n    serviceName: CISA Cybersecurity Advisories\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cybersecurity-and-infrastructure-security-agency/refs/heads/main/finops/cybersecurity-and-infrastructure-security-agency-finops.yml
sources: []
specification: FinOps Framework
tags:
- Advisories
- AIS
- Binding Operational Directive
- CSAF
- CVE
- CWE
- Cybersecurity
- Federal Government
- Government
- ICS-CERT
- Information Sharing
- KEV
- Known Exploited Vulnerabilities
- Risk Management
- Security
- STIX
- TAXII
- Threat Intelligence
- Vulnerability Management
- FinOps
- Cost Management
- FOCUS
---
