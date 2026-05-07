---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-ecs-openapi.yml
  format: yaml
  label: Amazon ECS API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-ecs/refs/heads/main/openapi/amazon-ecs-openapi.yml
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
description: 'FOCUS-aligned FinOps for Amazon ECS: ECS API and orchestration are free; cost arises from the launch type (Fargate vCPU/memory-seconds, EC2 instance-hours, or ECS Managed Instance fees) and associated resources.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  PricingCategory: On-Demand
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: Compute
  ServiceName: Amazon Elastic Container Service
  ServiceSubcategory: Containers
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - cluster
  - service
  - task_definition
  - cpu_architecture
  name: fargate_vcpu_seconds
  unit: vCPU-second
- aggregation: sum
  dimensions:
  - region
  - cluster
  - service
  - task_definition
  name: fargate_memory_seconds
  unit: GB-second
- aggregation: sum
  dimensions:
  - region
  - instance_type
  - cluster
  - capacity_provider
  name: ec2_instance_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - instance_type
  name: managed_instance_fee
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - direction
  name: data_transfer
  unit: GB
name: Amazon Ecs Finops
provider_name: Amazon ECS
provider_slug: amazon-ecs
publisher_name: Amazon Web Services, Inc.
service_category: Compute / Containers
slug: amazon-ecs-finops
source_filename: amazon-ecs-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/ecs/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon ECS\nproviderId: amazon-ecs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - Containers\n  - ECS\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon ECS: ECS API and orchestration are free; cost arises from\n  the launch type (Fargate vCPU/memory-seconds, EC2 instance-hours, or ECS Managed Instance fees) and\n  associated resources.'\nsources:\n  - https://aws.amazon.com/ecs/pricing/\n  - https://aws.amazon.com/fargate/pricing/\n  - https://aws.amazon.com/aws-cost-management/aws-cost-explorer/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Compute / Containers\n\
  billingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Amazon Elastic Container Service\n  ServiceCategory: Compute\n  ServiceSubcategory: Containers\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory: On-Demand\nmeters:\n  - name: fargate_vcpu_seconds\n    unit: vCPU-second\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n      - service\n      - task_definition\n      - cpu_architecture\n  - name: fargate_memory_seconds\n    unit: GB-second\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n      - service\n      - task_definition\n  - name: ec2_instance_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n   \
  \   - region\n      - instance_type\n      - cluster\n      - capacity_provider\n  - name: managed_instance_fee\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - instance_type\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - direction\nprinciples:\n  - name: Visibility\n    description: Use AWS Cost Explorer with the ECS dimension, AWS CUR/CUR 2.0 (FOCUS export), and CloudWatch\n      Container Insights to attribute spend to clusters, services, and tasks.\n  - name: Allocation\n    description: Apply user-defined tags (Environment, Team, Application) on clusters, services, and task\n      definitions; enable cost allocation tags in Billing.\n  - name: Optimization\n    description: Pick the right launch type per workload (Fargate Spot, EC2 Spot via capacity providers),\n      right-size CPU/memory in task definitions, use ARM/Graviton, commit to Compute Savings Plans for\n      steady baseline.\n\
  \  - name: Accountability\n    description: Set AWS Budgets per account/tag, configure anomaly detection, hold service owners accountable\n      via showback/chargeback from CUR.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Amazon Web Services\n    email: support@aws.amazon.com\n    url: https://aws.amazon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-ecs/refs/heads/main/finops/amazon-ecs-finops.yml
sources:
- https://aws.amazon.com/ecs/pricing/
- https://aws.amazon.com/fargate/pricing/
- https://aws.amazon.com/aws-cost-management/aws-cost-explorer/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Containers
- ECS
- Cost Management
---
