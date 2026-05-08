---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based
description: FinOps view of Modal spend. Modal bills usage-based per-second meters for CPU core-seconds, memory GiB-seconds, GPU-seconds (per GPU class), and storage GiB-months on top of a tiered subscription (Starter / Team / Enterprise). Free monthly credits offset compute up to a tier-specific amount.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Modal
  PricingCategory: Usage-Based
  ProviderName: Modal
  PublisherName: Modal
  ServiceCategory: AI and Machine Learning
  ServiceName: Modal
layout: finops
meters:
- aggregation: sum
  description: Physical CPU core-seconds consumed per container, billed at $0.0000131/core-sec.
  dimensions:
  - workspace
  - app
  - function
  name: cpu_core_seconds
  unit: core_seconds
- aggregation: sum
  description: Memory GiB-seconds consumed per container, billed at $0.00000222/GiB-sec.
  dimensions:
  - workspace
  - app
  - function
  name: memory_gib_seconds
  unit: gib_seconds
- aggregation: sum
  description: GPU-seconds consumed by class (T4 / L4 / A10 / A100-40 / A100-80 / H100 / H200 / B200) at the per-class rate.
  dimensions:
  - workspace
  - app
  - function
  - gpu_class
  name: gpu_seconds
  unit: gpu_seconds
- aggregation: sum
  description: Persistent Volume / NFS storage GiB-months above the 1 TiB/month free allotment, billed at $0.09/GiB-mo.
  dimensions:
  - workspace
  - volume
  name: storage_gib_months
  unit: gib_months
- aggregation: sum
  description: Workspace tier monthly subscription ($0 Starter / $250 Team / Enterprise contract).
  dimensions:
  - workspace
  - tier
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Tier-bundled monthly credits ($30 Starter / $100 Team) applied first against compute meters.
  dimensions:
  - workspace
  - tier
  name: included_credits
  unit: usd
name: Modal Finops
provider_name: Modal
provider_slug: modal
publisher_name: Modal
service_category: AI and Machine Learning
slug: modal-finops
source_filename: modal-finops.yml
source_heading: FinOps Profile
source_url: https://modal.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Modal\nproviderId: modal\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Serverless\n- Compute\n- Python\n- Inference\n- GPU\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FinOps view of Modal spend. Modal bills usage-based per-second meters for\n  CPU core-seconds, memory GiB-seconds, GPU-seconds (per GPU class), and\n  storage GiB-months on top of a tiered subscription (Starter / Team /\n  Enterprise). Free monthly credits offset compute up to a tier-specific\n  amount.\nnotes: >-\n  Storage includes 1 TiB/month free; CPU minimum is 0.125 cores per\n  container. Modal does not charge for idle resources - meters tick only\n  while containers are running.\nsources:\n- https://modal.com/pricing\n- https://modal.com/docs\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Modal\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Modal\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Modal\n  PublisherName: Modal\n  InvoiceIssuerName: Modal\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory: Usage-Based\nmeters:\n- name: cpu_core_seconds\n  description: Physical CPU core-seconds consumed per container, billed at $0.0000131/core-sec.\n  unit: core_seconds\n  aggregation: sum\n  dimensions:\n  - workspace\n  - app\n  - function\n- name: memory_gib_seconds\n  description: Memory GiB-seconds consumed per container, billed at $0.00000222/GiB-sec.\n  unit: gib_seconds\n\
  \  aggregation: sum\n  dimensions:\n  - workspace\n  - app\n  - function\n- name: gpu_seconds\n  description: GPU-seconds consumed by class (T4 / L4 / A10 / A100-40 / A100-80 / H100 / H200 / B200) at the per-class rate.\n  unit: gpu_seconds\n  aggregation: sum\n  dimensions:\n  - workspace\n  - app\n  - function\n  - gpu_class\n- name: storage_gib_months\n  description: Persistent Volume / NFS storage GiB-months above the 1 TiB/month free allotment, billed at $0.09/GiB-mo.\n  unit: gib_months\n  aggregation: sum\n  dimensions:\n  - workspace\n  - volume\n- name: subscription_fee\n  description: Workspace tier monthly subscription ($0 Starter / $250 Team / Enterprise contract).\n  unit: month\n  aggregation: sum\n  dimensions:\n  - workspace\n  - tier\n- name: included_credits\n  description: Tier-bundled monthly credits ($30 Starter / $100 Team) applied first against compute meters.\n  unit: usd\n  aggregation: sum\n  dimensions:\n  - workspace\n  - tier\nprinciples:\n- name: Visibility\n\
  \  description: Pull per-app usage from the Modal dashboard / Modal usage API; export monthly invoices.\n- name: Allocation\n  description: Tag apps and functions per team/workload via environments and labels; map to internal cost centers.\n- name: Optimization\n  description: Right-size CPU/memory and GPU class; use container_idle_timeout to release containers; pick smaller GPUs (T4/L4) when possible; aggregate workloads to amortize cold starts.\n- name: Accountability\n  description: Assign owners per app/environment; review monthly GPU-second burn vs. budget.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/modal/refs/heads/main/finops/modal-finops.yml
sources:
- https://modal.com/pricing
- https://modal.com/docs
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Serverless
- Compute
- Python
- Inference
- GPU
- FinOps
- Cost Management
- FOCUS
---
