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
description: FinOps framework definition for the Trellix API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Trellix
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Trellix
  PublisherName: Trellix
  ServiceCategory: Developer Tools / API
  ServiceName: Trellix
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
name: Trellix Finops
provider_name: Trellix
provider_slug: trellix
publisher_name: Trellix
service_category: API
slug: trellix-finops
source_filename: trellix-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Trellix\nproviderId: trellix\npublisherName: Trellix\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Security\n  - Cybersecurity\n  - Endpoint Security\n  - Threat Detection\n  - Threat Intelligence\n  - XDR\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Trellix API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Trellix\n  ServiceCategory: Developer Tools / API\n  ProviderName: Trellix\n  PublisherName: Trellix\n  InvoiceIssuerName: Trellix\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Trellix ePO API\n    baseURL: https://your-epo-server:8443/remote\n    tags:\n      - Endpoint Management\n      - Enterprise Security\n      - Policy Orchestration\n      - Security Management\n    serviceName: Trellix ePO API\n    serviceCategory: API\n  - name: Trellix ePO SaaS API\n    baseURL: https://api.manage.trellix.com\n    tags:\n      - Cloud Management\n      - Endpoint Management\n      - SaaS\n      - Security Management\n    serviceName: Trellix ePO SaaS API\n    serviceCategory: API\n  - name: Trellix Insights API\n    baseURL: https://api.manage.trellix.com\n    tags:\n      - Analytics\n      - Security Insights\n      - Threat Intelligence\n      - Threat\
  \ Research\n    serviceName: Trellix Insights API\n    serviceCategory: API\n  - name: Trellix EDR API\n    baseURL: https://api.manage.trellix.com\n    tags:\n      - Endpoint Detection\n      - Forensics\n      - Incident Response\n      - Threat Hunting\n    serviceName: Trellix EDR API\n    serviceCategory: API\n  - name: Trellix Data Exchange Layer (DXL) API\n    baseURL: https://dxl.trellix.com\n    tags:\n      - Automation\n      - Data Exchange\n      - Integration\n      - Messaging\n    serviceName: Trellix Data Exchange Layer (DXL) API\n    serviceCategory: API\n  - name: Trellix Endpoint Security (HX) API\n    baseURL: https://{hx-appliance}/hx/api/v3\n    tags:\n      - Containment\n      - Endpoint Security\n      - Incident Response\n      - Threat Detection\n    serviceName: Trellix Endpoint Security (HX) API\n    serviceCategory: API\n  - name: Trellix Data Loss Prevention (DLP) API\n    baseURL: https://{epo-server}:8443\n    tags:\n      - Compliance\n      - Data Loss\
  \ Prevention\n      - Data Protection\n      - Incident Management\n    serviceName: Trellix Data Loss Prevention (DLP) API\n    serviceCategory: API\n  - name: Trellix Email Security Cloud API\n    baseURL: https://etp.us.fireeye.com/api/v1\n    tags:\n      - Cloud Security\n      - Email Security\n      - Quarantine\n      - Threat Detection\n    serviceName: Trellix Email Security Cloud API\n    serviceCategory: API\n  - name: Trellix Helix API\n    baseURL: https://apps.fireeye.com/helix/api/v3\n    tags:\n      - Security Operations\n      - SIEM\n      - SOAR\n      - Threat Detection\n    serviceName: Trellix Helix API\n    serviceCategory: API\n  - name: Trellix Intelligent Sandbox API\n    baseURL: https://{sandbox-server}/php\n    tags:\n      - File Analysis\n      - Malware Analysis\n      - Sandbox\n      - Threat Detection\n    serviceName: Trellix Intelligent Sandbox API\n    serviceCategory: API\n  - name: Trellix Threat Intelligence Exchange (TIE) API\n    baseURL: https://dxl.trellix.com\n\
  \    tags:\n      - Data Exchange\n      - Malware Detection\n      - Reputation\n      - Threat Intelligence\n    serviceName: Trellix Threat Intelligence Exchange (TIE) API\n    serviceCategory: API\n  - name: Trellix IOC (Indicators of Compromise) API\n    baseURL: https://{hx-appliance}/hx/api/v3\n    tags:\n      - Indicators of Compromise\n      - Security Operations\n      - Threat Detection\n      - Threat Intelligence\n    serviceName: Trellix IOC (Indicators of Compromise) API\n    serviceCategory: API\n  - name: Trellix Detection as a Service API\n    baseURL: https://feapi.marketplace.apps.fireeye.com\n    tags:\n      - Cloud Security\n      - File Analysis\n      - Malware Detection\n      - Threat Detection\n    serviceName: Trellix Detection as a Service API\n    serviceCategory: API\n  - name: Trellix API Explorer\n    baseURL: https://api-docs.us.fireeye.com\n    tags:\n      - API Explorer\n      - Developer Tools\n      - Documentation\n      - Testing\n    serviceName:\
  \ Trellix API Explorer\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trellix/refs/heads/main/finops/trellix-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Security
- Cybersecurity
- Endpoint Security
- Threat Detection
- Threat Intelligence
- XDR
- FinOps
- Cost Management
- FOCUS
---
