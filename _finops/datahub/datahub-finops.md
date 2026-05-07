---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: datahub-openapi-openapi.yml
  format: yaml
  label: DataHub OpenAPI
  slug: datahub-openapi
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datahub/refs/heads/main/openapi/datahub-openapi-openapi.yml
- filename: datahub-actions-asyncapi.yml
  format: yaml
  label: DataHub Actions Framework
  slug: datahub-actions-framework
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/datahub/refs/heads/main/asyncapi/datahub-actions-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Open Source
description: 'FOCUS-aligned FinOps for DataHub: bifurcated billing model. DataHub Core is open source and produces no vendor invoice — cost is the underlying Kafka, Elasticsearch, and SQL infrastructure. DataHub Cloud is a managed subscription from Acryl Data sized by data scale and user count; per-unit prices are not public.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Acryl Data, Inc.
  PricingCategory: Subscription
  ProviderName: DataHub (Acryl Data)
  PublisherName: Acryl Data, Inc.
  ServiceCategory: Data Catalog
  ServiceName: DataHub
  ServiceSubcategory: Metadata Management
layout: finops
meters:
- aggregation: max
  description: Count of metadata entities (datasets, dashboards, ML models, etc.) cataloged in DataHub. Common scaling dimension for the Cloud SKU.
  dimensions:
  - environment
  - tenant
  - asset_type
  name: catalog_assets
  unit: asset
- aggregation: max
  description: Active user count consuming DataHub UI and APIs.
  dimensions:
  - tenant
  - role
  name: active_users
  unit: seat
- aggregation: sum
  description: Metadata change events written through the emitter / CLI / Actions framework.
  dimensions:
  - source
  - tenant
  name: ingestion_events
  unit: event
- aggregation: avg
  description: Underlying storage for the metadata graph (Elasticsearch indices, Kafka retention, SQL primary store). Self-hosted operators see this on their cloud bill; Cloud customers see it as part of the subscription.
  dimensions:
  - backend
  - tenant
  name: storage_gb
  unit: GB-month
name: Datahub Finops
provider_name: DataHub
provider_slug: datahub
publisher_name: Acryl Data, Inc.
service_category: Data Catalog
slug: datahub-finops
source_filename: datahub-finops.yml
source_heading: FinOps Profile
source_url: https://datahub.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: DataHub\nproviderId: datahub\npublisherName: Acryl Data, Inc.\nserviceCategory: Data Catalog\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Data Catalog\n  - Data Governance\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for DataHub: bifurcated billing model. DataHub Core is open\n  source and produces no vendor invoice — cost is the underlying Kafka, Elasticsearch, and SQL\n  infrastructure. DataHub Cloud is a managed subscription from Acryl Data sized by data scale and\n  user count; per-unit prices are not public.'\nsources:\n  - https://datahub.com/\n  - https://datahubproject.io/docs/\n\
  notes: No public per-unit pricing for DataHub Cloud; Core is OSS. Meters describe likely billable\n  shape (assets cataloged, users, ingestion volume) but cannot be reconciled to a public price.\nbillingModel:\n  pricingCategory: Subscription + Open Source\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: DataHub\n  ServiceCategory: Data Catalog\n  ServiceSubcategory: Metadata Management\n  ProviderName: DataHub (Acryl Data)\n  PublisherName: Acryl Data, Inc.\n  InvoiceIssuerName: Acryl Data, Inc.\n  PricingCategory: Subscription\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: catalog_assets\n    description: Count of metadata entities (datasets, dashboards, ML models, etc.) cataloged in\n      DataHub. Common scaling dimension for the Cloud SKU.\n    unit: asset\n    aggregation: max\n    dimensions:\n      - environment\n      - tenant\n      - asset_type\n  -\
  \ name: active_users\n    description: Active user count consuming DataHub UI and APIs.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n      - role\n  - name: ingestion_events\n    description: Metadata change events written through the emitter / CLI / Actions framework.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - source\n      - tenant\n  - name: storage_gb\n    description: Underlying storage for the metadata graph (Elasticsearch indices, Kafka retention,\n      SQL primary store). Self-hosted operators see this on their cloud bill; Cloud customers see\n      it as part of the subscription.\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - backend\n      - tenant\nprinciples:\n  - name: Visibility\n    description: For DataHub Core, join Kafka / Elasticsearch / SQL cost from the underlying cloud\n      provider. For DataHub Cloud, use the customer admin console for asset, user, and ingestion\n      counts and join with the\
  \ Acryl invoice.\n  - name: Allocation\n    description: Tag deployments by team and environment; allocate DataHub Core spend through the\n      cloud provider's tag-driven cost report. For Cloud, attribute the contract by the originating\n      data domain or platform team.\n  - name: Optimization\n    description: Prune unused or stale entities to keep asset counts under contractual ceilings,\n      tune Elasticsearch shard sizing, and reduce ingestion frequency for slow-changing sources.\n      Use scheduled rather than streaming ingestion where freshness allows.\n  - name: Accountability\n    description: Platform / data-engineering teams typically own the DataHub bill; downstream\n      consumers should be assigned ownership of their entities so unused assets can be reaped.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/datahub/refs/heads/main/finops/datahub-finops.yml
sources:
- https://datahub.com/
- https://datahubproject.io/docs/
specification: FinOps Framework
tags:
- Data Catalog
- Data Governance
- Open Source
- FinOps
- FOCUS
---
