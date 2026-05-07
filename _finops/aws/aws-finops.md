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
  label: Amazon EC2
  slug: amazon-ec2
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/ec2/2016-11-15/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon S3
  slug: amazon-s3
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/s3/2006-03-01/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Lambda
  slug: amazon-lambda
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/lambda/2015-03-31/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon DynamoDB
  slug: amazon-dynamodb
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/dynamodb/2012-08-10/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon RDS
  slug: amazon-rds
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/rds/2014-10-31/openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Amazon Web Services (AWS).
focus_columns:
  BillingCurrency: USD
  ProviderName: Amazon Web Services (AWS)
  PublisherName: Amazon Web Services (AWS)
  ServiceCategory: Cloud Infrastructure
  ServiceName: Amazon Web Services (AWS)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - region
  - instance_type
  - tenant
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - service
  - tier
  name: storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - egress_type
  - region_pair
  name: data_transfer
  unit: GB
- aggregation: sum
  dimensions:
  - service
  - operation
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - service
  name: managed_services
  unit: varies
name: Aws Finops
provider_name: Amazon Web Services (AWS)
provider_slug: aws
publisher_name: Amazon Web Services (AWS)
service_category: Cloud Infrastructure
slug: aws-finops
source_filename: aws-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon Web Services (AWS)\nproviderId: aws\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud Infrastructure\ndescription: FOCUS-aligned FinOps for Amazon Web Services (AWS).\nsources:\n  - https://aws.amazon.com/pricing/\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services (AWS)\nserviceCategory: Cloud Infrastructure\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Amazon Web Services (AWS)\n  ServiceCategory: Cloud Infrastructure\n  ProviderName: Amazon Web Services (AWS)\n  PublisherName:\
  \ Amazon Web Services (AWS)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Amazon Web Services (AWS) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend\
  \ alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aws/refs/heads/main/finops/aws-finops.yml
sources:
- https://aws.amazon.com/pricing/
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud Infrastructure
---
