---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rest_api.yaml
  format: yaml
  label: Triton HTTP/REST API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/triton-inference-server/server/blob/main/docs/protocol/rest_api.yaml
- filename: triton-metrics-openapi.yml
  format: yaml
  label: Triton Metrics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/triton/refs/heads/main/openapi/triton-metrics-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous (Compute) / Annual (Optional Support)
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Self-Hosted Open Source
description: 'FOCUS-aligned FinOps for NVIDIA Triton Inference Server: open-source, self-hosted software with no per-call NVIDIA charge. Real cost is the underlying compute (GPU / CPU hours) the operator consumes to serve inference, plus any optional NVIDIA AI Enterprise support contract.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: NVIDIA Corporation
  ProviderName: NVIDIA
  PublisherName: NVIDIA Corporation
  ServiceCategory: AI Infrastructure / Model Serving
  ServiceName: Triton Inference Server
layout: finops
meters:
- aggregation: sum
  dimensions:
  - gpu_type
  - cluster
  - model
  name: gpu_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - cluster
  - model
  name: cpu_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - model
  - backend
  - protocol
  name: inference_requests
  unit: request
- aggregation: sum
  dimensions:
  - tier
  name: ai_enterprise_subscription
  unit: month
name: Triton Finops
provider_name: Triton Inference Server
provider_slug: triton
publisher_name: NVIDIA Corporation
service_category: AI Infrastructure / Model Serving
slug: triton-finops
source_filename: triton-finops.yml
source_heading: FinOps Profile
source_url: https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/index.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Triton Inference Server\nproviderId: triton\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI\n  - Inference\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for NVIDIA Triton Inference Server: open-source, self-hosted\n  software with no per-call NVIDIA charge. Real cost is the underlying compute (GPU / CPU hours)\n  the operator consumes to serve inference, plus any optional NVIDIA AI Enterprise support contract.'\nsources:\n  - https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/index.html\n  - https://github.com/triton-inference-server/server\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: NVIDIA\
  \ Corporation\nserviceCategory: AI Infrastructure / Model Serving\nbillingModel:\n  pricingCategory: Self-Hosted Open Source\n  billingFrequency: Continuous (Compute) / Annual (Optional Support)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Triton Inference Server\n  ServiceCategory: AI Infrastructure / Model Serving\n  ProviderName: NVIDIA\n  PublisherName: NVIDIA Corporation\n  InvoiceIssuerName: NVIDIA Corporation\n  BillingCurrency: USD\nmeters:\n  - name: gpu_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - gpu_type\n      - cluster\n      - model\n  - name: cpu_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - model\n  - name: inference_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - model\n      - backend\n      - protocol\n  - name: ai_enterprise_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n \
  \     - tier\nprinciples:\n  - name: Visibility\n    description: Use Triton's Prometheus metrics endpoint (port 8002) to track inference request\n      counts, latencies, GPU utilization, and queue time per model; pair with the underlying\n      cloud / on-prem cost telemetry for total cost-of-inference.\n  - name: Allocation\n    description: Allocate inference cost by model, backend (TensorRT, ONNX, PyTorch, Python),\n      protocol (HTTP / gRPC), and consuming team using the model name and Triton tags as the\n      primary dimensions.\n  - name: Optimization\n    description: Optimization levers are operator-controlled — enable dynamic batching, tune\n      instance group counts, mix CPU and GPU instance groups, use TensorRT or ONNX-Runtime\n      backends for lower latency / higher throughput per dollar, and use the Model Analyzer to\n      pick batch sizes.\n  - name: Accountability\n    description: Platform / MLOps team owns the Triton deployment and underlying cluster cost; per-model\n\
  \      owners are accountable for their model's GPU-hour consumption and queue behavior.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/triton/refs/heads/main/finops/triton-finops.yml
sources:
- https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/index.html
- https://github.com/triton-inference-server/server
specification: FinOps Framework
tags:
- AI
- Inference
- Open Source
- FinOps
- FOCUS
---
