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
  slug: azure-key-vault-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/keyvault/resource-manager/Microsoft.KeyVault/stable/2023-02-01/keyvault.json
- filename: keyvault.json
  format: json
  label: Azure Key Vault Data Plane API
  slug: azure-key-vault-data-plane-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/keyvault/data-plane/Microsoft.KeyVault/stable/7.4/keyvault.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Azure Key Vault: per-10K-transaction usage metering for secrets, software keys, HSM-protected keys, and certificates, plus partition-hour billing for Managed HSM. Charges flow into the standard Azure invoice.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Pay-As-You-Go
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Security
  ServiceName: Azure Key Vault
layout: finops
meters:
- aggregation: sum
  description: Get/set/list secret operations
  dimensions:
  - vault
  - region
  - operation_type
  name: secret_operations
  unit: operation
- aggregation: sum
  description: Software-protected key crypto operations
  dimensions:
  - vault
  - region
  - key_type
  - key_size
  name: software_key_operations
  unit: operation
- aggregation: sum
  description: HSM-protected key crypto operations (Premium / Managed HSM)
  dimensions:
  - vault
  - region
  - key_type
  - key_size
  name: hsm_key_operations
  unit: operation
- aggregation: avg
  description: HSM-protected keys stored in Premium vault per month
  dimensions:
  - vault
  - region
  name: hsm_key_storage
  unit: key-month
- aggregation: sum
  description: Certificate create / get / renew operations
  dimensions:
  - vault
  - region
  name: certificate_operations
  unit: operation
- aggregation: sum
  description: Auto-renew issuances; metered separately from create
  name: certificate_renewals
  unit: renewal
- aggregation: sum
  description: Single-tenant Managed HSM partition active hours
  dimensions:
  - hsm_pool
  - region
  name: managed_hsm_partition_hours
  unit: partition-hour
name: Azure Key Vault Finops
provider_name: Azure Key Vault
provider_slug: microsoft-azure-key-vault
publisher_name: Microsoft Corporation
service_category: Security
slug: azure-key-vault-finops
source_filename: azure-key-vault-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/key-vault/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Key Vault\nproviderId: azure-key-vault\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Security\n  - Secrets Management\n  - HSM\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Azure Key Vault: per-10K-transaction usage metering for secrets,\n  software keys, HSM-protected keys, and certificates, plus partition-hour billing for Managed HSM. Charges\n  flow into the standard Azure invoice.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/key-vault/\n  - https://learn.microsoft.com/en-us/azure/key-vault/general/service-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Security\n\
  billingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Azure Key Vault\n  ServiceCategory: Security\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Pay-As-You-Go\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: secret_operations\n    description: Get/set/list secret operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - vault\n      - region\n      - operation_type\n  - name: software_key_operations\n    description: Software-protected key crypto operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - vault\n      - region\n      - key_type\n      - key_size\n  - name: hsm_key_operations\n    description: HSM-protected key crypto operations (Premium / Managed HSM)\n    unit: operation\n    aggregation:\
  \ sum\n    dimensions:\n      - vault\n      - region\n      - key_type\n      - key_size\n  - name: hsm_key_storage\n    description: HSM-protected keys stored in Premium vault per month\n    unit: key-month\n    aggregation: avg\n    dimensions:\n      - vault\n      - region\n  - name: certificate_operations\n    description: Certificate create / get / renew operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - vault\n      - region\n  - name: certificate_renewals\n    description: Auto-renew issuances; metered separately from create\n    unit: renewal\n    aggregation: sum\n  - name: managed_hsm_partition_hours\n    description: Single-tenant Managed HSM partition active hours\n    unit: partition-hour\n    aggregation: sum\n    dimensions:\n      - hsm_pool\n      - region\nprinciples:\n  - name: Visibility\n    description: Use Azure Monitor diagnostic logs and Log Analytics to track per-vault transaction volume\n      by operation type; correlate with Cost\
  \ Management cost-per-operation roll-ups.\n  - name: Allocation\n    description: Tag vaults by application / team; use one vault per workload to keep cost attribution\n      clean and respect throttling boundaries.\n  - name: Optimization\n    description: Cache secrets at the application tier; consolidate low-volume vaults; use software-protected\n      keys instead of HSM where compliance allows; size Managed HSM partitions to actual demand to avoid\n      idle hours.\n  - name: Accountability\n    description: Assign vault owners through Azure RBAC; review high-transaction vaults monthly; alert\n      on unusual operation volume which may signal cost or security incidents.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-key-vault/refs/heads/main/finops/azure-key-vault-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/key-vault/
- https://learn.microsoft.com/en-us/azure/key-vault/general/service-limits
specification: FinOps Framework
tags:
- Security
- Secrets Management
- HSM
- FinOps
- FOCUS
---
