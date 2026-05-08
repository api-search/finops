---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: global-relay-conversation-archiving-api-openapi.yml
  format: yaml
  label: Global Relay Conversation Archiving API
  slug: conversation-archiving-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/global-relay/refs/heads/main/openapi/global-relay-conversation-archiving-api-openapi.yml
- filename: global-relay-email-archiving-api-openapi.yml
  format: yaml
  label: Global Relay Email Archiving API
  slug: email-archiving-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/global-relay/refs/heads/main/openapi/global-relay-email-archiving-api-openapi.yml
- filename: global-relay-voice-archiving-api-openapi.yml
  format: yaml
  label: Global Relay Voice Archiving API
  slug: voice-archiving-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/global-relay/refs/heads/main/openapi/global-relay-voice-archiving-api-openapi.yml
- filename: global-relay-event-archiving-api-openapi.yml
  format: yaml
  label: Global Relay Event Archiving API
  slug: event-archiving-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/global-relay/refs/heads/main/openapi/global-relay-event-archiving-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Per-Seat Subscription
description: 'FOCUS-aligned FinOps for Global Relay: per-seat compliance archiving subscription with custom-priced storage/retention overlays. Specific rates are not publicly posted.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Global Relay Communications Inc.
  ProviderName: Global Relay
  PublisherName: Global Relay Communications Inc.
  ServiceCategory: Compliance Archiving
  ServiceName: Global Relay
layout: finops
meters:
- aggregation: max
  description: Active users covered by Global Relay Archive
  dimensions:
  - business_unit
  - data_source
  name: archived_seats
  unit: seat
- aggregation: sum
  description: Stored archive volume across all data sources
  dimensions:
  - data_source
  - retention_class
  name: archive_storage
  unit: GB-month
- aggregation: max
  description: Number of active communication-source connectors
  name: connector_count
  unit: connector
- aggregation: sum
  description: Messages reviewed via supervision/surveillance modules
  name: supervisory_review_volume
  unit: message
name: Global Relay Finops
provider_name: Global Relay
provider_slug: global-relay
publisher_name: Global Relay Communications Inc.
service_category: Compliance / Archiving
slug: global-relay-finops
source_filename: global-relay-finops.yml
source_heading: FinOps Profile
source_url: https://www.globalrelay.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Global Relay\nproviderId: global-relay\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Compliance\n  - Archiving\ndescription: 'FOCUS-aligned FinOps for Global Relay: per-seat compliance archiving subscription with custom-priced\n  storage/retention overlays. Specific rates are not publicly posted.'\nnotes: Reconcile when a published rate card is referenced.\nsources:\n  - https://www.globalrelay.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Global Relay Communications Inc.\nserviceCategory: Compliance / Archiving\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Global Relay\n  ServiceCategory: Compliance Archiving\n  ProviderName: Global Relay\n  PublisherName: Global Relay Communications Inc.\n  InvoiceIssuerName: Global Relay Communications Inc.\n  BillingCurrency: USD\nmeters:\n  - name: archived_seats\n    description: Active users covered by Global Relay Archive\n    unit: seat\n    aggregation: max\n    dimensions:\n      - business_unit\n      - data_source\n  - name: archive_storage\n    description: Stored archive volume across all data sources\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - data_source\n      - retention_class\n  - name: connector_count\n    description: Number of active communication-source connectors\n    unit: connector\n    aggregation: max\n  - name: supervisory_review_volume\n    description: Messages reviewed via supervision/surveillance modules\n    unit: message\n    aggregation: sum\n\
  principles:\n  - name: Visibility\n    description: Use the Global Relay reporting console to track licensed seat count, ingest volume,\n      and retention growth per data source.\n  - name: Allocation\n    description: Allocate seat costs to the regulated-business-unit owner; storage and retention overlays\n      to the legal/compliance budget.\n  - name: Optimization\n    description: Right-size seats by deactivating departed users promptly; tune retention class to regulatory\n      minimum; consolidate fragmented connectors.\n  - name: Accountability\n    description: Compliance and IT operations co-own Global Relay spend; renewal review is annual with\n      vendor.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/global-relay/refs/heads/main/finops/global-relay-finops.yml
sources:
- https://www.globalrelay.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Compliance
- Archiving
---
