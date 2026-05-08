---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual / Multi-year ELA
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Enterprise Subscription
description: FOCUS-aligned FinOps profile for Hyperscience. Hyperscience is enterprise- only with custom annual contracts; cost surfaces are (a) the Hypercell platform license, (b) optional industry-specific modules (Freight Pay, GenAI, SNAP), and (c) for on-premises deployments, the customer's own infrastructure spend.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Hyperscience
  PricingUnit: contract-year
  ProviderName: Hyperscience
  PublisherName: Hyperscience
  ServiceCategory: AI / IDP
  ServiceName: Hyperscience Hypercell
layout: finops
meters:
- aggregation: sum
  description: Annual Hypercell platform license.
  dimensions:
  - account
  name: hypercell_license
  unit: contract-year
- aggregation: sum
  description: Per-module add-on (Freight Pay, GenAI, SNAP).
  dimensions:
  - account
  - module
  name: module_addon
  unit: contract-year
- aggregation: sum
  description: Documents processed against contract throughput envelope.
  dimensions:
  - tenant
  - flow
  name: documents_processed
  unit: document
- aggregation: sum
  description: Pages processed (informational).
  dimensions:
  - tenant
  - flow
  name: pages_processed
  unit: page
- aggregation: sum
  description: Customer cloud / hardware spend for on-prem Hypercell deployments (cloud-billed).
  dimensions:
  - cloud_account
  - region
  name: on_prem_infra
  unit: vm-hour
name: Hyperscience Finops
provider_name: Hyperscience
provider_slug: hyperscience
publisher_name: Hyperscience
service_category: Enterprise IDP
slug: hyperscience-finops
source_filename: hyperscience-finops.yml
source_heading: FinOps Profile
source_url: https://www.hyperscience.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Hyperscience\nproviderId: hyperscience\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Document AI\n- IDP\n- Enterprise\n- Automation\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Hyperscience. Hyperscience is enterprise-\n  only with custom annual contracts; cost surfaces are (a) the Hypercell\n  platform license, (b) optional industry-specific modules (Freight Pay,\n  GenAI, SNAP), and (c) for on-premises deployments, the customer's own\n  infrastructure spend.\nnotes: >-\n  No public unit pricing. FedRAMP High authorisation makes Hyperscience an\n  unusually common pick for U.S. federal agencies; multi-year ELAs are\n  typical. Cost allocation by document type / business unit is best done at\n  the Flow / queue level inside Hypercell.\nsources:\n- https://www.hyperscience.ai/\n- https://www.hyperscience.ai/security/\n\
  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Hyperscience\nserviceCategory: Enterprise IDP\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual / Multi-year ELA\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Hyperscience Hypercell\n  ServiceCategory: AI / IDP\n  ProviderName: Hyperscience\n  PublisherName: Hyperscience\n  InvoiceIssuerName: Hyperscience\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: contract-year\nmeters:\n- name: hypercell_license\n  description: Annual Hypercell platform license.\n  unit: contract-year\n  aggregation: sum\n  dimensions:\n  - account\n- name: module_addon\n  description: Per-module add-on (Freight Pay,\
  \ GenAI, SNAP).\n  unit: contract-year\n  aggregation: sum\n  dimensions:\n  - account\n  - module\n- name: documents_processed\n  description: Documents processed against contract throughput envelope.\n  unit: document\n  aggregation: sum\n  dimensions:\n  - tenant\n  - flow\n- name: pages_processed\n  description: Pages processed (informational).\n  unit: page\n  aggregation: sum\n  dimensions:\n  - tenant\n  - flow\n- name: on_prem_infra\n  description: Customer cloud / hardware spend for on-prem Hypercell deployments (cloud-billed).\n  unit: vm-hour\n  aggregation: sum\n  dimensions:\n  - cloud_account\n  - region\nprinciples:\n- name: Visibility\n  description: Use Hypercell admin telemetry per Flow; reconcile with annual invoice.\n- name: Allocation\n  description: One Flow per business unit / document type; map to FOCUS ResourceTag.\n- name: Optimization\n  description: Tune extraction thresholds to reduce review touches; consolidate Flows; renegotiate at renewal based on actual\
  \ volume.\n- name: Accountability\n  description: Assign Flow owners; review monthly throughput against contract envelope.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hyperscience/refs/heads/main/finops/hyperscience-finops.yml
sources:
- https://www.hyperscience.ai/
- https://www.hyperscience.ai/security/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Document AI
- IDP
- Enterprise
- Automation
- FinOps
- Cost Management
- FOCUS
---
