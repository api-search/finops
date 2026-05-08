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
description: FinOps view of Anyscale spend. Anyscale meters compute by instance-hour per node type (CPU and NVIDIA T4 / L4 / A10G / A100 / H100 / H200). Hosted customers are invoiced directly by Anyscale; BYOC customers are charged the underlying cloud spend by AWS / GCP plus an Anyscale platform fee per instance-hour, often via a cloud marketplace.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Anyscale
  PricingCategory: Usage-Based
  ProviderName: Anyscale
  PublisherName: Anyscale
  ServiceCategory: AI and Machine Learning
  ServiceName: Anyscale Platform
layout: finops
meters:
- aggregation: sum
  description: CPU-only node hours billed per instance-hour ($0.0135/hr hosted).
  dimensions:
  - organization
  - cluster
  - workload_type
  name: cpu_instance_hours
  unit: hours
- aggregation: sum
  description: NVIDIA T4 GPU instance hours ($0.5682/hr hosted).
  dimensions:
  - organization
  - cluster
  name: gpu_instance_hours_t4
  unit: hours
- aggregation: sum
  description: NVIDIA L4 GPU instance hours ($0.9542/hr hosted).
  dimensions:
  - organization
  - cluster
  name: gpu_instance_hours_l4
  unit: hours
- aggregation: sum
  description: NVIDIA A10G GPU instance hours ($1.3635/hr hosted).
  dimensions:
  - organization
  - cluster
  name: gpu_instance_hours_a10g
  unit: hours
- aggregation: sum
  description: NVIDIA A100 GPU instance hours ($4.9591/hr hosted).
  dimensions:
  - organization
  - cluster
  name: gpu_instance_hours_a100
  unit: hours
- aggregation: sum
  description: NVIDIA H100 GPU instance hours ($9.2880/hr hosted).
  dimensions:
  - organization
  - cluster
  name: gpu_instance_hours_h100
  unit: hours
- aggregation: sum
  description: NVIDIA H200 GPU instance hours ($10.6812/hr hosted).
  dimensions:
  - organization
  - cluster
  name: gpu_instance_hours_h200
  unit: hours
- aggregation: sum
  description: BYOC platform-fee instance-hours invoiced via marketplace (rate contract-dependent).
  dimensions:
  - organization
  - cluster
  name: byoc_platform_hours
  unit: hours
name: Anyscale Finops
provider_name: Anyscale
provider_slug: anyscale
publisher_name: Anyscale
service_category: AI and Machine Learning
slug: anyscale-finops
source_filename: anyscale-finops.yml
source_heading: FinOps Profile
source_url: https://www.anyscale.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Anyscale\nproviderId: anyscale\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Distributed Computing\n- Ray\n- ML Platform\n- Inference\n- GPU\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FinOps view of Anyscale spend. Anyscale meters compute by instance-hour per\n  node type (CPU and NVIDIA T4 / L4 / A10G / A100 / H100 / H200). Hosted\n  customers are invoiced directly by Anyscale; BYOC customers are charged\n  the underlying cloud spend by AWS / GCP plus an Anyscale platform fee per\n  instance-hour, often via a cloud marketplace.\nnotes: >-\n  In BYOC mode the FOCUS dataset will combine an Anyscale ProviderName line\n  item with separate AWS / GCP ProviderName line items - reconcile both for\n  total cost-of-Ray.\nsources:\n- https://www.anyscale.com/pricing\n- https://docs.anyscale.com/\n- https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Anyscale\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Anyscale Platform\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Anyscale\n  PublisherName: Anyscale\n  InvoiceIssuerName: Anyscale\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory: Usage-Based\nmeters:\n- name: cpu_instance_hours\n  description: CPU-only node hours billed per instance-hour ($0.0135/hr hosted).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - organization\n  - cluster\n  - workload_type\n- name: gpu_instance_hours_t4\n  description: NVIDIA T4 GPU instance hours\
  \ ($0.5682/hr hosted).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - organization\n  - cluster\n- name: gpu_instance_hours_l4\n  description: NVIDIA L4 GPU instance hours ($0.9542/hr hosted).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - organization\n  - cluster\n- name: gpu_instance_hours_a10g\n  description: NVIDIA A10G GPU instance hours ($1.3635/hr hosted).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - organization\n  - cluster\n- name: gpu_instance_hours_a100\n  description: NVIDIA A100 GPU instance hours ($4.9591/hr hosted).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - organization\n  - cluster\n- name: gpu_instance_hours_h100\n  description: NVIDIA H100 GPU instance hours ($9.2880/hr hosted).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - organization\n  - cluster\n- name: gpu_instance_hours_h200\n  description: NVIDIA H200 GPU instance hours ($10.6812/hr hosted).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - organization\n\
  \  - cluster\n- name: byoc_platform_hours\n  description: BYOC platform-fee instance-hours invoiced via marketplace (rate contract-dependent).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - organization\n  - cluster\nprinciples:\n- name: Visibility\n  description: Pull Anyscale usage exports per cluster/project; in BYOC, also pull AWS/GCP cost exports tagged with cluster IDs.\n- name: Allocation\n  description: Tag clusters and services to projects/teams; map to internal cost centers.\n- name: Optimization\n  description: Right-size compute configs and autoscaler bounds; idle workspaces auto-suspend; use committed-spend discounts and BYOC GPU reservations.\n- name: Accountability\n  description: Assign owners per project; review monthly GPU-hour burn and idle utilization.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/anyscale/refs/heads/main/finops/anyscale-finops.yml
sources:
- https://www.anyscale.com/pricing
- https://docs.anyscale.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Distributed Computing
- Ray
- ML Platform
- Inference
- GPU
- FinOps
- Cost Management
- FOCUS
---
