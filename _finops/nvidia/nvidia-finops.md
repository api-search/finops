---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (subscription) or Hourly (cloud)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription (Per-GPU) + Pay-As-You-Go (Cloud Marketplace) + Free Trial
description: 'FOCUS-aligned FinOps for NVIDIA: hybrid commercial model spanning per-GPU/year AI Enterprise subscriptions (sold direct or via channel), hourly cloud marketplace SKUs (AWS/Azure/GCP), DGX Cloud hosted GPU rentals, and free build.nvidia.com trial credits. Cost allocation is GPU-centric: licenses, cloud-instance hours, and inference token throughput.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: NVIDIA Corporation (or AWS/Azure/GCP for marketplace)
  PricingCategory: Subscription
  PricingUnit: gpu
  ProviderName: NVIDIA
  PublisherName: NVIDIA Corporation
  ServiceCategory: AI Infrastructure
  ServiceName: NVIDIA AI / Developer Platform
layout: finops
meters:
- aggregation: sum
  description: Per-GPU per-year AI Enterprise software subscription
  dimensions:
  - gpu_model
  - cluster
  - region
  name: ai_enterprise_gpu_subscription
  unit: gpu-year
- aggregation: sum
  description: AI Enterprise hourly metered consumption on cloud marketplaces
  dimensions:
  - cloud
  - region
  - gpu_model
  name: ai_enterprise_marketplace_hours
  unit: gpu-hour
- aggregation: sum
  description: DGX Cloud / DGX Cloud Lepton hosted GPU instance hours
  dimensions:
  - cloud
  - region
  - instance_type
  name: dgx_cloud_instance_hours
  unit: instance-hour
- aggregation: sum
  description: build.nvidia.com NIM endpoint credit consumption
  dimensions:
  - model
  - api_key
  name: build_api_credits
  unit: credit
- aggregation: sum
  description: Inference tokens generated (input/output) on hosted or self-hosted NIM (operational telemetry)
  dimensions:
  - model
  - direction
  name: inference_tokens
  unit: token
name: Nvidia Finops
provider_name: Nvidia
provider_slug: nvidia
publisher_name: NVIDIA Corporation
service_category: AI Infrastructure
slug: nvidia-finops
source_filename: nvidia-finops.yml
source_heading: FinOps Profile
source_url: https://www.nvidia.com/en-us/data-center/products/ai-enterprise/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Nvidia\nproviderId: nvidia\npublisherName: NVIDIA Corporation\nserviceCategory: AI Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - GPU\n  - AI\n  - Machine Learning\n  - Computing\n  - Graphics\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for NVIDIA: hybrid commercial model spanning per-GPU/year AI Enterprise\n  subscriptions (sold direct or via channel), hourly cloud marketplace SKUs (AWS/Azure/GCP), DGX Cloud\n  hosted GPU rentals, and free build.nvidia.com trial credits. Cost allocation is GPU-centric: licenses,\n  cloud-instance hours, and inference token throughput.'\n\
  sources:\n  - https://www.nvidia.com/en-us/data-center/products/ai-enterprise/\n  - https://build.nvidia.com/\n  - https://catalog.ngc.nvidia.com/\nprinciples:\n  - name: Visibility\n    description: For AI Enterprise direct contracts, track per-GPU license entitlement vs. utilization.\n      For cloud marketplace consumption, pull FOCUS-aligned cost exports from AWS/Azure/GCP. For build.nvidia.com,\n      track per-API-key request and credit consumption via the NVIDIA developer dashboard.\n  - name: Allocation\n    description: Tag inference workloads (Kubernetes namespaces, model name, team) so per-GPU AI Enterprise\n      cost can be split across consuming products. For build.nvidia.com, allocate per-API-key.\n  - name: Optimization\n    description: Self-host NIM under AI Enterprise once steady-state inference exceeds the break-even\n      vs hosted endpoints. Right-size GPU type (L4/L40S/H100) per model size. Use TensorRT/Triton dynamic\n      batching to lift GPU utilization. For\
  \ training spikes, burst to DGX Cloud or cloud marketplace rather\n      than buying additional perpetual capacity.\n  - name: Accountability\n    description: Designate per-cluster GPU owners for utilization targets (>= 60% on production AI Enterprise\n      GPUs is a common SLO). Review monthly cloud-marketplace burn against forecast; flag idle GPU instances\n      within 24 hours.\nbillingModel:\n  pricingCategory: Subscription (Per-GPU) + Pay-As-You-Go (Cloud Marketplace) + Free Trial\n  billingFrequency: Annual (subscription) or Hourly (cloud)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: NVIDIA AI / Developer Platform\n  ServiceCategory: AI Infrastructure\n  ProviderName: NVIDIA\n  PublisherName: NVIDIA Corporation\n  InvoiceIssuerName: NVIDIA Corporation (or AWS/Azure/GCP for marketplace)\n  PricingCategory: Subscription\n  PricingUnit: gpu\n  BillingCurrency:\
  \ USD\n  ChargeCategory: Purchase\nmeters:\n  - name: ai_enterprise_gpu_subscription\n    description: Per-GPU per-year AI Enterprise software subscription\n    unit: gpu-year\n    aggregation: sum\n    dimensions:\n      - gpu_model\n      - cluster\n      - region\n  - name: ai_enterprise_marketplace_hours\n    description: AI Enterprise hourly metered consumption on cloud marketplaces\n    unit: gpu-hour\n    aggregation: sum\n    dimensions:\n      - cloud\n      - region\n      - gpu_model\n  - name: dgx_cloud_instance_hours\n    description: DGX Cloud / DGX Cloud Lepton hosted GPU instance hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud\n      - region\n      - instance_type\n  - name: build_api_credits\n    description: build.nvidia.com NIM endpoint credit consumption\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - model\n      - api_key\n  - name: inference_tokens\n    description: Inference tokens generated (input/output)\
  \ on hosted or self-hosted NIM (operational telemetry)\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - direction\napis:\n  - name: NVIDIA Developer API\n    baseURL: https://integrate.api.nvidia.com\n    tags:\n      - GPU\n      - AI\n      - Machine Learning\n      - Inference\n    serviceName: NVIDIA Developer API\n    serviceCategory: AI Infrastructure\nunitEconomics:\n  - name: Cost per inference token (hosted)\n    metric: build_credits_cost / inference_tokens\n    target: compare against self-hosted break-even\n  - name: GPU utilization\n    metric: gpu_busy_seconds / gpu_allocated_seconds\n    target: '>= 0.6 on production AI Enterprise clusters'\n  - name: Cost per million tokens (self-hosted)\n    metric: (ai_enterprise_subscription + power + amortized_hardware) / (inference_tokens / 1000000)\n    target: minimize via Triton dynamic batching\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nvidia/refs/heads/main/finops/nvidia-finops.yml
sources:
- https://www.nvidia.com/en-us/data-center/products/ai-enterprise/
- https://build.nvidia.com/
- https://catalog.ngc.nvidia.com/
specification: FinOps Framework
tags:
- GPU
- AI
- Machine Learning
- Computing
- Graphics
- FinOps
- Cost Management
- FOCUS
---
