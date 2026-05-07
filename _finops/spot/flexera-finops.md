---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spot-administration-api-openapi.yml
  format: yaml
  label: Spot Administration API
  slug: administration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-administration-api-openapi.yml
- filename: spot-elastigroup-api-openapi.yml
  format: yaml
  label: Spot Elastigroup API
  slug: elastigroup-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-elastigroup-api-openapi.yml
- filename: spot-ocean-api-openapi.yml
  format: yaml
  label: Spot Ocean API
  slug: ocean-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-ocean-api-openapi.yml
- filename: spot-eco-api-openapi.yml
  format: yaml
  label: Spot Eco API
  slug: eco-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-eco-api-openapi.yml
- filename: spot-billing-engine-api-openapi.yml
  format: yaml
  label: Spot Billing Engine API
  slug: billing-engine-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/openapi/spot-billing-engine-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Savings Share
description: FOCUS-aligned FinOps mapping for Spot (by Flexera) — savings-share billing on Eco/Ocean/Elastigroup with cloud-spend-under-management as the primary meter. Spot itself is a FinOps tool, so this artifact also describes the meters consumers should expose to their own FinOps practice.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Flexera Software LLC
  ProviderName: Flexera Software LLC
  PublisherName: Flexera Software LLC
  ServiceCategory: FinOps / Cloud Cost Optimization
  ServiceName: Spot by NetApp / Flexera
layout: finops
meters:
- aggregation: sum
  description: Net cloud savings delivered by Spot Eco (commitment portfolio optimization) — primary basis for savings-share billing
  dimensions:
  - cloud_provider
  - account
  - service
  name: net_savings_delivered
  unit: USD
- aggregation: sum
  description: Compute hours under management by Elastigroup / Ocean
  dimensions:
  - cloud_provider
  - region
  - cluster
  - instance_family
  name: managed_compute_hours
  unit: instance-hour
- aggregation: avg
  description: Reserved-instance / Savings-Plan / CUD volume managed by Eco
  dimensions:
  - cloud_provider
  - commitment_type
  name: commitments_managed
  unit: USD
- aggregation: max
  description: Kubernetes clusters managed by Spot Ocean
  dimensions:
  - cloud_provider
  - region
  name: managed_clusters
  unit: cluster-month
name: Flexera Finops
provider_name: Spot
provider_slug: spot
publisher_name: Flexera Software LLC
service_category: FinOps / Cloud Cost Optimization
slug: flexera-finops
source_filename: flexera-finops.yml
source_heading: FinOps Profile
source_url: https://www.flexera.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Spot\nproviderId: spot\npublisherName: Flexera Software LLC\nserviceCategory: FinOps / Cloud Cost Optimization\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud Cost Optimization\n  - Kubernetes\n  - Spot Instances\ndescription: FOCUS-aligned FinOps mapping for Spot (by Flexera) — savings-share billing on Eco/Ocean/Elastigroup with cloud-spend-under-management as the primary meter. Spot itself is a FinOps tool, so this artifact also describes the meters consumers should expose to their own FinOps practice.\nnotes: Public pricing is contact-sales; meters reflect documented Spot product behavior\
  \ (compute hours managed, commitments managed, net savings delivered).\nsources:\n  - https://www.flexera.com/products\n  - https://spot.io/products/\nbillingModel:\n  pricingCategory: Savings Share\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Spot by NetApp / Flexera\n  ServiceCategory: FinOps / Cloud Cost Optimization\n  ProviderName: Flexera Software LLC\n  PublisherName: Flexera Software LLC\n  InvoiceIssuerName: Flexera Software LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: net_savings_delivered\n    description: Net cloud savings delivered by Spot Eco (commitment portfolio optimization) — primary basis for savings-share billing\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - cloud_provider\n      - account\n      - service\n  - name: managed_compute_hours\n    description: Compute hours under management by Elastigroup /\
  \ Ocean\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud_provider\n      - region\n      - cluster\n      - instance_family\n  - name: commitments_managed\n    description: Reserved-instance / Savings-Plan / CUD volume managed by Eco\n    unit: USD\n    aggregation: avg\n    dimensions:\n      - cloud_provider\n      - commitment_type\n  - name: managed_clusters\n    description: Kubernetes clusters managed by Spot Ocean\n    unit: cluster-month\n    aggregation: max\n    dimensions:\n      - cloud_provider\n      - region\nprinciples:\n  - name: Visibility\n    description: Pull Spot's Cloud Analyzer and Eco reporting daily; reconcile reported \"net savings\" against your CUR/Cost-and-Usage report to validate the savings-share invoice.\n  - name: Allocation\n    description: Tag clusters and groups in Spot with cost-center metadata so Spot's allocation views align with FOCUS dimensions you use for chargeback.\n  - name: Optimization\n    description: Spot\
  \ is itself the optimization layer — measure unit-cost (cost per pod-hour, cost per instance-hour) before/after enabling Ocean and Eco and tune autoscaling policies based on observed savings.\n  - name: Accountability\n    description: Cloud platform / FinOps team owns the Spot relationship; finance audits the savings-share invoice against independent CUR-based savings calculations quarterly.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spot/refs/heads/main/finops/flexera-finops.yml
sources:
- https://www.flexera.com/products
- https://spot.io/products/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud Cost Optimization
- Kubernetes
- Spot Instances
---
