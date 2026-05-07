---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Cybersecurity Standards API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cybersecurity Standards
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cybersecurity Standards
  PublisherName: Cybersecurity Standards
  ServiceCategory: Developer Tools / API
  ServiceName: Cybersecurity Standards
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
name: Cybersecurity Standards Finops
provider_name: Cybersecurity Standards
provider_slug: cybersecurity-standards
publisher_name: Cybersecurity Standards
service_category: API
slug: cybersecurity-standards-finops
source_filename: cybersecurity-standards-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cybersecurity Standards\nproviderId: cybersecurity-standards\npublisherName: Cybersecurity Standards\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - CIS Controls\n  - Compliance\n  - CSF\n  - Cybersecurity\n  - FedRAMP\n  - Frameworks\n  - HIPAA\n  - HITRUST\n  - Information Security\n  - ISO 27001\n  - ISO 27002\n  - NIST\n  - NIST 800-171\n  - NIST 800-218\n  - NIST 800-53\n  - OSCAL\n  - OWASP\n  - PCI DSS\n  - Risk Management\n  - SOC 2\n  - SSDF\n  - Standards\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cybersecurity Standards API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage\
  \ measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n\
  \      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cybersecurity Standards\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cybersecurity Standards\n  PublisherName: Cybersecurity Standards\n  InvoiceIssuerName: Cybersecurity Standards\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory:\
  \ Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: NIST Cybersecurity Framework (CSF) 2.0\n    baseURL: ''\n    tags:\n      - CSF\n      - Framework\n      - NIST\n      - Risk Management\n    serviceName: NIST Cybersecurity Framework (CSF) 2.0\n    serviceCategory: API\n  - name: NIST SP 800-53 Security and Privacy Controls\n    baseURL: ''\n    tags:\n      - Controls\n      - FedRAMP\n      - NIST\n\
  \      - OSCAL\n      - RMF\n    serviceName: NIST SP 800-53 Security and Privacy Controls\n    serviceCategory: API\n  - name: NIST SP 800-171 Protecting CUI\n    baseURL: ''\n    tags:\n      - CMMC\n      - CUI\n      - DIB\n      - NIST\n    serviceName: NIST SP 800-171 Protecting CUI\n    serviceCategory: API\n  - name: NIST SP 800-218 Secure Software Development Framework (SSDF)\n    baseURL: ''\n    tags:\n      - NIST\n      - Secure Development\n      - SSDF\n    serviceName: NIST SP 800-218 Secure Software Development Framework (SSDF)\n    serviceCategory: API\n  - name: ISO/IEC 27001 Information Security Management\n    baseURL: ''\n    tags:\n      - Certification\n      - ISMS\n      - ISO 27001\n      - ISO 27002\n    serviceName: ISO/IEC 27001 Information Security Management\n    serviceCategory: API\n  - name: CIS Critical Security Controls and Benchmarks\n    baseURL: ''\n    tags:\n      - Benchmarks\n      - CIS\n      - Configuration\n      - Controls\n    serviceName:\
  \ CIS Critical Security Controls and Benchmarks\n    serviceCategory: API\n  - name: OWASP Top 10 and ASVS\n    baseURL: ''\n    tags:\n      - API Security\n      - ASVS\n      - AppSec\n      - OWASP\n    serviceName: OWASP Top 10 and ASVS\n    serviceCategory: API\n  - name: PCI DSS Payment Card Industry Data Security Standard\n    baseURL: ''\n    tags:\n      - Cardholder Data\n      - Payments\n      - PCI DSS\n    serviceName: PCI DSS Payment Card Industry Data Security Standard\n    serviceCategory: API\n  - name: SOC 2 Trust Services Criteria\n    baseURL: ''\n    tags:\n      - AICPA\n      - Audit\n      - SOC 2\n      - Trust Services\n    serviceName: SOC 2 Trust Services Criteria\n    serviceCategory: API\n  - name: FedRAMP Federal Cloud Authorization\n    baseURL: ''\n    tags:\n      - Cloud\n      - FedRAMP\n      - Federal Government\n    serviceName: FedRAMP Federal Cloud Authorization\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric:\
  \ billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cybersecurity-standards/refs/heads/main/finops/cybersecurity-standards-finops.yml
sources: []
specification: FinOps Framework
tags:
- CIS Controls
- Compliance
- CSF
- Cybersecurity
- FedRAMP
- Frameworks
- HIPAA
- HITRUST
- Information Security
- ISO 27001
- ISO 27002
- NIST
- NIST 800-171
- NIST 800-218
- NIST 800-53
- OSCAL
- OWASP
- PCI DSS
- Risk Management
- SOC 2
- SSDF
- Standards
- FinOps
- Cost Management
- FOCUS
---
