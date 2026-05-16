---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: resource-manager
  format: yaml
  label: Azure Event Hubs REST API
  slug: azure-event-hubs-rest-api
  spec_type: OpenAPI
  url: https://github.com/Azure/azure-rest-api-specs/tree/main/specification/eventhub/resource-manager
- filename: data-plane
  format: yaml
  label: Azure Event Hubs Data Plane API
  slug: azure-event-hubs-data-plane-api
  spec_type: OpenAPI
  url: https://github.com/Azure/azure-rest-api-specs/tree/main/specification/eventhub/data-plane
- filename: azure-event-hubs-messaging-asyncapi.yml
  format: yaml
  label: Azure Event Hubs Messaging API
  slug: azure-event-hubs-messaging-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-event-hubs/refs/heads/main/asyncapi/azure-event-hubs-messaging-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Azure Event Hubs: hourly per-TU (Basic/Standard), per-PU (Premium), and per-CU (Dedicated) billing plus per-million ingress events on Basic and Standard.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Messaging
  ServiceName: Azure Event Hubs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  - region
  - namespace
  name: throughput_unit_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - namespace
  name: processing_unit_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - cluster
  name: capacity_unit_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - namespace
  - eventhub
  name: ingress_events
  unit: event
- aggregation: sum
  dimensions:
  - namespace
  - destination
  name: capture_storage
  unit: GB
name: Microsoft Azure Event Hubs Finops
provider_name: Azure Event Hubs
provider_slug: microsoft-azure-event-hubs
publisher_name: Microsoft Corporation
service_category: Messaging / Event Streaming
slug: microsoft-azure-event-hubs-finops
source_filename: microsoft-azure-event-hubs-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/event-hubs/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Event Hubs\nproviderId: microsoft-azure-event-hubs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Event Streaming\n  - Microsoft Azure\ndescription: 'FOCUS-aligned FinOps for Azure Event Hubs: hourly per-TU (Basic/Standard), per-PU (Premium),\n  and per-CU (Dedicated) billing plus per-million ingress events on Basic and Standard.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/event-hubs/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Messaging / Event Streaming\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n\
  \  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Azure Event Hubs\n  ServiceCategory: Messaging\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: throughput_unit_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - tier\n      - region\n      - namespace\n  - name: processing_unit_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - namespace\n  - name: capacity_unit_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n  - name: ingress_events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - namespace\n      - eventhub\n  - name: capture_storage\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - namespace\n      - destination\nprinciples:\n\
  \  - name: Visibility\n    description: Use Azure Monitor metrics (Incoming Messages, Throttled Requests, Successful Requests)\n      and Cost Management cost analysis grouped by namespace.\n  - name: Allocation\n    description: Use namespace-per-team or per-product separation; tag namespaces with cost-center\n      tags; route data through dedicated namespaces for chargeback.\n  - name: Optimization\n    description: Right-size TUs/PUs; enable Auto-Inflate on Standard to avoid over-provisioning;\n      consolidate low-volume namespaces; move stable high-volume workloads to Dedicated CUs for unit\n      cost savings; use Capture instead of consumer-side ETL.\n  - name: Accountability\n    description: Assign namespace owners; alert on Throttled Requests metric; review tier choice\n      quarterly against ingress and retention needs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-event-hubs/refs/heads/main/finops/microsoft-azure-event-hubs-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/event-hubs/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Event Streaming
- Microsoft Azure
---
