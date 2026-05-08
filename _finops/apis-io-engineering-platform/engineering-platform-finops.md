---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aws-s3-openapi-original.yml
  format: yaml
  label: Amazon S3
  slug: aws-s3
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/aws-s3-openapi-original.yml
- filename: aws-lambda-openapi-original.yml
  format: yaml
  label: AWS Lambda
  slug: aws-lambda
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/aws-lambda-openapi-original.yml
- filename: aws-api-gateway-openapi-original.yml
  format: yaml
  label: AWS API Gateway
  slug: aws-api-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/aws-api-gateway-openapi-original.yml
- filename: aws-rds-openapi-original.yml
  format: yaml
  label: AWS RDS
  slug: aws-rds
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/aws-rds-openapi-original.yml
- filename: aws-iam-openapi-original.yml
  format: yaml
  label: AWS IAM
  slug: aws-iam
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/aws-iam-openapi-original.yml
- filename: microsoft-cognitive-web-search-openapi-original.yml
  format: yaml
  label: Microsoft Bing Search
  slug: microsoft-bing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/microsoft-cognitive-web-search-openapi-original.yml
- filename: postman-openapi-original.yml
  format: yaml
  label: Postman
  slug: postman
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/postman-openapi-original.yml
- filename: cloudflare-openapi-original.yml
  format: yaml
  label: Cloudflare
  slug: cloudflare
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/cloudflare-openapi-original.yml
- filename: github-openapi-original.yml
  format: yaml
  label: GitHub
  slug: github
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-search/engineering-platform/refs/heads/main/openapi/github-openapi-original.yml
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
description: FinOps framework definition for the APIs.io Engineering Platform API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: APIs.io Engineering Platform
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: APIs.io Engineering Platform
  PublisherName: APIs.io Engineering Platform
  ServiceCategory: Developer Tools / API
  ServiceName: APIs.io Engineering Platform
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
name: Engineering Platform Finops
provider_name: APIs.io Engineering Platform
provider_slug: apis-io-engineering-platform
publisher_name: APIs.io Engineering Platform
service_category: API
slug: engineering-platform-finops
source_filename: engineering-platform-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: APIs.io Engineering Platform\nproviderId: apis-io-engineering-platform\npublisherName: APIs.io Engineering Platform\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - APIs.io\n  - Engineering\n  - Platform\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the APIs.io Engineering Platform API surface. Provides a\n  FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the\n  provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: APIs.io Engineering Platform\n  ServiceCategory: Developer Tools / API\n  ProviderName: APIs.io Engineering Platform\n  PublisherName: APIs.io Engineering Platform\n  InvoiceIssuerName: APIs.io Engineering Platform\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon S3\n    baseURL: https://{bucketname}.s3.amazonaws.com\n    tags:\n      - Cloud\n      - Storage\n    serviceName: Amazon S3\n    serviceCategory: API\n  - name: AWS Lambda\n    baseURL: https://r275xc9bmd.execute-api.us-east-1.amazonaws.com\n    tags:\n      - Compute\n      - Execute\n      - Serverless\n    serviceName: AWS Lambda\n    serviceCategory: API\n  - name: AWS API Gateway\n    baseURL: http://api.example.com\n    tags:\n      - Gateway\n    serviceName: AWS API Gateway\n    serviceCategory: API\n  - name: AWS RDS\n    baseURL: http://api.example.com\n    tags:\n      - Database\n\
  \    serviceName: AWS RDS\n    serviceCategory: API\n  - name: AWS IAM\n    baseURL: http://api.example.com\n    tags:\n      - Access\n      - Identity\n      - Keys\n      - Tokens\n      - Users\n    serviceName: AWS IAM\n    serviceCategory: API\n  - name: Microsoft Bing Search\n    baseURL: https://api.bing.microsoft.com\n    tags:\n      - Search\n    serviceName: Microsoft Bing Search\n    serviceCategory: API\n  - name: Postman\n    baseURL: http://api.example.com\n    tags:\n      - Storage\n    serviceName: Postman\n    serviceCategory: API\n  - name: Cloudflare\n    baseURL: https://api.cloudflare.com/\n    tags:\n      - DNS\n    serviceName: Cloudflare\n    serviceCategory: API\n  - name: GitHub\n    baseURL: https://api.github.com\n    tags:\n      - Pipelines\n      - Source Control\n    serviceName: GitHub\n    serviceCategory: API\n  - name: VSCode\n    baseURL: ''\n    tags:\n      - IDE\n    serviceName: VSCode\n    serviceCategory: API\n  - name: EasyCron\n    baseURL:\
  \ https://api.easycron.com\n    tags:\n      - CRON\n      - Jobs\n      - Scheduling\n    serviceName: EasyCron\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    X-twitter: apievangelist\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apis-io-engineering-platform/refs/heads/main/finops/engineering-platform-finops.yml
sources: []
specification: FinOps Framework
tags:
- APIs.io
- Engineering
- Platform
- FinOps
- Cost Management
- FOCUS
---
