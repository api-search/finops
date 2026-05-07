---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Hugging Face Inference API
  slug: ''
  spec_type: OpenAPI
  url: https://huggingface.co/api-inference/openapi.json
- filename: openapi.json
  format: json
  label: Hugging Face Hub API
  slug: ''
  spec_type: OpenAPI
  url: https://huggingface.co/.well-known/openapi.json
- filename: hugging-face-inference-endpoints-api.yml
  format: yaml
  label: Hugging Face Inference Endpoints API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hugging-face/refs/heads/main/openapi/hugging-face-inference-endpoints-api.yml
- filename: hugging-face-inference-providers-api.yml
  format: yaml
  label: Hugging Face Inference Providers API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hugging-face/refs/heads/main/openapi/hugging-face-inference-providers-api.yml
- filename: openapi.json
  format: json
  label: Hugging Face Dataset Viewer API
  slug: ''
  spec_type: OpenAPI
  url: https://datasets-server.huggingface.co/openapi.json
- filename: hugging-face-text-generation-inference-api.yml
  format: yaml
  label: Hugging Face Text Generation Inference API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hugging-face/refs/heads/main/openapi/hugging-face-text-generation-inference-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Credit
  - Adjustment
  - Tax
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Hugging Face: per-seat subscriptions plus pay-as-you-go inference credits, per-instance-hour for Inference Endpoints and Spaces, and per-TB-month storage with volume discounts.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Hugging Face, Inc.
  ProviderName: Hugging Face
  PublisherName: Hugging Face, Inc.
  ServiceCategory: AI Infrastructure
  ServiceName: Hugging Face
layout: finops
meters:
- aggregation: max
  description: PRO ($9/mo), Team ($20/seat/mo), Enterprise ($50+/seat/mo) seat fees.
  dimensions:
  - plan
  - organization
  name: subscription_seats
  unit: seat
- aggregation: sum
  description: Pay-as-you-go credits consumed against partner inference providers; pass-through provider rate, no HF markup.
  dimensions:
  - provider
  - model
  - task
  - organization
  name: inference_provider_credits
  unit: USD
- aggregation: sum
  description: Replica-hours for dedicated Inference Endpoints, billed by hardware tier.
  dimensions:
  - hardware
  - cloud
  - region
  - endpoint
  name: inference_endpoint_hours
  unit: instance-hour
- aggregation: sum
  description: Hourly cost of Spaces hardware (CPU upgrade, T4, L4, A10G, A100, etc).
  dimensions:
  - hardware
  - space
  - owner
  name: spaces_hardware_hours
  unit: instance-hour
- aggregation: avg
  description: Tiered TB-month storage for public and private repos with volume discounts at 50/200/500 TB.
  dimensions:
  - repo_type
  - tier
  - owner
  name: hub_storage
  unit: GB-month
- aggregation: sum
  description: H200 GPU-seconds consumed under the ZeroGPU shared pool (free tier with quotas by plan).
  dimensions:
  - plan
  - space
  name: zerogpu_seconds
  unit: second
name: Hugging Face Finops
provider_name: Hugging Face
provider_slug: hugging-face
publisher_name: Hugging Face, Inc.
service_category: AI Infrastructure
slug: hugging-face-finops
source_filename: hugging-face-finops.yml
source_heading: FinOps Profile
source_url: https://huggingface.co/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Hugging Face\nproviderId: hugging-face\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI\n  - Machine Learning\n  - Inference\ndescription: 'FOCUS-aligned FinOps for Hugging Face: per-seat subscriptions plus pay-as-you-go inference\n  credits, per-instance-hour for Inference Endpoints and Spaces, and per-TB-month storage with volume\n  discounts.'\nsources:\n  - https://huggingface.co/pricing\n  - https://huggingface.co/docs/inference-providers/pricing\n  - https://huggingface.co/docs/inference-endpoints/pricing\n  - https://huggingface.co/settings/billing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Hugging Face, Inc.\nserviceCategory:\
  \ AI Infrastructure\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Credit\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Hugging Face\n  ServiceCategory: AI Infrastructure\n  ProviderName: Hugging Face\n  PublisherName: Hugging Face, Inc.\n  InvoiceIssuerName: Hugging Face, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: subscription_seats\n    description: PRO ($9/mo), Team ($20/seat/mo), Enterprise ($50+/seat/mo) seat fees.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n      - organization\n  - name: inference_provider_credits\n    description: Pay-as-you-go credits consumed against partner inference providers; pass-through\n      provider rate, no HF markup.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - provider\n      - model\n      - task\n      - organization\n  - name: inference_endpoint_hours\n\
  \    description: Replica-hours for dedicated Inference Endpoints, billed by hardware tier.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - hardware\n      - cloud\n      - region\n      - endpoint\n  - name: spaces_hardware_hours\n    description: Hourly cost of Spaces hardware (CPU upgrade, T4, L4, A10G, A100, etc).\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - hardware\n      - space\n      - owner\n  - name: hub_storage\n    description: Tiered TB-month storage for public and private repos with volume discounts at 50/200/500\n      TB.\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - repo_type\n      - tier\n      - owner\n  - name: zerogpu_seconds\n    description: H200 GPU-seconds consumed under the ZeroGPU shared pool (free tier with quotas by\n      plan).\n    unit: second\n    aggregation: sum\n    dimensions:\n      - plan\n      - space\nprinciples:\n  - name: Visibility\n    description: Track spending\
  \ in the billing settings (https://huggingface.co/settings/billing)\n      and the Inference Providers usage breakdown by model and provider. Organizations see pooled\n      usage on the org billing page.\n  - name: Allocation\n    description: Use the X-HF-Bill-To header to attribute Inference Providers requests to a specific\n      organization. Tag Spaces and Inference Endpoints with metadata for team/product chargeback.\n  - name: Optimization\n    description: Use \":cheapest\" provider routing policy for cost-sensitive workloads; bring your\n      own provider key when you have negotiated rates with a specific partner; scale Inference Endpoints\n      to zero when idle; use ZeroGPU for low-traffic Spaces; consolidate storage to take advantage\n      of 50/200/500 TB volume discounts.\n  - name: Accountability\n    description: Team and Enterprise admins set spending limits and disable specific Inference Providers\n      from organization settings. Reconcile monthly invoices against\
  \ the per-model usage breakdown\n      to attribute spend back to product owners.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hugging-face/refs/heads/main/finops/hugging-face-finops.yml
sources:
- https://huggingface.co/pricing
- https://huggingface.co/docs/inference-providers/pricing
- https://huggingface.co/docs/inference-endpoints/pricing
- https://huggingface.co/settings/billing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI
- Machine Learning
- Inference
---
