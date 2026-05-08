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
  - Adjustment
  pricingCategory: Pass-Through Vendor Spend
description: FOCUS-aligned FinOps view for the APIs.io Engineering Platform — a federation of third-party vendors (AWS, GitHub, Cloudflare, Bing, Postman, EasyCron). The FinOps practice rolls up the line items from each vendor invoice rather than billing through a single platform meter.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: per-vendor (AWS, GitHub, Cloudflare, Microsoft, Postman, EasyCron)
  ProviderName: APIs.io
  PublisherName: APIs.io
  ServiceCategory: Federated Engineering Platform
  ServiceName: APIs.io Engineering Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - account
  - region
  name: aws_spend
  unit: USD
- aggregation: sum
  dimensions:
  - product
  - org
  name: github_spend
  unit: USD
- aggregation: sum
  dimensions:
  - product
  - account
  name: cloudflare_spend
  unit: USD
- aggregation: sum
  dimensions:
  - vendor
  - product
  name: saas_spend
  unit: USD
name: Engineering Platform Finops
provider_name: APIs.io Engineering Platform
provider_slug: apis-io-engineering-platform
publisher_name: APIs.io
service_category: Federated Engineering Platform
slug: engineering-platform-finops
source_filename: engineering-platform-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/api-search/engineering-platform
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: APIs.io Engineering Platform\nproviderId: apis-io-engineering-platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - APIs.io\n  - Engineering\n  - Platform\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps view for the APIs.io Engineering Platform — a federation of third-party\n  vendors (AWS, GitHub, Cloudflare, Bing, Postman, EasyCron). The FinOps practice rolls up the line items\n  from each vendor invoice rather than billing through a single platform meter.\nnotes: Spend originates with the underlying vendors; reconcile against each vendor's billing/usage API\n  (AWS Cost Explorer / CUR, GitHub billing, Cloudflare billing, Microsoft Azure Cost Management for Bing,\n  Postman billing, EasyCron invoices).\nsources:\n  - https://github.com/api-search/engineering-platform\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: APIs.io\nserviceCategory: Federated Engineering Platform\nbillingModel:\n  pricingCategory: Pass-Through Vendor Spend\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: APIs.io Engineering Platform\n  ServiceCategory: Federated Engineering Platform\n  ProviderName: APIs.io\n  PublisherName: APIs.io\n  InvoiceIssuerName: per-vendor (AWS, GitHub, Cloudflare, Microsoft, Postman, EasyCron)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: aws_spend\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - service\n      - account\n      - region\n  - name: github_spend\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product\n      - org\n  - name: cloudflare_spend\n\
  \    unit: USD\n    aggregation: sum\n    dimensions:\n      - product\n      - account\n  - name: saas_spend\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - vendor\n      - product\nprinciples:\n  - name: Visibility\n    description: Pull each vendor's billing data (AWS CUR, GitHub billing API, Cloudflare billing, Postman\n      billing) into a single dashboard for unified APIs.io platform visibility.\n  - name: Allocation\n    description: Tag every vendor account / project with the consuming APIs.io workload so spend can be\n      attributed back to the team or product.\n  - name: Optimization\n    description: Optimization is per-vendor — Reserved Instances and Savings Plans on AWS, plan-tier review\n      on GitHub/Cloudflare/Postman, request batching for paid Bing search.\n  - name: Accountability\n    description: APIs.io engineering owns the federation; per-vendor budgets and alerts are configured\n      in each vendor console with monthly review.\nmaintainers:\n\
  \  - FN: Kin Lane\n    X-twitter: apievangelist\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apis-io-engineering-platform/refs/heads/main/finops/engineering-platform-finops.yml
sources:
- https://github.com/api-search/engineering-platform
specification: FinOps Framework
tags:
- APIs.io
- Engineering
- Platform
- FinOps
- FOCUS
---
