---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dapr-state-management-openapi.yml
  format: yaml
  label: Dapr State Management API
  slug: state-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-state-management-openapi.yml
- filename: dapr-pubsub-openapi.yml
  format: yaml
  label: Dapr Pub/Sub API
  slug: pubsub
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-pubsub-openapi.yml
- filename: dapr-service-invocation-openapi.yml
  format: yaml
  label: Dapr Service Invocation API
  slug: service-invocation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-service-invocation-openapi.yml
- filename: dapr-bindings-openapi.yml
  format: yaml
  label: Dapr Bindings API
  slug: bindings
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-bindings-openapi.yml
- filename: dapr-secrets-openapi.yml
  format: yaml
  label: Dapr Secrets API
  slug: secrets
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-secrets-openapi.yml
- filename: dapr-actors-openapi.yml
  format: yaml
  label: Dapr Actors API
  slug: actors
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-actors-openapi.yml
- filename: dapr-workflow-openapi.yml
  format: yaml
  label: Dapr Workflow API
  slug: workflow
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-workflow-openapi.yml
- filename: dapr-configuration-openapi.yml
  format: yaml
  label: Dapr Configuration API
  slug: configuration
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-configuration-openapi.yml
- filename: dapr-distributed-lock-openapi.yml
  format: yaml
  label: Dapr Distributed Lock API
  slug: distributed-lock
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-distributed-lock-openapi.yml
- filename: dapr-cryptography-openapi.yml
  format: yaml
  label: Dapr Cryptography API
  slug: cryptography
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-cryptography-openapi.yml
- filename: dapr-jobs-openapi.yml
  format: yaml
  label: Dapr Jobs API
  slug: jobs
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-jobs-openapi.yml
- filename: dapr-health-openapi.yml
  format: yaml
  label: Dapr Health API
  slug: health
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-health-openapi.yml
- filename: dapr-metadata-openapi.yml
  format: yaml
  label: Dapr Metadata API
  slug: metadata
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/openapi/dapr-metadata-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  pricingCategory: Open Source / Self-Hosted
description: 'FOCUS-aligned FinOps for Dapr: there is no vendor invoice for upstream Dapr itself. Cost emerges from the underlying compute (sidecar CPU/memory), state store, message broker, and any commercial managed Dapr distribution the operator chooses (Diagrid Catalyst, Azure Container Apps Dapr extension, etc.). FinOps reporting for Dapr workloads should attach to the cloud provider that hosts the sidecars rather than to Dapr itself.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  PricingCategory: Open Source
  ProviderName: Dapr (CNCF)
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Developer Tools
  ServiceName: Dapr
  ServiceSubcategory: Distributed Application Runtime
layout: finops
meters:
- aggregation: sum
  description: CPU/memory hours consumed by Dapr sidecars (daprd) running alongside application workloads. Charged by the underlying compute provider, not by Dapr.
  dimensions:
  - cluster
  - namespace
  - app_id
  - region
  name: sidecar_compute_hours
  unit: instance-hour
- aggregation: sum
  description: Reads/writes to the configured state store backend (Redis, Cosmos DB, DynamoDB, etc.). Billed by the state-store provider.
  dimensions:
  - state_store
  - app_id
  name: state_store_operations
  unit: request
- aggregation: sum
  description: Messages published or delivered through the configured pub/sub broker (Kafka, RabbitMQ, Service Bus, etc.). Billed by the broker provider.
  dimensions:
  - broker
  - topic
  - app_id
  name: pubsub_messages
  unit: message
- aggregation: sum
  description: Network egress between Dapr sidecars and external state/broker/binding endpoints.
  dimensions:
  - region
  - destination
  name: data_egress
  unit: GB
name: Dapr Finops
provider_name: Dapr
provider_slug: dapr
publisher_name: Cloud Native Computing Foundation
service_category: Developer Tools
slug: dapr-finops
source_filename: dapr-finops.yml
source_heading: FinOps Profile
source_url: https://dapr.io
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dapr\nproviderId: dapr\npublisherName: Cloud Native Computing Foundation\nserviceCategory: Developer Tools\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Distributed Systems\n  - Microservices\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Dapr: there is no vendor invoice for upstream Dapr itself.\n  Cost emerges from the underlying compute (sidecar CPU/memory), state store, message broker, and\n  any commercial managed Dapr distribution the operator chooses (Diagrid Catalyst, Azure Container\n  Apps Dapr extension, etc.). FinOps reporting for Dapr workloads should attach to the cloud\n\
  \  provider that hosts the sidecars rather than to Dapr itself.'\nsources:\n  - https://dapr.io\n  - https://docs.dapr.io\n  - https://www.cncf.io/projects/dapr/\nnotes: No direct vendor billing. FinOps meters track underlying infrastructure spend (sidecar\n  hours, state-store IO, broker throughput) attributed to the apps that run alongside Dapr.\nbillingModel:\n  pricingCategory: Open Source / Self-Hosted\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Dapr\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: Distributed Application Runtime\n  ProviderName: Dapr (CNCF)\n  PublisherName: Cloud Native Computing Foundation\n  PricingCategory: Open Source\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: sidecar_compute_hours\n    description: CPU/memory hours consumed by Dapr sidecars (daprd) running alongside application\n      workloads. Charged by the underlying compute provider, not by\
  \ Dapr.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\n      - app_id\n      - region\n  - name: state_store_operations\n    description: Reads/writes to the configured state store backend (Redis, Cosmos DB, DynamoDB,\n      etc.). Billed by the state-store provider.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - state_store\n      - app_id\n  - name: pubsub_messages\n    description: Messages published or delivered through the configured pub/sub broker (Kafka,\n      RabbitMQ, Service Bus, etc.). Billed by the broker provider.\n    unit: message\n    aggregation: sum\n    dimensions:\n      - broker\n      - topic\n      - app_id\n  - name: data_egress\n    description: Network egress between Dapr sidecars and external state/broker/binding endpoints.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - destination\nprinciples:\n  - name: Visibility\n    description: Dapr emits Prometheus\
  \ metrics, OpenTelemetry traces, and structured logs for every\n      sidecar. Pipe these into the operator's observability stack and join with cloud-provider\n      billing exports keyed on cluster/namespace/app_id.\n  - name: Allocation\n    description: Tag every Dapr sidecar pod with team, environment, and app_id labels; allocation\n      then flows from cloud-provider billing tags rather than from a Dapr invoice.\n  - name: Optimization\n    description: Right-size sidecar resources (CPU/memory requests and limits), enable component\n      pluggability to use cheaper state stores in non-prod, batch pub/sub messages where ordering\n      allows, and use Resiliency policies to avoid runaway retry storms that amplify bill.\n  - name: Accountability\n    description: Cluster owners and platform teams own infrastructure spend; application teams own\n      per-app sidecar density. Review sidecar utilization quarterly and consolidate co-located\n      apps where the sidecar is over-provisioned.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dapr/refs/heads/main/finops/dapr-finops.yml
sources:
- https://dapr.io
- https://docs.dapr.io
- https://www.cncf.io/projects/dapr/
specification: FinOps Framework
tags:
- Distributed Systems
- Microservices
- Open Source
- FinOps
- FOCUS
---
