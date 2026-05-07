---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: prometheus-http-api-openapi.yml
  format: yaml
  label: Prometheus HTTP API
  slug: prometheus-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/openapi/prometheus-http-api-openapi.yml
- filename: prometheus-management-api-openapi.yml
  format: yaml
  label: Prometheus Management API
  slug: prometheus-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/openapi/prometheus-management-api-openapi.yml
- filename: prometheus-pushgateway-api-openapi.yml
  format: yaml
  label: Prometheus Pushgateway API
  slug: prometheus-pushgateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/openapi/prometheus-pushgateway-api-openapi.yml
- filename: prometheus-alertmanager-api-openapi.yml
  format: yaml
  label: Prometheus Alertmanager API
  slug: prometheus-alertmanager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/openapi/prometheus-alertmanager-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Open Source
description: FOCUS-aligned FinOps shape for Prometheus. Prometheus has no vendor invoice — it is Apache 2.0 software. The FinOps surface is therefore the operator's own infrastructure cost (compute, storage, network) for running the server, exporters, and remote-write / long-term-storage backends.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: n/a (self-hosted)
  ProviderName: Prometheus
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Observability
  ServiceName: Prometheus
layout: finops
meters:
- aggregation: sum
  dimensions:
  - role
  - environment
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - retention_tier
  name: persistent_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - destination
  name: network_egress
  unit: GB
name: Prometheus Finops
provider_name: Prometheus
provider_slug: prometheus
publisher_name: Cloud Native Computing Foundation
service_category: Observability
slug: prometheus-finops
source_filename: prometheus-finops.yml
source_heading: FinOps Profile
source_url: https://prometheus.io/docs/introduction/overview/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Prometheus\nproviderId: prometheus\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Observability\n  - Monitoring\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Prometheus. Prometheus has no vendor invoice — it is Apache\n  2.0 software. The FinOps surface is therefore the operator's own infrastructure cost (compute, storage,\n  network) for running the server, exporters, and remote-write / long-term-storage backends.\nnotes: There is no Prometheus vendor billing. Cost lives in the underlying infrastructure provider (AWS,\n  GCP, on-prem) and is observable via that provider's FOCUS export, not via Prometheus.\nsources:\n  - https://prometheus.io/docs/introduction/overview/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cloud Native Computing Foundation\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Prometheus\n  ServiceCategory: Observability\n  ProviderName: Prometheus\n  PublisherName: Cloud Native Computing Foundation\n  InvoiceIssuerName: 'n/a (self-hosted)'\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - role\n      - environment\n  - name: persistent_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - retention_tier\n  - name: network_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - destination\nprinciples:\n  - name: Visibility\n    description: Cost visibility comes from the infrastructure provider's FOCUS / billing\
  \ export, not\n      from Prometheus itself; Prometheus can however scrape and report its own resource consumption\n      (process_resident_memory_bytes, prometheus_tsdb_head_series).\n  - name: Allocation\n    description: Allocate Prometheus infrastructure cost by Kubernetes namespace, team, or environment\n      using cloud-provider tags; tenancy lives in your deployment topology, not in the binary.\n  - name: Optimization\n    description: Right-size scrape interval, retention, and series cardinality; offload long-term storage\n      to remote_write (Thanos, Mimir, Cortex) and tune `queue_config`.\n  - name: Accountability\n    description: Spend is owned by the platform / SRE team operating the Prometheus stack; there is\n      no vendor invoice.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/finops/prometheus-finops.yml
sources:
- https://prometheus.io/docs/introduction/overview/
specification: FinOps Framework
tags:
- Observability
- Monitoring
- Open Source
- FinOps
- FOCUS
---
