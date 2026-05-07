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
  - Adjustment
  pricingCategory: Enterprise Contract
description: 'FOCUS-aligned FinOps for Nike: no public API SaaS exists. Partner program operates under enterprise contract terms negotiated per partner.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: NIKE, Inc.
  PricingCategory: Contract
  ProviderName: Nike
  PublisherName: NIKE, Inc.
  ServiceCategory: Retail
  ServiceName: Nike Partner API
  ServiceSubcategory: Product Data
layout: finops
meters:
- aggregation: sum
  description: Nike partner program contractual obligations.
  dimensions:
  - partner
  - region
  name: partner_contract
  unit: contract-month
name: Nike Finops
provider_name: nike
provider_slug: nike
publisher_name: NIKE, Inc.
service_category: Retail + E-Commerce
slug: nike-finops
source_filename: nike-finops.yml
source_heading: FinOps Profile
source_url: https://developer.nike.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Nike\nproviderId: nike\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Retail\n  - E-Commerce\nnotes: Nike does not sell APIs as a public product; FinOps shape captured here documents the partner\n  program billing pattern only. Reconcile if Nike publishes a developer commercial program.\ndescription: 'FOCUS-aligned FinOps for Nike: no public API SaaS exists. Partner program operates under\n  enterprise contract terms negotiated per partner.'\nsources:\n  - https://developer.nike.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: NIKE, Inc.\nserviceCategory: Retail + E-Commerce\nbillingModel:\n  pricingCategory: Enterprise\
  \ Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Nike Partner API\n  ServiceCategory: Retail\n  ServiceSubcategory: Product Data\n  ProviderName: Nike\n  PublisherName: NIKE, Inc.\n  InvoiceIssuerName: NIKE, Inc.\n  BillingCurrency: USD\n  PricingCategory: Contract\nmeters:\n  - name: partner_contract\n    description: Nike partner program contractual obligations.\n    unit: contract-month\n    aggregation: sum\n    dimensions:\n      - partner\n      - region\nprinciples:\n  - name: Visibility\n    description: Partner-side; Nike does not expose self-service usage telemetry to third-party FinOps\n      tooling.\n  - name: Allocation\n    description: Each Nike partner manages internal cost attribution for any data-feed integrations.\n  - name: Optimization\n    description: Optimize partner integration scope to the minimum data required; avoid over-fetching\n      on inventory feeds.\n\
  \  - name: Accountability\n    description: Partner contract owner inside the consumer organization owns the contractual SLA and\n      any usage commitments.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nike/refs/heads/main/finops/nike-finops.yml
sources:
- https://developer.nike.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Retail
- E-Commerce
---
