---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage (overage)
description: FOCUS-aligned FinOps profile for DocRaptor. Billing is a flat monthly tier fee with included documents and a tier-specific per-document overage rate ($0.025–$0.12/doc). Test documents are free and unlimited (watermarked). Annual billing options exist on Bronze and higher.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: DocRaptor
  PricingUnit: document
  ProviderName: DocRaptor
  PublisherName: DocRaptor
  ServiceCategory: Document Generation
  ServiceName: DocRaptor
layout: finops
meters:
- aggregation: sum
  description: Flat monthly DocRaptor plan fee.
  dimensions:
  - account
  - tier
  name: plan_subscription
  unit: month
- aggregation: sum
  description: Production documents generated against the included monthly bundle.
  dimensions:
  - account
  - format
  name: documents_generated
  unit: document
- aggregation: sum
  description: Documents above the included bundle billed at tier overage rate.
  dimensions:
  - account
  name: document_overage
  unit: document
- aggregation: sum
  description: Test (watermarked) documents (informational; not billed).
  dimensions:
  - account
  name: test_documents
  unit: document
name: Docraptor Finops
provider_name: DocRaptor
provider_slug: docraptor
publisher_name: DocRaptor
service_category: Document Generation
slug: docraptor-finops
source_filename: docraptor-finops.yml
source_heading: FinOps Profile
source_url: https://docraptor.com/plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: DocRaptor\nproviderId: docraptor\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Document Generation\n- PDF\n- HTML\n- Excel\n- API\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for DocRaptor. Billing is a flat monthly tier\n  fee with included documents and a tier-specific per-document overage rate\n  ($0.025–$0.12/doc). Test documents are free and unlimited (watermarked).\n  Annual billing options exist on Bronze and higher.\nnotes: >-\n  Optimisation is mostly about right-sizing the monthly tier — effective\n  per-document rate decreases sharply as you climb tiers (Basic ~$0.12/doc,\n  Gold ~$0.025/doc).\nsources:\n- https://docraptor.com/plans\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: DocRaptor\nserviceCategory: Document Generation\nbillingModel:\n  pricingCategory: Subscription + Usage (overage)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: DocRaptor\n  ServiceCategory: Document Generation\n  ProviderName: DocRaptor\n  PublisherName: DocRaptor\n  InvoiceIssuerName: DocRaptor\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: document\nmeters:\n- name: plan_subscription\n  description: Flat monthly DocRaptor plan fee.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - tier\n- name: documents_generated\n  description: Production documents generated against the included monthly bundle.\n  unit: document\n  aggregation: sum\n  dimensions:\n  - account\n  - format\n- name: document_overage\n  description: Documents\
  \ above the included bundle billed at tier overage rate.\n  unit: document\n  aggregation: sum\n  dimensions:\n  - account\n- name: test_documents\n  description: Test (watermarked) documents (informational; not billed).\n  unit: document\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use DocRaptor account dashboard usage page; reconcile against monthly invoice.\n- name: Allocation\n  description: One API key per app/team; map to FOCUS ResourceTag downstream.\n- name: Optimization\n  description: Step up tier when overage is sustained; cache rendered PDFs server-side; use async to amortise concurrency.\n- name: Accountability\n  description: Assign API-key owners; alert on monthly burn-down toward bundle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/docraptor/refs/heads/main/finops/docraptor-finops.yml
sources:
- https://docraptor.com/plans
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Document Generation
- PDF
- HTML
- Excel
- API
- FinOps
- Cost Management
- FOCUS
---
