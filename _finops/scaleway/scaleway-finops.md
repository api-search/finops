---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: scaleway-instance-openapi.yml
  format: yaml
  label: Scaleway Instance API
  slug: scaleway-instance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-instance-openapi.yml
- filename: scaleway-kubernetes-openapi.yml
  format: yaml
  label: Scaleway Kubernetes API
  slug: scaleway-kubernetes-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-kubernetes-openapi.yml
- filename: scaleway-iam-openapi.yml
  format: yaml
  label: Scaleway IAM API
  slug: scaleway-iam-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-iam-openapi.yml
- filename: scaleway-load-balancer-openapi.yml
  format: yaml
  label: Scaleway Load Balancer API
  slug: scaleway-load-balancer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-load-balancer-openapi.yml
- filename: scaleway-database-openapi.yml
  format: yaml
  label: Scaleway Managed Database API
  slug: scaleway-database-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-database-openapi.yml
- filename: scaleway-vpc-openapi.yml
  format: yaml
  label: Scaleway VPC API
  slug: scaleway-vpc-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-vpc-openapi.yml
- filename: scaleway-serverless-containers-openapi.yml
  format: yaml
  label: Scaleway Serverless Containers API
  slug: scaleway-serverless-containers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-serverless-containers-openapi.yml
- filename: scaleway-serverless-functions-openapi.yml
  format: yaml
  label: Scaleway Serverless Functions API
  slug: scaleway-serverless-functions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-serverless-functions-openapi.yml
- filename: scaleway-secret-manager-openapi.yml
  format: yaml
  label: Scaleway Secret Manager API
  slug: scaleway-secret-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-secret-manager-openapi.yml
- filename: scaleway-transactional-email-openapi.yml
  format: yaml
  label: Scaleway Transactional Email API
  slug: scaleway-transactional-email-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/openapi/scaleway-transactional-email-openapi.yml
billing_model:
  billingCurrency: EUR
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Scaleway: pay-as-you-go European cloud billed per second / per GB-month / per request across compute, storage, network, AI, and managed services, with a real-time Billing API for consumption and invoice export.'
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Scaleway SAS
  ProviderName: Scaleway
  PublisherName: Scaleway SAS
  ServiceCategory: Cloud Infrastructure
  ServiceName: Scaleway
layout: finops
meters:
- aggregation: sum
  dimensions:
  - instance_type
  - zone
  - project
  name: instance_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - volume_type
  - zone
  - project
  name: block_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - storage_class
  - region
  - project
  name: object_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - project
  name: public_ipv4
  unit: ip-month
- aggregation: sum
  dimensions:
  - cluster_type
  - region
  name: kubernetes_kapsule
  unit: cluster-hour
- aggregation: sum
  dimensions:
  - product
  - region
  - project
  name: serverless_invocations
  unit: request
- aggregation: sum
  dimensions:
  - model
  - direction
  - project
  name: generative_ai_tokens
  unit: token
name: Scaleway Finops
provider_name: Scaleway
provider_slug: scaleway
publisher_name: Scaleway SAS
service_category: Cloud Infrastructure
slug: scaleway-finops
source_filename: scaleway-finops.yml
source_heading: FinOps Profile
source_url: https://www.scaleway.com/en/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Scaleway\nproviderId: scaleway\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud Computing\n  - European Cloud\ndescription: 'FOCUS-aligned FinOps for Scaleway: pay-as-you-go European cloud billed per\n  second / per GB-month / per request across compute, storage, network, AI, and managed services,\n  with a real-time Billing API for consumption and invoice export.'\nsources:\n  - https://www.scaleway.com/en/pricing/\n  - https://www.scaleway.com/en/developers/api/billing/\n  - https://www.scaleway.com/en/developers/api/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Scaleway SAS\nserviceCategory: Cloud Infrastructure\nbillingModel:\n\
  \  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: EUR\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Scaleway\n  ServiceCategory: Cloud Infrastructure\n  ProviderName: Scaleway\n  PublisherName: Scaleway SAS\n  InvoiceIssuerName: Scaleway SAS\n  BillingCurrency: EUR\nmeters:\n  - name: instance_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - instance_type\n      - zone\n      - project\n  - name: block_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - volume_type\n      - zone\n      - project\n  - name: object_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - storage_class\n      - region\n      - project\n  - name: public_ipv4\n    unit: ip-month\n    aggregation: sum\n    dimensions:\n      - region\n      - project\n  - name: kubernetes_kapsule\n    unit: cluster-hour\n    aggregation: sum\n\
  \    dimensions:\n      - cluster_type\n      - region\n  - name: serverless_invocations\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - region\n      - project\n  - name: generative_ai_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - direction\n      - project\nprinciples:\n  - name: Visibility\n    description: Use the Scaleway Billing API (/billing/v2beta1/consumptions, /invoices,\n      /export-invoices) for real-time spend and CSV export; the console exposes per-project\n      cost dashboards.\n  - name: Allocation\n    description: Use Scaleway Projects and resource tags plus IAM to segregate spend per\n      team or environment; export invoices to CSV for chargeback.\n  - name: Optimization\n    description: Right-size between DEV / GP / PRO / Compute / Memory instance lines, use\n      per-second billing to shut idle workloads, prefer Object Storage Glacier class for\n      cold data, and negotiate committed-use\
  \ for predictable workloads.\n  - name: Accountability\n    description: Assign a project owner per Scaleway Project; reconcile monthly invoice\n      exports against the consumption API and investigate anomalies via the Billing API.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scaleway/refs/heads/main/finops/scaleway-finops.yml
sources:
- https://www.scaleway.com/en/pricing/
- https://www.scaleway.com/en/developers/api/billing/
- https://www.scaleway.com/en/developers/api/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud Computing
- European Cloud
---
