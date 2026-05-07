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
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-tensorflow/refs/heads/main/openapi/tensorflow-serving-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Open Source
description: 'FOCUS-aligned FinOps for Google TensorFlow: open-source, no-cost framework. Cost surfaces are entirely the underlying compute, storage, and engineer-time consumed by self-hosted TensorFlow Serving and training pipelines, not TensorFlow license fees.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (open source)
  ProviderName: TensorFlow / Google
  PublisherName: Google LLC
  ServiceCategory: AI Infrastructure
  ServiceName: Google TensorFlow
layout: finops
meters:
- aggregation: sum
  description: Inference requests handled by self-hosted TensorFlow Serving (operational metric, not a billing line)
  dimensions:
  - model
  - version
  - environment
  name: serving_inference_requests
  unit: request
- aggregation: sum
  description: Underlying compute hours consumed by TensorFlow Serving processes
  dimensions:
  - instance_type
  - accelerator
  - region
  name: serving_compute_hours
  unit: instance-hour
- aggregation: sum
  description: Compute consumed during model training / fine-tuning
  dimensions:
  - instance_type
  - accelerator
  - region
  name: training_compute_hours
  unit: instance-hour
- aggregation: avg
  description: Storage occupied by trained model artifacts and checkpoints
  dimensions:
  - storage_class
  - region
  name: model_artifact_storage
  unit: GB-month
- aggregation: sum
  description: Pre-trained model downloads from TensorFlow Hub / Kaggle Models
  dimensions:
  - model
  name: hub_model_downloads
  unit: download
name: Google Tensorflow Finops
provider_name: Google TensorFlow
provider_slug: google-tensorflow
publisher_name: TensorFlow Authors / Google LLC
service_category: AI Infrastructure
slug: google-tensorflow-finops
source_filename: google-tensorflow-finops.yml
source_heading: FinOps Profile
source_url: https://www.tensorflow.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google TensorFlow\nproviderId: google-tensorflow\npublisherName: TensorFlow Authors / Google LLC\nserviceCategory: AI Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI\n  - Machine Learning\n  - Open Source\ndescription: 'FOCUS-aligned FinOps for Google TensorFlow: open-source, no-cost framework. Cost surfaces\n  are entirely the underlying compute, storage, and engineer-time consumed by self-hosted TensorFlow\n  Serving and training pipelines, not TensorFlow license fees.'\nsources:\n  - https://www.tensorflow.org/\n  - https://github.com/tensorflow/serving\nbillingModel:\n  pricingCategory:\
  \ Open Source\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Google TensorFlow\n  ServiceCategory: AI Infrastructure\n  ProviderName: TensorFlow / Google\n  PublisherName: Google LLC\n  InvoiceIssuerName: 'N/A (open source)'\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: serving_inference_requests\n    description: Inference requests handled by self-hosted TensorFlow Serving (operational metric, not\n      a billing line)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - model\n      - version\n      - environment\n  - name: serving_compute_hours\n    description: Underlying compute hours consumed by TensorFlow Serving processes\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - instance_type\n      - accelerator\n      - region\n  - name: training_compute_hours\n    description: Compute consumed during model training / fine-tuning\n    unit: instance-hour\n\
  \    aggregation: sum\n    dimensions:\n      - instance_type\n      - accelerator\n      - region\n  - name: model_artifact_storage\n    description: Storage occupied by trained model artifacts and checkpoints\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - storage_class\n      - region\n  - name: hub_model_downloads\n    description: Pre-trained model downloads from TensorFlow Hub / Kaggle Models\n    unit: download\n    aggregation: sum\n    dimensions:\n      - model\nprinciples:\n  - name: Visibility\n    description: Track inference and training compute / storage cost in the underlying cloud bill (GCP,\n      AWS, Azure) — TensorFlow itself produces no invoice. Use Prometheus / OpenTelemetry exporters to\n      attribute requests-per-model.\n  - name: Allocation\n    description: Tag the cloud resources running TensorFlow Serving / training jobs with team, model,\n      and environment labels so attached compute spend rolls up to the consuming product.\n  - name:\
  \ Optimization\n    description: Use TFLite / quantization / pruning to shrink models; right-size accelerators; enable\n      batching in TF Serving; share inference clusters across low-traffic models.\n  - name: Accountability\n    description: Each ML team owns the cloud cost of training and serving its models; review monthly\n      training-run cost vs. model-quality lift in MLOps reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-tensorflow/refs/heads/main/finops/google-tensorflow-finops.yml
sources:
- https://www.tensorflow.org/
- https://github.com/tensorflow/serving
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI
- Machine Learning
- Open Source
---
