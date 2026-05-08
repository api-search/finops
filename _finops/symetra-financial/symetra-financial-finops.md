---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Partner Integration
description: Symetra's APIs are partner-integration channels (HR platforms, brokers, advisors) without public usage-based pricing or a FOCUS-aligned cost export.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Symetra Life Insurance Company
  ProviderName: Symetra Financial
  PublisherName: Symetra Life Insurance Company
  ServiceCategory: Insurance / Financial Services
  ServiceName: Symetra Financial APIs
layout: finops
meters:
- aggregation: count
  description: Partner integration relationships - the unit of consumption for Symetra's APIs is the connectivity agreement, not per-call.
  name: partner_integration
  unit: varies
name: Symetra Financial Finops
provider_name: Symetra Financial
provider_slug: symetra-financial
publisher_name: Symetra Life Insurance Company
service_category: Insurance / Financial Services
slug: symetra-financial-finops
source_filename: symetra-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.symetra.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Symetra Financial\nproviderId: symetra-financial\npublisherName: Symetra Life Insurance Company\nserviceCategory: Insurance / Financial Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Annuities\n  - Employee Benefits\n  - FinOps\n  - FOCUS\ndescription: Symetra's APIs are partner-integration channels (HR platforms, brokers, advisors) without public usage-based pricing or a FOCUS-aligned cost export.\nsources:\n  - https://www.symetra.com\n  - https://www.symetra.com/learn/articles-for-employers/technology-solutions/\nnotes: No public usage telemetry or FOCUS-aligned export. Cost data must be reconciled\
  \ from partner connectivity contracts and any insurance product premium / commission flows associated with the integration.\nbillingModel:\n  pricingCategory: Partner Integration\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Symetra Financial APIs\n  ServiceCategory: Insurance / Financial Services\n  ProviderName: Symetra Financial\n  PublisherName: Symetra Life Insurance Company\n  InvoiceIssuerName: Symetra Life Insurance Company\n  BillingCurrency: USD\nmeters:\n  - name: partner_integration\n    description: Partner integration relationships - the unit of consumption for Symetra's APIs is the connectivity agreement, not per-call.\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Cost visibility flows through Symetra account management to the partner; there is no self-service usage console or FOCUS-aligned export.\n  - name: Allocation\n    description: Allocate\
  \ against the partner relationship (HR platform, broker, advisor) rather than per API call - that is the contractual unit Symetra prices on.\n  - name: Optimization\n    description: Optimization is contractual - reduce manual EOI / claims handoffs and rely on the API for straight-through processing to lower per-transaction operating cost on the partner side.\n  - name: Accountability\n    description: The partner's integration owner and the Symetra account team jointly own the relationship; commercial review happens at contract renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/symetra-financial/refs/heads/main/finops/symetra-financial-finops.yml
sources:
- https://www.symetra.com
- https://www.symetra.com/learn/articles-for-employers/technology-solutions/
specification: FinOps Framework
tags:
- Insurance
- Annuities
- Employee Benefits
- FinOps
- FOCUS
---
