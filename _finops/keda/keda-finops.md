---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: keda-metrics-api-openapi.yml
  format: yaml
  label: KEDA Metrics API
  slug: keda-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/keda/refs/heads/main/openapi/keda-metrics-api-openapi.yml
- filename: keda-cloud-events-asyncapi.yml
  format: yaml
  label: KEDA CloudEventSource API
  slug: keda-cloud-event-source-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/keda/refs/heads/main/asyncapi/keda-cloud-events-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Usage
  pricingCategory: Open Source (no project fees)
description: FOCUS-aligned FinOps scaffold for KEDA. KEDA itself has no project fees; its FinOps relevance is as a cost-optimization lever - it scales workloads to zero and back on event volume, directly reducing underlying-Kubernetes spend.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Not Applicable (open source)
  ProviderName: KEDA - CNCF
  PublisherName: KEDA - CNCF
  ServiceCategory: Open-Source Kubernetes Autoscaling
  ServiceName: KEDA
layout: finops
meters:
- aggregation: max
  dimensions:
  - namespace
  - cluster
  name: scaledobject_count
  unit: scaledobject
- aggregation: sum
  dimensions:
  - scaler
  - scaledobject
  - namespace
  name: scaler_polls
  unit: poll
- aggregation: sum
  dimensions:
  - scaledobject
  - direction
  name: scaling_events
  unit: event
name: Keda Finops
provider_name: KEDA
provider_slug: keda
publisher_name: KEDA - CNCF
service_category: Open-Source Kubernetes Autoscaling
slug: keda-finops
source_filename: keda-finops.yml
source_heading: FinOps Profile
source_url: https://keda.sh/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: KEDA\nproviderId: keda\npublisherName: KEDA - CNCF\nserviceCategory: Open-Source Kubernetes Autoscaling\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Autoscaling\n  - CNCF\n  - Event-Driven\n  - Kubernetes\n  - FinOps\n  - FOCUS\n  - Open Source\ndescription: FOCUS-aligned FinOps scaffold for KEDA. KEDA itself has no project fees; its\n  FinOps relevance is as a cost-optimization lever - it scales workloads to zero and back\n  on event volume, directly reducing underlying-Kubernetes spend.\nsources:\n  - https://keda.sh/\n  - https://keda.sh/docs/latest/\n  - https://www.finops.org/framework/\n  - https://focus.finops.org/focus-specification/v1-3/\n\
  billingModel:\n  pricingCategory: Open Source (no project fees)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: KEDA\n  ServiceCategory: Open-Source Kubernetes Autoscaling\n  ProviderName: KEDA - CNCF\n  PublisherName: KEDA - CNCF\n  InvoiceIssuerName: Not Applicable (open source)\n  BillingCurrency: USD\nmeters:\n  - name: scaledobject_count\n    unit: scaledobject\n    aggregation: max\n    dimensions:\n      - namespace\n      - cluster\n  - name: scaler_polls\n    unit: poll\n    aggregation: sum\n    dimensions:\n      - scaler\n      - scaledobject\n      - namespace\n  - name: scaling_events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - scaledobject\n      - direction\nprinciples:\n  - name: Visibility\n    description: KEDA exports Prometheus metrics (keda_scaler_metrics_value, keda_scaled_object_paused,\n      keda_scaler_errors_total) and emits CloudEvents (ScaledObjectReady, ScalerError);\
  \ pipe\n      both into the cluster monitoring stack to see scaling behavior.\n  - name: Allocation\n    description: KEDA itself is not billed. Allocate the spend it influences by namespace /\n      workload and tie scaling events to the workload owner via labels.\n  - name: Optimization\n    description: KEDA is itself an optimization lever - scale-to-zero on idle queues, tune\n      pollingInterval / cooldownPeriod, and use the Multiple-Triggers pattern to scale on\n      the most cost-relevant signal.\n  - name: Accountability\n    description: Platform team owns the KEDA install; workload owners are accountable for\n      their ScaledObject definitions and the resulting cluster spend.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/keda/refs/heads/main/finops/keda-finops.yml
sources:
- https://keda.sh/
- https://keda.sh/docs/latest/
- https://www.finops.org/framework/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Autoscaling
- CNCF
- Event-Driven
- Kubernetes
- FinOps
- FOCUS
- Open Source
---
