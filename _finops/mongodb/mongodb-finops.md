---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mongodb-atlas-openapi.yaml
  format: yaml
  label: MongoDB Atlas Administration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mongodb/refs/heads/main/openapi/mongodb-atlas-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Usage-Based
description: FOCUS-aligned FinOps for MongoDB Atlas.
focus_columns:
  BillingCurrency: USD
  ProviderName: MongoDB
  PublisherName: MongoDB, Inc.
  ServiceCategory: Database-as-a-Service
  ServiceName: MongoDB Atlas
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - tier
  - region
  - cloud
  name: cluster_hours
  unit: cluster-hour
- aggregation: sum
  name: serverless_reads
  unit: million_reads
- aggregation: sum
  name: serverless_writes
  unit: million_writes
- aggregation: sum
  name: data_transfer_inter_region
  unit: GB
- aggregation: sum
  name: data_transfer_internet
  unit: GB
- aggregation: max
  name: backup_storage
  unit: GB-month
- aggregation: sum
  name: atlas_search_indexes
  unit: search-index-hour
name: Mongodb Finops
provider_name: MongoDB
provider_slug: mongodb
publisher_name: MongoDB, Inc.
service_category: Database-as-a-Service
slug: mongodb-finops
source_filename: mongodb-finops.yml
source_heading: FinOps Profile
source_url: https://www.mongodb.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: MongoDB Atlas\nproviderId: mongodb\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Database\ndescription: FOCUS-aligned FinOps for MongoDB Atlas.\nsources:\n  - https://www.mongodb.com/pricing\n  - https://www.mongodb.com/pricing/calculator\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: MongoDB, Inc.\nserviceCategory: Database-as-a-Service\nbillingModel:\n  pricingCategory: Subscription + Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: MongoDB Atlas\n  ServiceCategory: Database-as-a-Service\n  ProviderName: MongoDB\n  PublisherName: MongoDB, Inc.\n  BillingCurrency: USD\nmeters:\n\
  \  - name: cluster_hours\n    unit: cluster-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - tier\n      - region\n      - cloud\n  - name: serverless_reads\n    unit: million_reads\n    aggregation: sum\n  - name: serverless_writes\n    unit: million_writes\n    aggregation: sum\n  - name: data_transfer_inter_region\n    unit: GB\n    aggregation: sum\n  - name: data_transfer_internet\n    unit: GB\n    aggregation: sum\n  - name: backup_storage\n    unit: GB-month\n    aggregation: max\n  - name: atlas_search_indexes\n    unit: search-index-hour\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use Atlas Cost Explorer per project; export billing JSON via Atlas Admin API.\n  - name: Allocation\n    description: Use projects per env/team; tag clusters for chargeback.\n  - name: Optimization\n    description: Right-size cluster tier; use Flex for unpredictable; serverless for spiky reads; cap\n      egress with VPC peering.\n  - name: Accountability\n\
  \    description: Per-project billing alerts; quarterly tier review using Performance Advisor.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mongodb/refs/heads/main/finops/mongodb-finops.yml
sources:
- https://www.mongodb.com/pricing
- https://www.mongodb.com/pricing/calculator
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Database
---
