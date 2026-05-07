---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: AWS Lambda API
  slug: aws-lambda-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/lambda/2015-03-31/openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for AWS Lambda: pay-as-you-go billing on requests + GB-seconds with separate meters for x86 vs ARM, provisioned concurrency, ephemeral storage above 512 MB, and data transfer. Compute Savings Plans give up to 17% discount.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  RegionId: varies
  ServiceCategory: Compute
  ServiceName: AWS Lambda
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - function_name
  - architecture
  name: requests
  unit: request
- aggregation: sum
  dimensions:
  - region
  - function_name
  - architecture
  - memory_size
  name: compute_gb_seconds
  unit: GB-second
- aggregation: sum
  dimensions:
  - region
  - function_name
  - architecture
  name: provisioned_concurrency_gb_seconds
  unit: GB-second
- aggregation: sum
  dimensions:
  - region
  - function_name
  name: provisioned_concurrency_executions
  unit: GB-second
- aggregation: sum
  dimensions:
  - region
  - function_name
  name: ephemeral_storage_gb_seconds
  unit: GB-second
- aggregation: sum
  dimensions:
  - region
  - destination
  name: data_transfer_out
  unit: GB
- aggregation: sum
  name: savings_plan_commitment
  unit: USD-hour
name: Aws Lambda Finops
provider_name: AWS Lambda
provider_slug: aws-lambda
publisher_name: Amazon Web Services, Inc.
service_category: Serverless Compute
slug: aws-lambda-finops
source_filename: aws-lambda-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/lambda/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AWS Lambda\nproviderId: aws-lambda\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Serverless\n  - Functions\n  - AWS\ndescription: 'FOCUS-aligned FinOps for AWS Lambda: pay-as-you-go billing on requests + GB-seconds with\n  separate meters for x86 vs ARM, provisioned concurrency, ephemeral storage above 512 MB, and data\n  transfer. Compute Savings Plans give up to 17% discount.'\nsources:\n  - https://aws.amazon.com/lambda/pricing/\n  - https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Serverless Compute\nbillingModel:\n\
  \  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: AWS Lambda\n  ServiceCategory: Compute\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  RegionId: varies\nmeters:\n  - name: requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - function_name\n      - architecture\n  - name: compute_gb_seconds\n    unit: GB-second\n    aggregation: sum\n    dimensions:\n      - region\n      - function_name\n      - architecture\n      - memory_size\n  - name: provisioned_concurrency_gb_seconds\n    unit: GB-second\n    aggregation: sum\n    dimensions:\n      - region\n      - function_name\n      - architecture\n  - name: provisioned_concurrency_executions\n    unit: GB-second\n    aggregation: sum\n \
  \   dimensions:\n      - region\n      - function_name\n  - name: ephemeral_storage_gb_seconds\n    unit: GB-second\n    aggregation: sum\n    dimensions:\n      - region\n      - function_name\n  - name: data_transfer_out\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - destination\n  - name: savings_plan_commitment\n    unit: USD-hour\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use CloudWatch Lambda Insights or the built-in Duration / Invocations / Errors metrics\n      per function. Cost Explorer breaks Lambda spend by UsageType (Lambda-Edge-Requests,\n      Lambda-GB-Second, Lambda-Provisioned-GB-Second, Lambda-Provisioned-Concurrency). The CUR\n      records per-function cost when functions are tagged.\n  - name: Allocation\n    description: Tag functions with team / product / environment cost allocation tags. Use\n      function-level tags (not just resource group) so the CUR splits cost by lambda:function-name.\n  - name:\
  \ Optimization\n    description: 'Top levers: (1) move to ARM/Graviton2 for ~20% compute savings; (2) right-size memory\n      using AWS Lambda Power Tuning to find the cost-minimum point (memory drives both CPU and\n      duration); (3) use provisioned concurrency only where cold-start tail latency hurts SLO;\n      (4) cap ephemeral storage near the 512 MB free included; (5) buy Compute Savings Plans for\n      stable baseline; (6) prefer asynchronous / event-source invocation for non-user-facing\n      workloads.'\n  - name: Accountability\n    description: Platform team typically owns Lambda governance (concurrency quotas, savings plan\n      commitment); each function's owning team is on the hook for memory size, runtime cost, and\n      cold-start mitigation in their service.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aws-lambda/refs/heads/main/finops/aws-lambda-finops.yml
sources:
- https://aws.amazon.com/lambda/pricing/
- https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Serverless
- Functions
---
