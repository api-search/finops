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
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Azure Key Vault: per-10,000-operation pricing on the Standard tier and per-active-HSM-key plus per-operation pricing on the Premium tier; Managed HSM bills per pool-hour plus per-operation.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Security
  ServiceName: Azure Key Vault
layout: finops
meters:
- aggregation: sum
  dimensions:
  - vault
  - region
  name: secret_operations
  unit: operation
- aggregation: sum
  dimensions:
  - vault
  - region
  name: software_key_operations
  unit: operation
- aggregation: sum
  dimensions:
  - vault
  - region
  - key_type
  name: hsm_key_operations
  unit: operation
- aggregation: max
  dimensions:
  - vault
  - key_type
  name: hsm_active_keys
  unit: key-month
- aggregation: sum
  dimensions:
  - vault
  name: certificate_renewals
  unit: certificate
- aggregation: sum
  dimensions:
  - region
  - pool
  name: managed_hsm_pool_hours
  unit: instance-hour
name: Microsoft Azure Key Vault Finops
provider_name: Azure Key Vault
provider_slug: microsoft-azure-key-vault
publisher_name: Microsoft Corporation
service_category: Security / Key Management
slug: microsoft-azure-key-vault-finops
source_filename: microsoft-azure-key-vault-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/key-vault/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Key Vault\nproviderId: microsoft-azure-key-vault\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Security\n  - Microsoft Azure\ndescription: 'FOCUS-aligned FinOps for Azure Key Vault: per-10,000-operation pricing on the Standard\n  tier and per-active-HSM-key plus per-operation pricing on the Premium tier; Managed HSM bills per\n  pool-hour plus per-operation.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/key-vault/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Security / Key Management\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Azure Key Vault\n  ServiceCategory: Security\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: secret_operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - vault\n      - region\n  - name: software_key_operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - vault\n      - region\n  - name: hsm_key_operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - vault\n      - region\n      - key_type\n  - name: hsm_active_keys\n    unit: key-month\n    aggregation: max\n    dimensions:\n      - vault\n      - key_type\n  - name: certificate_renewals\n    unit: certificate\n    aggregation: sum\n    dimensions:\n      - vault\n  - name: managed_hsm_pool_hours\n\
  \    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - pool\nprinciples:\n  - name: Visibility\n    description: Use Azure Monitor metrics (TotalServiceApiHits, ServiceApiResultStatus) and Cost\n      Management filtered to Microsoft.KeyVault to break down per-vault and per-operation cost.\n  - name: Allocation\n    description: Use one Key Vault per environment/team/application and tag with cost-center; per-vault\n      cost rolls up cleanly to that owner.\n  - name: Optimization\n    description: Avoid per-operation calls in hot paths via DEK caching with envelope encryption;\n      consolidate low-volume vaults; choose Standard over Premium when HSM is not required; use Managed\n      HSM only when FIPS 140-2 L3 is needed.\n  - name: Accountability\n    description: Assign vault owners as cost owners; alert on operation-rate spikes and certificate-renewal\n      cost; review HSM key inventory quarterly to remove inactive keys (only active keys are billed).\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-key-vault/refs/heads/main/finops/microsoft-azure-key-vault-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/key-vault/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Security
- Microsoft Azure
---
