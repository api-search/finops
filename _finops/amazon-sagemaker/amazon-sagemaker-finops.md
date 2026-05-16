---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-sagemaker-openapi.yml
  format: yaml
  label: Amazon SageMaker API
  slug: amazon-sagemaker-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-sagemaker/refs/heads/main/openapi/amazon-sagemaker-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Amazon SageMaker AI: per-ML-instance-hour billing across notebook, training, batch transform, real-time, and asynchronous inference, plus serverless inference (GB-second + GB-data) and SageMaker Savings Plans for 1- or 3-year commitments.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: AI and Machine Learning
  ServiceName: Amazon SageMaker
  ServiceSubcategory: ML Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - instance_type
  - user
  name: notebook_instance_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - instance_type
  - job_name
  name: training_instance_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - instance_type
  - job_name
  name: batch_transform_instance_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - instance_type
  - endpoint_name
  - variant_name
  name: realtime_endpoint_instance_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - endpoint_name
  name: serverless_inference_gb_seconds
  unit: GB-second
- aggregation: sum
  dimensions:
  - region
  - endpoint_name
  name: serverless_inference_data_processed_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - workload
  name: storage_gb_month
  unit: GB-month
name: Amazon Sagemaker Finops
provider_name: Amazon SageMaker
provider_slug: amazon-sagemaker
publisher_name: Amazon Web Services, Inc.
service_category: AI / Machine Learning
slug: amazon-sagemaker-finops
source_filename: amazon-sagemaker-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/sagemaker-ai/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon SageMaker\nproviderId: amazon-sagemaker\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - Machine Learning\n  - SageMaker\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon SageMaker AI: per-ML-instance-hour billing across notebook,\n  training, batch transform, real-time, and asynchronous inference, plus serverless inference (GB-second\n  + GB-data) and SageMaker Savings Plans for 1- or 3-year commitments.'\nsources:\n  - https://aws.amazon.com/sagemaker-ai/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: AI / Machine Learning\nbillingModel:\n\
  \  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Amazon SageMaker\n  ServiceCategory: AI and Machine Learning\n  ServiceSubcategory: ML Platform\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: notebook_instance_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - instance_type\n      - user\n  - name: training_instance_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - instance_type\n      - job_name\n  - name: batch_transform_instance_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - instance_type\n      - job_name\n  - name: realtime_endpoint_instance_hours\n\
  \    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - instance_type\n      - endpoint_name\n      - variant_name\n  - name: serverless_inference_gb_seconds\n    unit: GB-second\n    aggregation: sum\n    dimensions:\n      - region\n      - endpoint_name\n  - name: serverless_inference_data_processed_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - endpoint_name\n  - name: storage_gb_month\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - workload\nprinciples:\n  - name: Visibility\n    description: Use SageMaker Studio cost dashboards, CloudWatch metrics (Invocations, ModelLatency, CPUUtilization,\n      GPUUtilization), and CUR / FOCUS export for per-job and per-endpoint spend.\n  - name: Allocation\n    description: Tag training jobs, endpoints, notebooks, and Studio profiles with Project, Team, Owner;\n      enable cost allocation tags so charges flow into FOCUS columns.\n  - name:\
  \ Optimization\n    description: Use Spot training for fault-tolerant jobs, right-size endpoint instance types, scale endpoints\n      to zero (Serverless or async) when traffic is sparse, commit to Savings Plans for steady inference,\n      use Inferentia/Trainium families for higher price-performance, and stop idle notebooks.\n  - name: Accountability\n    description: Set AWS Budgets per project tag, alert on training job duration anomalies, and review\n      monthly endpoint utilization against InvocationsPerInstance.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Amazon Web Services\n    email: support@aws.amazon.com\n    url: https://aws.amazon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-sagemaker/refs/heads/main/finops/amazon-sagemaker-finops.yml
sources:
- https://aws.amazon.com/sagemaker-ai/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Machine Learning
- SageMaker
- Cost Management
---
