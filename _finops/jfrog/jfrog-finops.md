---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jfrog-artifactory-openapi.yml
  format: yaml
  label: JFrog Artifactory REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-artifactory-openapi.yml
- filename: jfrog-artifactory-openapi.yml
  format: yaml
  label: JFrog Artifactory REST API V2
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-artifactory-openapi.yml
- filename: jfrog-xray-openapi.yml
  format: yaml
  label: JFrog Xray REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-xray-openapi.yml
- filename: jfrog-distribution-openapi.yml
  format: yaml
  label: JFrog Distribution REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-distribution-openapi.yml
- filename: jfrog-pipelines-openapi.yml
  format: yaml
  label: JFrog Pipelines REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-pipelines-openapi.yml
- filename: jfrog-platform-openapi.yml
  format: yaml
  label: JFrog Platform REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-platform-openapi.yml
- filename: jfrog-access-openapi.yml
  format: yaml
  label: JFrog Access REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-access-openapi.yml
- filename: jfrog-curation-openapi.yml
  format: yaml
  label: JFrog Curation REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-curation-openapi.yml
- filename: jfrog-mission-control-openapi.yml
  format: yaml
  label: JFrog Mission Control REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-mission-control-openapi.yml
- filename: jfrog-release-lifecycle-openapi.yml
  format: yaml
  label: JFrog Release Lifecycle Management REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-release-lifecycle-openapi.yml
- filename: jfrog-workers-openapi.yml
  format: yaml
  label: JFrog Workers REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-workers-openapi.yml
- filename: jfrog-ml-openapi.yml
  format: yaml
  label: JFrog ML REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-ml-openapi.yml
- filename: jfrog-connect-openapi.yml
  format: yaml
  label: JFrog Connect REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-connect-openapi.yml
- filename: jfrog-catalog-openapi.yml
  format: yaml
  label: JFrog Catalog REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-catalog-openapi.yml
- filename: jfrog-evidence-openapi.yml
  format: yaml
  label: JFrog Evidence REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-evidence-openapi.yml
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
description: FinOps framework definition for the JFrog API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: JFrog
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: JFrog
  PublisherName: JFrog
  ServiceCategory: Developer Tools / API
  ServiceName: JFrog
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
name: Jfrog Finops
provider_name: JFrog
provider_slug: jfrog
publisher_name: JFrog
service_category: API
slug: jfrog-finops
source_filename: jfrog-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: JFrog\nproviderId: jfrog\npublisherName: JFrog\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Artifactory\n  - CI/CD\n  - Container Registry\n  - DevOps\n  - MLOps\n  - Package Management\n  - Security\n  - Software Supply Chain\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the JFrog API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: JFrog\n  ServiceCategory: Developer Tools / API\n  ProviderName: JFrog\n  PublisherName: JFrog\n  InvoiceIssuerName: JFrog\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: JFrog Artifactory REST API\n    baseURL: https://myserver.jfrog.io/artifactory/api\n    tags:\n      - Artifacts\n      - Binary Management\n      - DevOps\n      - Package Management\n      - Repository Management\n    serviceName: JFrog Artifactory REST API\n    serviceCategory: API\n  - name: JFrog Artifactory REST API V2\n    baseURL: https://myserver.jfrog.io/artifactory/api/v2\n    tags:\n      - API V2\n      - Artifacts\n      - Binary Management\n      - Package Management\n      - Repository Management\n    serviceName: JFrog Artifactory REST API V2\n    serviceCategory: API\n  - name: JFrog Xray REST API\n    baseURL: https://myserver.jfrog.io/xray/api\n    tags:\n  \
  \    - DevSecOps\n      - License Compliance\n      - Security\n      - Software Composition Analysis\n      - Vulnerability Scanning\n    serviceName: JFrog Xray REST API\n    serviceCategory: API\n  - name: JFrog Distribution REST API\n    baseURL: https://myserver.jfrog.io/distribution/api\n    tags:\n      - CDN\n      - Distribution\n      - Edge Nodes\n      - Release Management\n      - Software Distribution\n    serviceName: JFrog Distribution REST API\n    serviceCategory: API\n  - name: JFrog Pipelines REST API\n    baseURL: https://myserver.jfrog.io/pipelines/api\n    tags:\n      - Automation\n      - CI/CD\n      - DevOps\n      - Pipelines\n      - Workflows\n    serviceName: JFrog Pipelines REST API\n    serviceCategory: API\n  - name: JFrog Platform REST API\n    baseURL: https://myserver.jfrog.io/\n    tags:\n      - Access Management\n      - Administration\n      - Configuration\n      - Platform\n      - System Health\n    serviceName: JFrog Platform REST API\n    serviceCategory:\
  \ API\n  - name: JFrog Access REST API\n    baseURL: https://myserver.jfrog.io/access/api\n    tags:\n      - Access Management\n      - Authentication\n      - Permissions\n      - Tokens\n      - Users\n    serviceName: JFrog Access REST API\n    serviceCategory: API\n  - name: JFrog Curation REST API\n    baseURL: https://myserver.jfrog.io/curation/api\n    tags:\n      - Curation\n      - Open Source\n      - Policy Management\n      - Security\n      - Software Supply Chain\n    serviceName: JFrog Curation REST API\n    serviceCategory: API\n  - name: JFrog Mission Control REST API\n    baseURL: https://myserver.jfrog.io/mc/api\n    tags:\n      - Administration\n      - Mission Control\n      - Monitoring\n      - Multi-Instance Management\n      - Operations\n    serviceName: JFrog Mission Control REST API\n    serviceCategory: API\n  - name: JFrog Release Lifecycle Management REST API\n    baseURL: https://myserver.jfrog.io/lifecycle/api\n    tags:\n      - Evidence\n      - Lifecycle\n\
  \      - Promotion\n      - Release Bundles\n      - Release Management\n    serviceName: JFrog Release Lifecycle Management REST API\n    serviceCategory: API\n  - name: JFrog Workers REST API\n    baseURL: https://myserver.jfrog.io/worker/api\n    tags:\n      - Automation\n      - Extensibility\n      - Plugins\n      - Serverless\n      - Workers\n    serviceName: JFrog Workers REST API\n    serviceCategory: API\n  - name: JFrog ML REST API\n    baseURL: https://myserver.jfrog.io/ml/api\n    tags:\n      - AI\n      - Machine Learning\n      - MLOps\n      - Model Management\n      - Model Registry\n    serviceName: JFrog ML REST API\n    serviceCategory: API\n  - name: JFrog Connect REST API\n    baseURL: https://api.connect.jfrog.io/v2\n    tags:\n      - Device Management\n      - Edge Computing\n      - Fleet Management\n      - IoT\n      - OTA Updates\n    serviceName: JFrog Connect REST API\n    serviceCategory: API\n  - name: JFrog Catalog REST API\n    baseURL: https://myserver.jfrog.io/catalog/api/v1\n\
  \    tags:\n      - Catalog\n      - CVE Search\n      - Package Metadata\n      - Security\n      - Software Supply Chain\n    serviceName: JFrog Catalog REST API\n    serviceCategory: API\n  - name: JFrog Evidence REST API\n    baseURL: https://myserver.jfrog.io/evidence/api\n    tags:\n      - Attestation\n      - Compliance\n      - Evidence\n      - Software Supply Chain\n      - Supply Chain Security\n    serviceName: JFrog Evidence REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/finops/jfrog-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artifactory
- CI/CD
- Container Registry
- DevOps
- MLOps
- Package Management
- Security
- Software Supply Chain
- FinOps
- Cost Management
- FOCUS
---
