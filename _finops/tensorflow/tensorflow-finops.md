---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tensorflow-serving-openapi.yml
  format: yaml
  label: TensorFlow Serving REST API
  slug: tensorflow-serving-rest
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tensorflow/refs/heads/main/openapi/tensorflow-serving-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Open Source
description: 'FOCUS-aligned FinOps for TensorFlow: TensorFlow itself is free open-source software (Apache 2.0); the FinOps surface is the underlying compute, accelerator, and storage spend incurred by training and serving TensorFlow workloads on cloud or on-prem infrastructure.'
focus_columns:
  BillingCurrency: USD
  ProviderName: TensorFlow
  PublisherName: TensorFlow contributors / Google LLC
  ServiceCategory: Machine Learning Framework
  ServiceName: TensorFlow
layout: finops
meters:
- aggregation: sum
  dimensions:
  - accelerator_type
  - region
  name: training_accelerator_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - accelerator_type
  - region
  name: inference_accelerator_hours
  unit: instance-hour
- aggregation: avg
  dimensions:
  - storage_class
  name: model_storage
  unit: GB-month
name: Tensorflow Finops
provider_name: TensorFlow
provider_slug: tensorflow
publisher_name: TensorFlow contributors / Google LLC (project sponsor)
service_category: Machine Learning Framework
slug: tensorflow-finops
source_filename: tensorflow-finops.yml
source_heading: FinOps Profile
source_url: https://www.tensorflow.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TensorFlow\nproviderId: tensorflow\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Machine Learning\n  - Open Source\ndescription: >-\n  FOCUS-aligned FinOps for TensorFlow: TensorFlow itself is free open-source software (Apache 2.0); the\n  FinOps surface is the underlying compute, accelerator, and storage spend incurred by training and serving\n  TensorFlow workloads on cloud or on-prem infrastructure.\nsources:\n  - https://www.tensorflow.org/\n  - https://github.com/tensorflow/tensorflow/blob/master/LICENSE\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TensorFlow contributors\
  \ / Google LLC (project sponsor)\nserviceCategory: Machine Learning Framework\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: TensorFlow\n  ServiceCategory: Machine Learning Framework\n  ProviderName: TensorFlow\n  PublisherName: TensorFlow contributors / Google LLC\n  BillingCurrency: USD\nmeters:\n  - name: training_accelerator_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - accelerator_type\n      - region\n  - name: inference_accelerator_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - accelerator_type\n      - region\n  - name: model_storage\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - storage_class\nprinciples:\n  - name: Visibility\n    description: TensorFlow itself emits no billing telemetry; visibility comes from the underlying cloud\n      provider's cost / usage reports (e.g.\
  \ GCP Billing export, AWS CUR) and from MLOps tracking (TensorBoard\n      run metadata, TFX pipeline metrics).\n  - name: Allocation\n    description: Tag training and inference jobs with project / experiment / model_id labels at the cloud\n      resource level so FOCUS BillingAccountId / tags can attribute spend back to the model owner.\n  - name: Optimization\n    description: Reduce TensorFlow infrastructure cost via mixed-precision training, distillation / quantization\n      for inference, batch and concurrency tuning in TensorFlow Serving, spot/preemptible accelerators\n      for training, and selective use of TPUs vs GPUs for the workload shape.\n  - name: Accountability\n    description: Model owner / ML platform team is accountable for per-model training and serving spend\n      and reviews unit cost per prediction or per training run on a regular cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tensorflow/refs/heads/main/finops/tensorflow-finops.yml
sources:
- https://www.tensorflow.org/
- https://github.com/tensorflow/tensorflow/blob/master/LICENSE
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Machine Learning
- Open Source
---
