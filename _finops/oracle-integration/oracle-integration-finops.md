---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-integration-developer-api.yaml
  format: yaml
  label: Oracle Integration Developer API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-integration/refs/heads/main/openapi/oracle-integration-developer-api.yaml
- filename: oracle-integration-process-automation-api.yaml
  format: yaml
  label: Oracle Integration Process Automation API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-integration/refs/heads/main/openapi/oracle-integration-process-automation-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go (Per-Edition Hourly)
description: 'FOCUS-aligned FinOps view for Oracle Integration: per-hour billing of the service edition (Standard / Enterprise / Healthcare) multiplied by the provisioned message-pack count, plus separate OCI charges for outbound data transfer and any auxiliary OCI resources (object storage, identity domains). FinOps observation focuses on edition + message-pack utilization, active integrations, and File Server storage against the contractual edition.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: Pay-As-You-Go
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: Integration / iPaaS
  ServiceName: Oracle Integration
layout: finops
meters:
- aggregation: sum
  description: Message-pack hours consumed by Oracle Integration instances
  dimensions:
  - edition
  - region
  - instance
  - tag
  name: oic_message_pack_hours
  unit: message-pack-hour
- aggregation: max
  description: Active integrations against the per-instance cap of 700
  dimensions:
  - instance
  - environment
  name: oic_active_integrations
  unit: integrations
- aggregation: max
  description: File Server storage consumed against the 500 GB per-instance cap
  dimensions:
  - instance
  name: oic_file_server_storage_gb
  unit: GB
- aggregation: sum
  description: Daily outbound notification emails against the 10,000 per-instance cap
  dimensions:
  - instance
  - day
  name: oic_outbound_email
  unit: emails
- aggregation: sum
  description: Outbound data transfer attributable to Oracle Integration
  dimensions:
  - region
  name: oci_egress_gb
  unit: GB
name: Oracle Integration Finops
provider_name: Oracle Integration
provider_slug: oracle-integration
publisher_name: Oracle America, Inc.
service_category: Integration / iPaaS
slug: oracle-integration-finops
source_filename: oracle-integration-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/integration/integration-cloud/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Integration\nproviderId: oracle-integration\npublisherName: Oracle America, Inc.\nserviceCategory: Integration / iPaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - iPaaS\n  - Cloud Integration\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle Integration: per-hour billing of the\n  service edition (Standard / Enterprise / Healthcare) multiplied by the\n  provisioned message-pack count, plus separate OCI charges for outbound\n  data transfer and any auxiliary OCI resources (object storage, identity\n  domains). FinOps observation focuses on edition + message-pack\
  \ utilization,\n  active integrations, and File Server storage against the contractual\n  edition.\nsources:\n  - https://www.oracle.com/integration/integration-cloud/\n  - https://docs.oracle.com/en/cloud/paas/application-integration/\n  - https://www.oracle.com/cloud/price-list/\nnotes: >-\n  Per-hour message-pack price is not publicly fetchable. Track edition,\n  message-pack hours, and active-integration count via OCI Cost Analysis and\n  the Oracle Integration monitoring dashboards.\nbillingModel:\n  pricingCategory: Pay-As-You-Go (Per-Edition Hourly)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle Integration\n  ServiceCategory: Integration / iPaaS\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: Pay-As-You-Go\n  ChargeCategory: Usage\nmeters:\n \
  \ - name: oic_message_pack_hours\n    description: Message-pack hours consumed by Oracle Integration instances\n    unit: message-pack-hour\n    aggregation: sum\n    dimensions:\n      - edition\n      - region\n      - instance\n      - tag\n  - name: oic_active_integrations\n    description: Active integrations against the per-instance cap of 700\n    unit: integrations\n    aggregation: max\n    dimensions:\n      - instance\n      - environment\n  - name: oic_file_server_storage_gb\n    description: File Server storage consumed against the 500 GB per-instance cap\n    unit: GB\n    aggregation: max\n    dimensions:\n      - instance\n  - name: oic_outbound_email\n    description: Daily outbound notification emails against the 10,000 per-instance cap\n    unit: emails\n    aggregation: sum\n    dimensions:\n      - instance\n      - day\n  - name: oci_egress_gb\n    description: Outbound data transfer attributable to Oracle Integration\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - region\nprinciples:\n  - name: Visibility\n    description: >-\n      Use OCI Cost Analysis with cost-tracking tags applied to each Oracle\n      Integration instance, and the Oracle Integration monitoring dashboards\n      for active integrations, message volume, and File Server consumption.\n  - name: Allocation\n    description: >-\n      Apply cost-tracking tags (e.g. team, business_capability, environment)\n      to each instance so iPaaS spend can be allocated back to the consuming\n      product line.\n  - name: Optimization\n    description: >-\n      Right-size message-pack count to peak concurrent messages, drop unused\n      activated integrations to stay below the 700-integration cap, and\n      consolidate low-volume tenants onto shared instances. Move bursty\n      bulk workloads onto scheduled integrations to flatten message-pack\n      demand.\n  - name: Accountability\n    description: >-\n      Assign an integration center-of-excellence owner per instance; review\n\
  \      message-pack utilization and edition fit at quarterly business\n      reviews and at each renewal.\napis:\n  - name: Oracle Integration Developer API\n    serviceName: Oracle Integration Developer API\n    serviceCategory: Integration / iPaaS\n  - name: Oracle Integration Process Automation API\n    serviceName: Oracle Integration Process Automation API\n    serviceCategory: Integration / iPaaS\n  - name: Oracle Integration File Server API\n    serviceName: Oracle Integration File Server API\n    serviceCategory: Integration / iPaaS\n  - name: Oracle Integration Administrative API\n    serviceName: Oracle Integration Administrative API\n    serviceCategory: Integration / iPaaS\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-integration/refs/heads/main/finops/oracle-integration-finops.yml
sources:
- https://www.oracle.com/integration/integration-cloud/
- https://docs.oracle.com/en/cloud/paas/application-integration/
- https://www.oracle.com/cloud/price-list/
specification: FinOps Framework
tags:
- iPaaS
- Cloud Integration
- Oracle Cloud
- FinOps
- FOCUS
---
