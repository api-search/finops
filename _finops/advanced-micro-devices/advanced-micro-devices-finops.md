---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amd-developer-cloud-api-openapi.yml
  format: yaml
  label: AMD Developer Cloud API
  slug: amd-developer-cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/advanced-micro-devices/refs/heads/main/openapi/amd-developer-cloud-api-openapi.yml
- filename: amd-rocm-management-api-openapi.yml
  format: yaml
  label: AMD ROCm API
  slug: amd-rocm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/advanced-micro-devices/refs/heads/main/openapi/amd-rocm-management-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for AMD: hardware purchase + cloud-provider-mediated GPU-hour consumption.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Advanced Micro Devices, Inc.
  ProviderName: Advanced Micro Devices
  PublisherName: Advanced Micro Devices, Inc.
  ServiceCategory: Compute / Semiconductors
  ServiceName: AMD
layout: finops
meters:
- aggregation: sum
  dimensions:
  - sku
  - region
  - cloud_provider
  name: gpu_hours
  unit: GPU-hour
- aggregation: sum
  dimensions:
  - sku
  - reseller
  name: hardware_units
  unit: unit
- aggregation: sum
  dimensions:
  - support_tier
  name: support_subscriptions
  unit: month
name: Advanced Micro Devices Finops
provider_name: Advanced Micro Devices
provider_slug: advanced-micro-devices
publisher_name: Advanced Micro Devices, Inc.
service_category: Compute / Semiconductors
slug: advanced-micro-devices-finops
source_filename: advanced-micro-devices-finops.yml
source_heading: FinOps Profile
source_url: https://www.amd.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Advanced Micro Devices\nproviderId: advanced-micro-devices\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: AMD-issued invoices typically reflect hardware/license purchases; recurring GPU-hour\n  spend usually flows through cloud providers (AWS, Azure, OCI) rather than AMD directly.\ntags:\n  - FinOps\n  - FOCUS\n  - GPU\n  - HPC\ndescription: 'FOCUS-aligned FinOps for AMD: hardware purchase + cloud-provider-mediated GPU-hour\n  consumption.'\nsources:\n  - https://www.amd.com/\n  - https://rocm.docs.amd.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Advanced Micro Devices, Inc.\nserviceCategory: Compute / Semiconductors\nbillingModel:\n  pricingCategory:\
  \ Pay-As-You-Go + Committed Use\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: AMD\n  ServiceCategory: Compute / Semiconductors\n  ProviderName: Advanced Micro Devices\n  PublisherName: Advanced Micro Devices, Inc.\n  InvoiceIssuerName: Advanced Micro Devices, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: gpu_hours\n    unit: GPU-hour\n    aggregation: sum\n    dimensions:\n      - sku\n      - region\n      - cloud_provider\n  - name: hardware_units\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - sku\n      - reseller\n  - name: support_subscriptions\n    unit: month\n    aggregation: sum\n    dimensions:\n      - support_tier\nprinciples:\n  - name: Visibility\n    description: Track GPU-hour consumption through the hosting cloud provider's billing exports\n      (CUR, OCI Usage, Azure Cost Management); attribute hardware spend via PO-level tagging.\n  - name:\
  \ Allocation\n    description: Tag AMD-instance jobs by team/model/experiment in the cloud provider's billing\n      data.\n  - name: Optimization\n    description: Use ROCm-native frameworks to maximize GPU utilization; right-size MI300X vs MI250X\n      for workload; pursue committed-use discounts on the host cloud.\n  - name: Accountability\n    description: Assign GPU-hour budget owner; review monthly utilization and idle-GPU exposure.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/advanced-micro-devices/refs/heads/main/finops/advanced-micro-devices-finops.yml
sources:
- https://www.amd.com/
- https://rocm.docs.amd.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- GPU
- HPC
---
