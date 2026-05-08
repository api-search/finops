---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: keyvault.json
  format: json
  label: Azure Key Vault API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/keyvault/resource-manager/Microsoft.KeyVault/stable/2023-02-01/keyvault.json
- filename: keyvault.json
  format: json
  label: Azure Key Vault Data Plane API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/keyvault/data-plane/Microsoft.KeyVault/stable/7.4/keyvault.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Azure Key Vault API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Key Vault
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Key Vault
  PublisherName: Azure Key Vault
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Key Vault
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Microsoft Azure Key Vault Finops
provider_name: Azure Key Vault
provider_slug: microsoft-azure-key-vault
publisher_name: Azure Key Vault
service_category: API
slug: microsoft-azure-key-vault-finops
source_filename: microsoft-azure-key-vault-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Key Vault\nproviderId: microsoft-azure-key-vault\npublisherName: Azure Key Vault\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Certificates\n  - Cloud Security\n  - Cryptography\n  - Key Management\n  - Secrets Management\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Key Vault API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Key Vault\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Key Vault\n  PublisherName: Azure Key Vault\n  InvoiceIssuerName: Azure Key Vault\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Key Vault API\n    baseURL: https://management.azure.com\n    tags:\n      - Certificates\n      - Keys\n      - Secrets\n      - Vaults\n    serviceName: Azure Key Vault API\n    serviceCategory: API\n  - name: Azure Key Vault Data Plane API\n    baseURL: https://{vault-name}.vault.azure.net\n    tags:\n      - Certificate Operations\n      - Cryptographic Operations\n      - Key Operations\n      - Secret Operations\n    serviceName: Azure Key Vault Data Plane API\n    serviceCategory: API\n  - name: Azure Key Vault Keys API\n    baseURL: https://{vault-name}.vault.azure.net\n    tags:\n      - Cryptographic\
  \ Operations\n      - Encryption\n      - HSM\n      - Keys\n      - Signing\n    serviceName: Azure Key Vault Keys API\n    serviceCategory: API\n  - name: Azure Key Vault Secrets API\n    baseURL: https://{vault-name}.vault.azure.net\n    tags:\n      - Connection Strings\n      - Passwords\n      - Secrets\n      - Secure Storage\n    serviceName: Azure Key Vault Secrets API\n    serviceCategory: API\n  - name: Azure Key Vault Certificates API\n    baseURL: https://{vault-name}.vault.azure.net\n    tags:\n      - Certificate Authorities\n      - Certificate Management\n      - Certificates\n      - SSL\n      - TLS\n    serviceName: Azure Key Vault Certificates API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-key-vault/refs/heads/main/finops/microsoft-azure-key-vault-finops.yml
sources: []
specification: FinOps Framework
tags:
- Certificates
- Cloud Security
- Cryptography
- Key Management
- Secrets Management
- Security
- FinOps
- Cost Management
- FOCUS
---
