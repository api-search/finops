---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: azure-management-openapi.yaml
  format: yaml
  label: Azure Compute API
  slug: azure-compute-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure/refs/heads/main/openapi/azure-management-openapi.yaml
- filename: azure-management-openapi.yaml
  format: yaml
  label: Azure Storage API
  slug: azure-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure/refs/heads/main/openapi/azure-management-openapi.yaml
- filename: azure-management-openapi.yaml
  format: yaml
  label: Azure Cognitive Services API
  slug: azure-cognitive-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure/refs/heads/main/openapi/azure-management-openapi.yaml
billing_model:
  billingCurrency: USD/EUR/GBP/local
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Microsoft Azure: hyperscale cloud platform with pay-as-you-go consumption metering across hundreds of services, augmented by reservations, savings plans, and enterprise agreements. Microsoft is a founding member of the FinOps Foundation and a primary contributor to the FOCUS specification; Azure Cost Management + Billing exports natively conform to FOCUS 1.0/1.1.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Pay-As-You-Go
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Cloud Infrastructure
  ServiceName: Microsoft Azure
layout: finops
meters:
- aggregation: sum
  description: Virtual machine, container, and serverless compute time
  dimensions:
  - region
  - sku
  - vm_family
  - subscription
  - resource_group
  name: compute_hours
  unit: instance-hour
- aggregation: avg
  description: Blob, file, queue, table, and disk storage
  dimensions:
  - region
  - storage_tier
  - redundancy
  name: storage_capacity
  unit: GB-month
- aggregation: sum
  description: Egress bandwidth across regions, AZs, internet
  dimensions:
  - source_region
  - destination
  name: data_transfer
  unit: GB
- aggregation: sum
  description: Service-specific transaction count (Storage, Cosmos DB, Functions, etc.)
  dimensions:
  - service
  - region
  name: api_transactions
  unit: transaction
- aggregation: max
  description: Per-seat / per-month subscriptions for managed offerings
  dimensions:
  - product
  name: licenses_subscriptions
  unit: seat
- aggregation: sum
  description: Committed-use commitments billed monthly across covered SKUs
  dimensions:
  - term
  - scope
  name: reservations_savings_plans
  unit: month
name: Azure Finops
provider_name: Microsoft Azure
provider_slug: azure
publisher_name: Microsoft Corporation
service_category: Cloud Infrastructure
slug: azure-finops
source_filename: azure-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Azure\nproviderId: azure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud Computing\n  - Infrastructure\n  - Platform as a Service\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Azure: hyperscale cloud platform with pay-as-you-go consumption\n  metering across hundreds of services, augmented by reservations, savings plans, and enterprise agreements.\n  Microsoft is a founding member of the FinOps Foundation and a primary contributor to the FOCUS specification;\n  Azure Cost Management + Billing exports natively conform to FOCUS 1.0/1.1.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/dataset-schema/cost-usage-details-focus\nalignedWith:\n  framework:\
  \ FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Cloud Infrastructure\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD/EUR/GBP/local\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Azure\n  ServiceCategory: Cloud Infrastructure\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Pay-As-You-Go\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: compute_hours\n    description: Virtual machine, container, and serverless compute time\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - sku\n      -\
  \ vm_family\n      - subscription\n      - resource_group\n  - name: storage_capacity\n    description: Blob, file, queue, table, and disk storage\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - storage_tier\n      - redundancy\n  - name: data_transfer\n    description: Egress bandwidth across regions, AZs, internet\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source_region\n      - destination\n  - name: api_transactions\n    description: Service-specific transaction count (Storage, Cosmos DB, Functions, etc.)\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n  - name: licenses_subscriptions\n    description: Per-seat / per-month subscriptions for managed offerings\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n  - name: reservations_savings_plans\n    description: Committed-use commitments billed monthly across covered SKUs\n    unit: month\n    aggregation: sum\n\
  \    dimensions:\n      - term\n      - scope\nprinciples:\n  - name: Visibility\n    description: Use Azure Cost Management + Billing, FOCUS-aligned cost exports to ADLS Gen2, and Azure\n      Workbooks / Power BI for near-real-time spend visibility down to resource and tag.\n  - name: Allocation\n    description: Apply tags, management groups, subscriptions, and resource groups to attribute spend\n      to teams, products, and environments; configure tag inheritance and tag policy.\n  - name: Optimization\n    description: Use Azure Advisor recommendations; right-size VMs; adopt Reservations and Azure Savings\n      Plan for stable workloads; use Spot instances for fault-tolerant compute; enable autoscale; clean\n      up unattached disks and idle resources.\n  - name: Accountability\n    description: Set Cost Management budgets with alerts; assign subscription / resource-group owners;\n      run monthly FinOps reviews; chargeback / showback via FOCUS exports.\nmaintainers:\n  - FN:\
  \ Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure/refs/heads/main/finops/azure-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/
- https://learn.microsoft.com/en-us/azure/cost-management-billing/
- https://learn.microsoft.com/en-us/azure/cost-management-billing/dataset-schema/cost-usage-details-focus
specification: FinOps Framework
tags:
- Cloud Computing
- Infrastructure
- Platform as a Service
- FinOps
- FOCUS
---
