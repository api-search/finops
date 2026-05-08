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
description: FinOps framework definition for the Microsoft Intune API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Intune
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Intune
  PublisherName: Microsoft Intune
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Intune
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
name: Microsoft Intune Finops
provider_name: Microsoft Intune
provider_slug: microsoft-intune
publisher_name: Microsoft Intune
service_category: API
slug: microsoft-intune-finops
source_filename: microsoft-intune-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Intune\nproviderId: microsoft-intune\npublisherName: Microsoft Intune\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - App Protection\n  - Azure\n  - Compliance\n  - Device Configuration\n  - Endpoint Management\n  - Enrollment\n  - MAM\n  - MDM\n  - Microsoft Graph\n  - Mobile Application Management\n  - Mobile Device Management\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Intune API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Intune\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Intune\n  PublisherName: Microsoft Intune\n  InvoiceIssuerName: Microsoft Intune\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Intune API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Applications\n      - Compliance\n      - Devices\n      - Groups\n      - Policies\n      - Users\n    serviceName: Microsoft Intune API\n    serviceCategory: API\n  - name: Intune Data Warehouse API\n    baseURL: https://api.manage.microsoft.com/\n    tags:\n      - Analytics\n      - Data Warehouse\n      - Odata\n      - Reporting\n    serviceName: Intune Data Warehouse API\n    serviceCategory: API\n  - name:\
  \ Intune Device Management API\n    baseURL: https://graph.microsoft.com/v1.0/deviceManagement\n    tags:\n      - Device Compliance\n      - Devices\n      - Managed Devices\n      - Remote Actions\n    serviceName: Intune Device Management API\n    serviceCategory: API\n  - name: Intune Device Configuration API\n    baseURL: https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations\n    tags:\n      - CSP\n      - Device Configuration\n      - Policies\n      - Settings\n    serviceName: Intune Device Configuration API\n    serviceCategory: API\n  - name: Intune Device Compliance API\n    baseURL: https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies\n    tags:\n      - Compliance\n      - Device Compliance\n      - Policies\n      - Security\n    serviceName: Intune Device Compliance API\n    serviceCategory: API\n  - name: Intune Device Enrollment API\n    baseURL: https://graph.microsoft.com/v1.0/deviceManagement\n    tags:\n      - Corporate Devices\n\
  \      - Enrollment\n      - Onboarding\n    serviceName: Intune Device Enrollment API\n    serviceCategory: API\n  - name: Intune Mobile App Management API\n    baseURL: https://graph.microsoft.com/beta/deviceAppManagement\n    tags:\n      - App Protection\n      - Applications\n      - MAM\n      - Mobile App Management\n    serviceName: Intune Mobile App Management API\n    serviceCategory: API\n  - name: Intune Reports Export API\n    baseURL: https://graph.microsoft.com/v1.0/deviceManagement/reports\n    tags:\n      - Analytics\n      - Compliance Reports\n      - Export\n      - Reports\n    serviceName: Intune Reports Export API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-intune/refs/heads/main/finops/microsoft-intune-finops.yml
sources: []
specification: FinOps Framework
tags:
- App Protection
- Azure
- Compliance
- Device Configuration
- Endpoint Management
- Enrollment
- MAM
- MDM
- Microsoft Graph
- Mobile Application Management
- Mobile Device Management
- Security
- FinOps
- Cost Management
- FOCUS
---
