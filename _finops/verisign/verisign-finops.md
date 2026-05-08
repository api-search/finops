---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Verisign: registry operator with contractual / per-domain wholesale pricing rather than a public API consumption model. There is no public usage/billing API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: VeriSign, Inc.
  ProviderName: Verisign
  PublisherName: VeriSign, Inc.
  ServiceCategory: Internet Infrastructure
  ServiceName: Verisign Registry Services
layout: finops
meters:
- aggregation: sum
  description: Wholesale per-domain-year line under the registry agreement; not an API consumption meter.
  name: domain_registration
  unit: domain-year
name: Verisign Finops
provider_name: VeriSign
provider_slug: verisign
publisher_name: VeriSign, Inc.
service_category: Internet Infrastructure
slug: verisign-finops
source_filename: verisign-finops.yml
source_heading: FinOps Profile
source_url: https://www.verisign.com/en_US/domain-names/online/index.xhtml
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: VeriSign\nproviderId: verisign\npublisherName: VeriSign, Inc.\nserviceCategory: Internet Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - DNS\n  - Domain Registry\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Verisign: registry operator with contractual / per-domain\n  wholesale pricing rather than a public API consumption model. There is no public usage/billing API.'\nsources:\n  - https://www.verisign.com/en_US/domain-names/online/index.xhtml\nnotes: Verisign's billing surface is registrar-contract pricing per registered domain, not API consumption.\n  Stub retained for catalog completeness;\
  \ reconciliation deferred pending registrar-portal discovery.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Verisign Registry Services\n  ServiceCategory: Internet Infrastructure\n  ProviderName: Verisign\n  PublisherName: VeriSign, Inc.\n  InvoiceIssuerName: VeriSign, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: domain_registration\n    description: Wholesale per-domain-year line under the registry agreement; not an API consumption\n      meter.\n    unit: domain-year\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into registered domains is exposed to accredited registrars via EPP / RDAP\n      and registrar portal reporting; end customers see invoice-level data only.\n  - name: Allocation\n    description: Allocation is per registered domain to the registrant of record via the accredited registrar.\n  - name: Optimization\n\
  \    description: Optimization is portfolio-management (consolidation, renewal cadence, premium-name strategy)\n      rather than rate-card optimization; wholesale rates are contractual.\n  - name: Accountability\n    description: Accountability sits with the registrar of record for each domain, with end-of-portfolio\n      ownership at the registrant.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/verisign/refs/heads/main/finops/verisign-finops.yml
sources:
- https://www.verisign.com/en_US/domain-names/online/index.xhtml
specification: FinOps Framework
tags:
- DNS
- Domain Registry
- FinOps
- FOCUS
---
