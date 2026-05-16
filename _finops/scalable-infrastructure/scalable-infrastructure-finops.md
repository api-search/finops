---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: AWS EC2 API
  slug: aws-ec2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/amazonaws.com/ec2/2016-11-15/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: AWS VPC API
  slug: aws-vpc-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/amazonaws.com/ec2/2016-11-15/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: AWS EKS API
  slug: aws-eks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/amazonaws.com/eks/2018-08-23/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Google Compute Engine API
  slug: google-compute-engine-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/googleapis.com/compute/v1/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Google Kubernetes Engine API
  slug: google-kubernetes-engine-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/googleapis.com/container/v1/openapi.yaml
- filename: resources.json
  format: json
  label: Azure Resource Manager API
  slug: azure-resource-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/resources/resource-manager/Microsoft.Resources/stable/2023-07-01/resources.json
- filename: managedClusters.json
  format: json
  label: Azure AKS API
  slug: azure-aks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/containerservice/resource-manager/Microsoft.ContainerService/aks/stable/2024-01-01/managedClusters.json
- filename: DigitalOcean-public.v2.yaml
  format: yaml
  label: DigitalOcean API
  slug: digitalocean-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/digitalocean/openapi/main/specification/DigitalOcean-public.v2.yaml
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
description: FinOps framework definition for the Scalable Infrastructure API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scalable Infrastructure
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scalable Infrastructure
  PublisherName: Scalable Infrastructure
  ServiceCategory: Developer Tools / API
  ServiceName: Scalable Infrastructure
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
name: Scalable Infrastructure Finops
provider_name: Scalable Infrastructure
provider_slug: scalable-infrastructure
publisher_name: Scalable Infrastructure
service_category: API
slug: scalable-infrastructure-finops
source_filename: scalable-infrastructure-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scalable Infrastructure\nproviderId: scalable-infrastructure\npublisherName: Scalable Infrastructure\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cloud Infrastructure\n  - Compute\n  - DevOps\n  - Infrastructure as Code\n  - Kubernetes\n  - Networking\n  - Scalability\n  - Storage\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scalable Infrastructure API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scalable Infrastructure\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scalable Infrastructure\n  PublisherName: Scalable Infrastructure\n  InvoiceIssuerName: Scalable Infrastructure\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: AWS EC2 API\n    baseURL: ''\n    tags:\n      - Amazon Web Services\n      - Cloud\n      - Compute\n      - EC2\n      - Infrastructure\n      - Instances\n    serviceName: AWS EC2 API\n    serviceCategory: API\n  - name: AWS VPC API\n    baseURL: ''\n    tags:\n      - Amazon Web Services\n      - Cloud\n      - Infrastructure\n      - Networking\n      - Security\n      - VPC\n    serviceName: AWS VPC API\n    serviceCategory: API\n  - name: AWS EKS API\n    baseURL: ''\n    tags:\n      - Amazon Web Services\n      - Cloud\n\
  \      - Containers\n      - EKS\n      - Kubernetes\n      - Managed Service\n    serviceName: AWS EKS API\n    serviceCategory: API\n  - name: Google Compute Engine API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Compute\n      - Google Cloud\n      - Infrastructure\n      - Instances\n      - Virtual Machines\n    serviceName: Google Compute Engine API\n    serviceCategory: API\n  - name: Google Kubernetes Engine API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Containers\n      - GKE\n      - Google Cloud\n      - Kubernetes\n      - Managed Service\n    serviceName: Google Kubernetes Engine API\n    serviceCategory: API\n  - name: Azure Resource Manager API\n    baseURL: ''\n    tags:\n      - Azure\n      - Cloud\n      - Infrastructure\n      - Management\n      - Microsoft\n      - Resource Management\n    serviceName: Azure Resource Manager API\n    serviceCategory: API\n  - name: Azure AKS API\n    baseURL: ''\n    tags:\n      - AKS\n      - Azure\n      - Cloud\n\
  \      - Containers\n      - Kubernetes\n      - Managed Service\n    serviceName: Azure AKS API\n    serviceCategory: API\n  - name: DigitalOcean API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Compute\n      - Developer-Friendly\n      - DigitalOcean\n      - Infrastructure\n      - Kubernetes\n    serviceName: DigitalOcean API\n    serviceCategory: API\n  - name: Terraform Registry API\n    baseURL: ''\n    tags:\n      - Infrastructure as Code\n      - IaC\n      - Open Source\n      - Provisioning\n      - Terraform\n    serviceName: Terraform Registry API\n    serviceCategory: API\n  - name: Pulumi Cloud API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Infrastructure as Code\n      - IaC\n      - Open Source\n      - Provisioning\n      - Pulumi\n    serviceName: Pulumi Cloud API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric:\
  \ billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalable-infrastructure/refs/heads/main/finops/scalable-infrastructure-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Infrastructure
- Compute
- DevOps
- Infrastructure as Code
- Kubernetes
- Networking
- Scalability
- Storage
- FinOps
- Cost Management
- FOCUS
---
