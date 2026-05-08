---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aqua-security-api.yaml
  format: yaml
  label: Aqua Security
  slug: aqua-security
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aqua-security/refs/heads/main/openapi/aqua-security-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom / Contract
description: FOCUS-aligned FinOps placeholder for Aqua Security. No public billing-model details, meters, or invoice schema are published; this artifact records the absence so consumers know to source commercial terms from the provider directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Aqua Security Software Ltd.
  ProviderName: Aqua Security
  PublisherName: Aqua Security Software Ltd.
  ServiceCategory: Cloud Native Security
  ServiceName: Aqua Security
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line items once an invoice or usage schema is available.
  dimensions:
  - contract
  - consumer
  name: contract_usage
  unit: varies
name: Aqua Security Finops
provider_name: Aqua Security
provider_slug: aqua-security
publisher_name: Aqua Security Software Ltd.
service_category: Security
slug: aqua-security-finops
source_filename: aqua-security-finops.yml
source_heading: FinOps Profile
source_url: https://www.aquasec.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Aqua Security\nproviderId: aqua-security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Cloud Native\n- Containers\n- Kubernetes\n- Runtime Protection\n- Security\n- Vulnerability Scanning\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Aqua Security. No public billing-model details, meters,\n  or invoice schema are published; this artifact records the absence so consumers know to source commercial\n  terms from the provider directly.\nnotes: Aqua Security uses consumption-based enterprise pricing — Dev Security is priced per code repository\n  and Cloud Security per workload (EC2 instance, Fargate container, Lambda function, etc.). No public\n  per-tier prices, free tier, or quotas are published; the pricing page directs prospects to Request a\n  Trial / Get a Demo.\nsources:\n- https://www.aquasec.com\n\
  - https://focus.finops.org/focus-specification/v1-3/\n- https://www.aquasec.com/pricing/\n- https://docs.aquasec.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Aqua Security Software Ltd.\nserviceCategory: Security\nbillingModel:\n  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Aqua Security\n  ServiceCategory: Cloud Native Security\n  ProviderName: Aqua Security\n  PublisherName: Aqua Security Software Ltd.\n  InvoiceIssuerName: Aqua Security Software Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: contract_usage\n  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line\n    items once an invoice\
  \ or usage schema is available.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - contract\n  - consumer\nprinciples:\n- name: Visibility\n  description: Because the provider does not publish a usage API or self-serve billing dashboard, request\n    invoice copies and contract usage exports directly from the account team and load them into your own\n    FinOps tooling.\n- name: Allocation\n  description: Allocate spend by tagging invoice line items to consuming business units in your ERP /\n    FinOps store; no provider-side tagging surface is available.\n- name: Optimization\n  description: Optimization levers are commercial — renegotiate volume commitments, consolidate accounts,\n    or align contract scope with actual usage at renewal.\n- name: Accountability\n  description: Assign a contract owner who reviews invoices against the negotiated agreement, since usage\n    drift cannot be detected from a published meter feed.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aqua-security/refs/heads/main/finops/aqua-security-finops.yml
sources:
- https://www.aquasec.com
- https://focus.finops.org/focus-specification/v1-3/
- https://www.aquasec.com/pricing/
- https://docs.aquasec.com
specification: FinOps Framework
tags:
- Cloud Native
- Containers
- Kubernetes
- Runtime Protection
- Security
- Vulnerability Scanning
- FinOps
- Cost Management
- FOCUS
---
