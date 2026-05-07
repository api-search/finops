---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: compute.json
  format: json
  label: Azure Compute API
  slug: azure-compute-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/compute/resource-manager/Microsoft.Compute/stable/2023-03-01/compute.json
- filename: storage.json
  format: json
  label: Azure Storage API
  slug: azure-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/storage/resource-manager/Microsoft.Storage/stable/2023-01-01/storage.json
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
description: FinOps framework definition for the Microsoft Azure Cloud API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Azure Cloud
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Azure Cloud
  PublisherName: Microsoft Azure Cloud
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Azure Cloud
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
name: Azure Cloud Finops
provider_name: Microsoft Azure Cloud
provider_slug: azure-cloud
publisher_name: Microsoft Azure Cloud
service_category: API
slug: azure-cloud-finops
source_filename: azure-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Azure Cloud\nproviderId: azure-cloud\npublisherName: Microsoft Azure Cloud\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - AI\n  - Cloud Computing\n  - Databases\n  - IaaS\n  - Infrastructure\n  - Machine Learning\n  - Microsoft\n  - Networking\n  - PaaS\n  - Platform as a Service\n  - SaaS\n  - Storage\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Azure Cloud API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible\
  \ to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Azure Cloud\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Azure Cloud\n  PublisherName: Microsoft Azure Cloud\n  InvoiceIssuerName: Microsoft Azure Cloud\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      -\
  \ api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Compute API\n    baseURL: https://management.azure.com\n    tags:\n      - App Service\n      - Compute\n      - Containers\n      - Functions\n      - Kubernetes\n      - Serverless\n      - Virtual Machines\n    serviceName: Azure Compute API\n    serviceCategory: API\n  - name: Azure Storage API\n    baseURL: https://management.azure.com\n    tags:\n      - Blob Storage\n      - Cloud Storage\n      - File Storage\n      - Object Storage\n      - Queue Storage\n      - Storage\n      - Table Storage\n\
  \    serviceName: Azure Storage API\n    serviceCategory: API\n  - name: Azure Networking API\n    baseURL: https://management.azure.com\n    tags:\n      - ExpressRoute\n      - Firewall\n      - Load Balancer\n      - Networking\n      - Virtual Network\n      - VPN\n    serviceName: Azure Networking API\n    serviceCategory: API\n  - name: Azure Databases API\n    baseURL: https://management.azure.com\n    tags:\n      - Cosmos DB\n      - Databases\n      - MySQL\n      - NoSQL\n      - PostgreSQL\n      - Redis\n      - SQL\n    serviceName: Azure Databases API\n    serviceCategory: API\n  - name: Azure AI Services API\n    baseURL: https://management.azure.com\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Computer Vision\n      - Language\n      - Machine Learning\n      - OpenAI\n      - Speech\n    serviceName: Azure AI Services API\n    serviceCategory: API\n  - name: Azure Security API\n    baseURL: https://management.azure.com\n    tags:\n      - Defender\n\
  \      - Identity\n      - Key Vault\n      - Security\n      - Sentinel\n    serviceName: Azure Security API\n    serviceCategory: API\n  - name: Azure Integration API\n    baseURL: https://management.azure.com\n    tags:\n      - API Management\n      - Event Grid\n      - Integration\n      - Logic Apps\n      - Messaging\n      - Service Bus\n      - Workflows\n    serviceName: Azure Integration API\n    serviceCategory: API\n  - name: Azure Analytics API\n    baseURL: https://management.azure.com\n    tags:\n      - Analytics\n      - Big Data\n      - Data Factory\n      - ETL\n      - Stream Analytics\n      - Synapse\n    serviceName: Azure Analytics API\n    serviceCategory: API\n  - name: Azure Management API\n    baseURL: https://management.azure.com\n    tags:\n      - Cost Management\n      - Governance\n      - Management\n      - Monitor\n      - Policy\n      - Resource Manager\n    serviceName: Azure Management API\n    serviceCategory: API\n  - name: Azure IoT API\n \
  \   baseURL: https://management.azure.com\n    tags:\n      - Digital Twins\n      - IoT\n      - IoT Central\n      - IoT Edge\n      - IoT Hub\n    serviceName: Azure IoT API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-cloud/refs/heads/main/finops/azure-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Cloud Computing
- Databases
- IaaS
- Infrastructure
- Machine Learning
- Microsoft
- Networking
- PaaS
- Platform as a Service
- SaaS
- Storage
- FinOps
- Cost Management
- FOCUS
---
