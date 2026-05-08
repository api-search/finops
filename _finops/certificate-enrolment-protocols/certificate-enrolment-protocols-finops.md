---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: certificate-enrolment-protocols-openapi.yml
  format: yaml
  label: ACME - Automatic Certificate Management Environment (RFC 8555)
  slug: acme-rfc-8555
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/certificate-enrolment-protocols/refs/heads/main/openapi/certificate-enrolment-protocols-openapi.yml
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
description: FinOps framework definition for the Certificate Enrolment Protocols API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Certificate Enrolment Protocols
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Certificate Enrolment Protocols
  PublisherName: Certificate Enrolment Protocols
  ServiceCategory: Developer Tools / API
  ServiceName: Certificate Enrolment Protocols
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
name: Certificate Enrolment Protocols Finops
provider_name: Certificate Enrolment Protocols
provider_slug: certificate-enrolment-protocols
publisher_name: Certificate Enrolment Protocols
service_category: API
slug: certificate-enrolment-protocols-finops
source_filename: certificate-enrolment-protocols-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Certificate Enrolment Protocols\nproviderId: certificate-enrolment-protocols\npublisherName: Certificate Enrolment Protocols\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - ACME\n  - Automation\n  - CMP\n  - Certificates\n  - Cryptography\n  - EST\n  - IETF\n  - Let's Encrypt\n  - PKI\n  - RFC\n  - Renewal\n  - SCEP\n  - Security\n  - Standards\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Certificate Enrolment Protocols API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Certificate Enrolment Protocols\n  ServiceCategory: Developer Tools / API\n  ProviderName: Certificate Enrolment Protocols\n  PublisherName: Certificate Enrolment Protocols\n  InvoiceIssuerName: Certificate Enrolment Protocols\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable\
  \ API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ACME - Automatic Certificate Management Environment (RFC 8555)\n    baseURL: ''\n    tags:\n      - ACME\n      - Let's Encrypt\n      - RFC 8555\n      - Web PKI\n    serviceName: ACME - Automatic Certificate Management Environment (RFC 8555)\n    serviceCategory: API\n  - name: SCEP - Simple Certificate Enrollment Protocol\n    baseURL: ''\n    tags:\n      - IoT\n      - MDM\n      - Network Devices\n      - SCEP\n    serviceName:\
  \ SCEP - Simple Certificate Enrollment Protocol\n    serviceCategory: API\n  - name: EST - Enrollment over Secure Transport (RFC 7030)\n    baseURL: ''\n    tags:\n      - EST\n      - IoT\n      - RFC 7030\n      - TLS\n    serviceName: EST - Enrollment over Secure Transport (RFC 7030)\n    serviceCategory: API\n  - name: CMP - Certificate Management Protocol (RFC 4210 / RFC 9480)\n    baseURL: ''\n    tags:\n      - CMP\n      - Enterprise PKI\n      - Industrial\n      - RFC 4210\n      - RFC 9480\n    serviceName: CMP - Certificate Management Protocol (RFC 4210 / RFC 9480)\n    serviceCategory: API\n  - name: cert-manager (Kubernetes ACME Client)\n    baseURL: ''\n    tags:\n      - ACME\n      - CNCF\n      - Client\n      - Kubernetes\n    serviceName: cert-manager (Kubernetes ACME Client)\n    serviceCategory: API\n  - name: Certbot (ACME Reference Client)\n    baseURL: ''\n    tags:\n      - ACME\n      - Certbot\n      - EFF\n      - Let's Encrypt\n    serviceName: Certbot (ACME\
  \ Reference Client)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/certificate-enrolment-protocols/refs/heads/main/finops/certificate-enrolment-protocols-finops.yml
sources: []
specification: FinOps Framework
tags:
- ACME
- Automation
- CMP
- Certificates
- Cryptography
- EST
- IETF
- Let's Encrypt
- PKI
- RFC
- Renewal
- SCEP
- Security
- Standards
- FinOps
- Cost Management
- FOCUS
---
