---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: agilent-ilab-operations-api.yaml
  format: yaml
  label: Agilent iLab Operations API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/agilent-technologies/refs/heads/main/openapi/agilent-ilab-operations-api.yaml
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
description: FinOps framework definition for the agilent-technologies API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: agilent-technologies
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: agilent-technologies
  PublisherName: agilent-technologies
  ServiceCategory: Developer Tools / API
  ServiceName: agilent-technologies
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
name: Agilent Technologies Finops
provider_name: agilent-technologies
provider_slug: agilent-technologies
publisher_name: agilent-technologies
service_category: API
slug: agilent-technologies-finops
source_filename: agilent-technologies-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: agilent-technologies\nproviderId: agilent-technologies\npublisherName: agilent-technologies\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Life Sciences\n  - Diagnostics\n  - Laboratory\n  - Scientific Instruments\n  - LIMS\n  - Laboratory Automation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the agilent-technologies API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: agilent-technologies\n  ServiceCategory: Developer Tools / API\n  ProviderName: agilent-technologies\n  PublisherName: agilent-technologies\n  InvoiceIssuerName: agilent-technologies\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Agilent iLab Operations API\n    baseURL: https://api.ilabsolutions.com/v1\n    tags:\n      - Laboratory Operations\n      - Billing\n      - Core Facilities\n      - Scheduling\n    serviceName: Agilent iLab Operations API\n    serviceCategory: API\n  - name: Agilent SLIMS REST API\n    baseURL: https://your-slims-instance/rest\n    tags:\n      - LIMS\n      - Laboratory Information Management\n      - NGS\n      - Biobank\n    serviceName: Agilent SLIMS REST API\n    serviceCategory: API\n  - name: Agilent CrossLab Asset Manager API\n    baseURL: https://crosslab-api.agilent.com\n\
  \    tags:\n      - Asset Management\n      - Instrument Services\n      - CrossLab\n      - Maintenance\n    serviceName: Agilent CrossLab Asset Manager API\n    serviceCategory: API\n  - name: Agilent VWorks Automation API\n    baseURL: https://www.agilent.com\n    tags:\n      - Laboratory Automation\n      - Robotics\n      - Liquid Handling\n      - Workstation\n    serviceName: Agilent VWorks Automation API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/agilent-technologies/refs/heads/main/finops/agilent-technologies-finops.yml
sources: []
specification: FinOps Framework
tags:
- Life Sciences
- Diagnostics
- Laboratory
- Scientific Instruments
- LIMS
- Laboratory Automation
- FinOps
- Cost Management
- FOCUS
---
