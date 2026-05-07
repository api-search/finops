---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: deno-deploy-rest-api-openapi.yml
  format: yaml
  label: Deno Deploy REST API
  slug: deploy-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deno/refs/heads/main/openapi/deno-deploy-rest-api-openapi.yml
- filename: deno-deploy-v2-api-openapi.yml
  format: yaml
  label: Deno Deploy API V2
  slug: deploy-v2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deno/refs/heads/main/openapi/deno-deploy-v2-api-openapi.yml
- filename: deno-subhosting-api-openapi.yml
  format: yaml
  label: Deno Subhosting API
  slug: subhosting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deno/refs/heads/main/openapi/deno-subhosting-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Tiered Subscription + Pay-As-You-Go Overage
description: 'FOCUS-aligned FinOps for Deno Deploy: tiered subscription (Free / Pro $20 / Builder $200 / Enterprise) with included monthly quotas plus pay-as-you-go overage on requests, bandwidth, CPU/memory time, and KV storage and operations.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Deno Land Inc.
  PricingCategory: Subscription + Usage-Based
  PricingUnit: varies
  ProviderName: Deno
  PublisherName: Deno Land Inc.
  ServiceCategory: Edge Compute / Serverless Runtime
  ServiceName: Deno Deploy
layout: finops
meters:
- aggregation: sum
  description: Monthly Pro / Builder / Enterprise subscription fee
  dimensions:
  - plan
  - organization
  name: subscription_fee
  unit: month
- aggregation: sum
  description: HTTP requests served by deployments
  dimensions:
  - organization
  - deployment
  - region
  name: requests
  unit: request
- aggregation: sum
  description: Outbound network bandwidth from deployments
  dimensions:
  - organization
  - deployment
  - region
  name: bandwidth_egress
  unit: GB
- aggregation: sum
  description: Wall-clock CPU time consumed by isolates
  dimensions:
  - organization
  - deployment
  name: cpu_time
  unit: hour
- aggregation: sum
  description: Memory-time product (memory allocation x duration)
  dimensions:
  - organization
  - deployment
  name: memory_time
  unit: GB-hour
- aggregation: max
  description: Resident KV storage volume
  dimensions:
  - organization
  name: kv_storage
  unit: GB
- aggregation: sum
  description: KV read operations
  dimensions:
  - organization
  name: kv_reads
  unit: read
- aggregation: sum
  description: KV write operations
  dimensions:
  - organization
  name: kv_writes
  unit: write
- aggregation: max
  description: Resident volume storage
  dimensions:
  - organization
  name: volume_storage
  unit: GB-month
name: Deno Finops
provider_name: Deno
provider_slug: deno
publisher_name: Deno Land Inc.
service_category: Edge Compute / Serverless Runtime
slug: deno-finops
source_filename: deno-finops.yml
source_heading: FinOps Profile
source_url: https://deno.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Deno\nproviderId: deno\npublisherName: Deno Land Inc.\nserviceCategory: Edge Compute / Serverless Runtime\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Edge Compute\n  - Serverless\n  - JavaScript\n  - Runtime\n  - TypeScript\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Deno Deploy: tiered subscription (Free / Pro $20 / Builder $200\n  / Enterprise) with included monthly quotas plus pay-as-you-go overage on requests, bandwidth, CPU/memory\n  time, and KV storage and operations.'\nsources:\n  - https://deno.com/pricing\n  - https://docs.deno.com/deploy/manual/pricing-and-limits\nprinciples:\n  - name: Visibility\n    description:\
  \ Use the Deno Deploy dashboard's usage and billing pages plus the alert-threshold and\n      hard spending-limit controls to monitor request, bandwidth, CPU/memory, and KV consumption per organization\n      in near real time.\n  - name: Allocation\n    description: Tag spend by Deno organization, project, and deployment. Use separate organizations per\n      cost-center where strict allocation is needed since billing rolls up at the org level.\n  - name: Optimization\n    description: Right-size memory and isolate behavior, cache aggressively at the edge to reduce request\n      counts, compress responses to lower egress GB, and prefer KV reads (cheaper) over writes; consolidate\n      deployments to stay inside the included CPU/memory-time quotas.\n  - name: Accountability\n    description: Set hard spending limits per organization to bound overage from traffic spikes, and assign\n      a billing owner for each Deploy organization in the dashboard's billing settings.\ndomains:\n  -\
  \ name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Tiered Subscription + Pay-As-You-Go Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency:\
  \ Recurring\nfocusColumns:\n  ServiceName: Deno Deploy\n  ServiceCategory: Edge Compute / Serverless Runtime\n  ProviderName: Deno\n  PublisherName: Deno Land Inc.\n  InvoiceIssuerName: Deno Land Inc.\n  PricingCategory: Subscription + Usage-Based\n  PricingUnit: varies\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: subscription_fee\n    description: Monthly Pro / Builder / Enterprise subscription fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - organization\n  - name: requests\n    description: HTTP requests served by deployments\n    unit: request\n    aggregation: sum\n    dimensions:\n      - organization\n      - deployment\n      - region\n  - name: bandwidth_egress\n    description: Outbound network bandwidth from deployments\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - organization\n      - deployment\n      - region\n  - name: cpu_time\n    description: Wall-clock CPU time consumed by isolates\n    unit:\
  \ hour\n    aggregation: sum\n    dimensions:\n      - organization\n      - deployment\n  - name: memory_time\n    description: Memory-time product (memory allocation x duration)\n    unit: GB-hour\n    aggregation: sum\n    dimensions:\n      - organization\n      - deployment\n  - name: kv_storage\n    description: Resident KV storage volume\n    unit: GB\n    aggregation: max\n    dimensions:\n      - organization\n  - name: kv_reads\n    description: KV read operations\n    unit: read\n    aggregation: sum\n    dimensions:\n      - organization\n  - name: kv_writes\n    description: KV write operations\n    unit: write\n    aggregation: sum\n    dimensions:\n      - organization\n  - name: volume_storage\n    description: Resident volume storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - organization\napis:\n  - name: Deno Deploy REST API\n    baseURL: https://api.deno.com/v1\n    tags:\n      - Deployment\n      - Edge\n      - Management\n      - Serverless\n\
  \    serviceName: Deno Deploy REST API\n    serviceCategory: API\n  - name: Deno Deploy API V2\n    baseURL: https://api.deno.com/v2\n    tags:\n      - Deployment\n      - Edge\n      - Management\n      - Serverless\n    serviceName: Deno Deploy API V2\n    serviceCategory: API\n  - name: Deno KV API\n    baseURL: https://api.deno.com\n    tags:\n      - Database\n      - Edge\n      - Key-Value\n      - Storage\n    serviceName: Deno KV API\n    serviceCategory: API\n  - name: Deno Subhosting API\n    baseURL: https://api.deno.com/v1\n    tags:\n      - Deployment\n      - Multi-Tenant\n      - Serverless\n      - Subhosting\n    serviceName: Deno Subhosting API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1M Requests\n    metric: billed_cost / (requests / 1000000)\n    target: '$2 above included; $0 within plan quota'\n  - name: Cost per GB Egress\n    metric: bandwidth_cost / bandwidth_gb\n    target: '$0.50 above included'\n  - name: Cost per Active Deployment\n\
  \    metric: billed_cost / active_deployments\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/deno/refs/heads/main/finops/deno-finops.yml
sources:
- https://deno.com/pricing
- https://docs.deno.com/deploy/manual/pricing-and-limits
specification: FinOps Framework
tags:
- Edge Compute
- Serverless
- JavaScript
- Runtime
- TypeScript
- FinOps
- Cost Management
- FOCUS
---
