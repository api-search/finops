---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hvault-system-backend-openapi.yml
  format: yaml
  label: Vault System Backend API
  slug: vault-system-backend-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hvault/refs/heads/main/openapi/hvault-system-backend-openapi.yml
- filename: hvault-secrets-engines-openapi.yml
  format: yaml
  label: Vault Secrets Engines API
  slug: vault-secrets-engines-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hvault/refs/heads/main/openapi/hvault-secrets-engines-openapi.yml
- filename: hvault-auth-methods-openapi.yml
  format: yaml
  label: Vault Auth Methods API
  slug: vault-auth-methods-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hvault/refs/heads/main/openapi/hvault-auth-methods-openapi.yml
- filename: hvault-identity-openapi.yml
  format: yaml
  label: Vault Identity API
  slug: vault-identity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hvault/refs/heads/main/openapi/hvault-identity-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (Enterprise) / Hourly (HCP)
  chargeCategories:
  - Purchase
  - Usage
  - Credit
  - Tax
  - Adjustment
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for HashiCorp Vault: open-source self-managed (no vendor cost), Enterprise self-managed (annual contract priced by client count), HCP Vault Dedicated (cluster-hour), and HCP Vault Secrets (per-secret-per-month). IBM acquired HashiCorp in 2025 - billing for HCP flows through the IBM HashiCorp Cloud Platform.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: IBM HashiCorp Cloud Platform
  ProviderName: HashiCorp
  PublisherName: HashiCorp, Inc.
  ServiceCategory: Security & Identity
  ServiceName: HashiCorp Vault
layout: finops
meters:
- aggregation: max
  description: Distinct clients (services or humans) authenticating against Vault Enterprise; the primary pricing dimension for self-managed Enterprise contracts.
  dimensions:
  - cluster
  - namespace
  name: enterprise_clients
  unit: client
- aggregation: sum
  description: Cluster-hours for HCP Vault Dedicated, billed by cluster size and tier (Development, Standard, Plus).
  dimensions:
  - cluster_size
  - tier
  - cloud
  - region
  name: hcp_cluster_hours
  unit: cluster-hour
- aggregation: max
  description: Active secrets stored in HCP Vault Secrets, billed per-secret-per-month.
  dimensions:
  - project
  - app
  name: hcp_secrets
  unit: secret-month
- aggregation: sum
  description: Native syncs from HCP Vault Secrets to integration targets (AWS, Azure, GCP, Vercel, GitHub Actions).
  dimensions:
  - target
  - project
  name: hcp_secrets_syncs
  unit: sync
- aggregation: sum
  description: Internal Vault API request volume, useful for capacity planning even when not directly billed.
  dimensions:
  - mount
  - namespace
  - path
  name: api_requests
  unit: request
name: Hvault Finops
provider_name: HashiCorp Vault
provider_slug: hvault
publisher_name: HashiCorp, Inc. (an IBM company)
service_category: Security & Identity
slug: hvault-finops
source_filename: hvault-finops.yml
source_heading: FinOps Profile
source_url: https://www.hashicorp.com/products/vault
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: HashiCorp Vault\nproviderId: hvault\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Secrets Management\n  - Security\ndescription: 'FOCUS-aligned FinOps for HashiCorp Vault: open-source self-managed (no vendor cost),\n  Enterprise self-managed (annual contract priced by client count), HCP Vault Dedicated (cluster-hour),\n  and HCP Vault Secrets (per-secret-per-month). IBM acquired HashiCorp in 2025 - billing for HCP\n  flows through the IBM HashiCorp Cloud Platform.'\nnotes: HCP Vault Dedicated cluster-hour rates and HCP Vault Secrets per-secret rates are not published\n  on the public pricing page; sign-in to the HashiCorp Cloud Platform console is required to view.\nsources:\n  - https://www.hashicorp.com/products/vault\n  - https://www.hashicorp.com/en/pricing?tab=vault\n  - https://developer.hashicorp.com/hcp/docs/vault\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: HashiCorp, Inc. (an IBM company)\nserviceCategory: Security & Identity\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Annual (Enterprise) / Hourly (HCP)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Credit\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: HashiCorp Vault\n  ServiceCategory: Security & Identity\n  ProviderName: HashiCorp\n  PublisherName: HashiCorp, Inc.\n  InvoiceIssuerName: IBM HashiCorp Cloud Platform\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: enterprise_clients\n    description: Distinct clients (services or humans) authenticating against Vault Enterprise; the\n      primary pricing dimension for self-managed Enterprise contracts.\n\
  \    unit: client\n    aggregation: max\n    dimensions:\n      - cluster\n      - namespace\n  - name: hcp_cluster_hours\n    description: Cluster-hours for HCP Vault Dedicated, billed by cluster size and tier (Development,\n      Standard, Plus).\n    unit: cluster-hour\n    aggregation: sum\n    dimensions:\n      - cluster_size\n      - tier\n      - cloud\n      - region\n  - name: hcp_secrets\n    description: Active secrets stored in HCP Vault Secrets, billed per-secret-per-month.\n    unit: secret-month\n    aggregation: max\n    dimensions:\n      - project\n      - app\n  - name: hcp_secrets_syncs\n    description: Native syncs from HCP Vault Secrets to integration targets (AWS, Azure, GCP, Vercel,\n      GitHub Actions).\n    unit: sync\n    aggregation: sum\n    dimensions:\n      - target\n      - project\n  - name: api_requests\n    description: Internal Vault API request volume, useful for capacity planning even when not directly\n      billed.\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - mount\n      - namespace\n      - path\nprinciples:\n  - name: Visibility\n    description: Use the HashiCorp Cloud Platform billing dashboard for HCP usage. For self-managed\n      Enterprise, monitor Vault telemetry (vault.core.handle_login_request, vault.core.handle_request,\n      vault.expire.num_leases) via Prometheus or Datadog; correlate against the contracted client\n      count.\n  - name: Allocation\n    description: Use Vault Enterprise namespaces to allocate cost to business units. Tag HCP Vault\n      Dedicated clusters and HCP Vault Secrets projects with team/product metadata for chargeback.\n  - name: Optimization\n    description: Right-size HCP Vault Dedicated clusters (Development vs Standard vs Plus); consolidate\n      low-traffic workloads onto shared self-managed clusters; use lease quotas to prevent runaway\n      lease growth that drives oversized clusters; consider HCP Vault Secrets free tier (25 secrets)\n      for small applications.\n\
  \  - name: Accountability\n    description: For Enterprise, monitor active client count against the contractual ceiling and\n      forecast renewal sizing. For HCP, set spending alerts in the HashiCorp Cloud Platform console.\n      The $500 IBM HashiCorp Cloud Platform credit can offset initial proof-of-value cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hvault/refs/heads/main/finops/hvault-finops.yml
sources:
- https://www.hashicorp.com/products/vault
- https://www.hashicorp.com/en/pricing?tab=vault
- https://developer.hashicorp.com/hcp/docs/vault
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Secrets Management
- Security
---
