---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: client-server
  format: yaml
  label: Synapse Client-Server API
  slug: synapse-client-server-api
  spec_type: OpenAPI
  url: https://github.com/matrix-org/matrix-spec/tree/main/data/api/client-server
- filename: server-server
  format: yaml
  label: Synapse Server-Server API
  slug: synapse-server-server-api
  spec_type: OpenAPI
  url: https://github.com/matrix-org/matrix-spec/tree/main/data/api/server-server
- filename: synapse-admin-api-openapi.yml
  format: yaml
  label: Synapse Admin API
  slug: synapse-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/synapse/refs/heads/main/openapi/synapse-admin-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous (Operator Infra)
  chargeCategories:
  - Usage
  pricingCategory: Open-Source (Operator-Hosted)
description: FOCUS-aligned FinOps for Synapse - the software is free (AGPL-3.0) so all cost is operator-borne infrastructure. The billing surface is the operator's underlying compute, database, media storage, and federation egress invoice rather than a Synapse-issued invoice. Element Server Suite is a separately-priced commercial distribution.
focus_columns:
  BillingCurrency: USD
  ProviderName: Element / matrix-org
  PublisherName: Element (New Vector Ltd.)
  ServiceCategory: Open-Source Messaging Infrastructure
  ServiceName: Synapse Matrix Homeserver
layout: finops
meters:
- aggregation: max
  description: MAUs on the homeserver - the most useful unit for sizing compute and database load.
  dimensions:
  - server
  name: monthly_active_users
  unit: user
- aggregation: sum
  description: Bytes exchanged over federation; drives egress and database growth on busy public rooms.
  dimensions:
  - server
  - peer
  name: federation_traffic
  unit: GB
- aggregation: max
  description: Media repository storage (uploads, thumbnails) - persistent storage cost.
  dimensions:
  - server
  name: media_storage
  unit: GB-month
- aggregation: max
  description: Postgres-backing database growth - the dominant operator cost on large deployments.
  dimensions:
  - server
  name: postgres_storage
  unit: GB-month
- aggregation: sum
  description: Persisted room events; drives database write IO and disk consumption.
  dimensions:
  - server
  - room
  name: room_event_volume
  unit: event
name: Synapse Finops
provider_name: Synapse
provider_slug: synapse
publisher_name: Element (New Vector Ltd.) / matrix-org community
service_category: Open-Source Messaging Infrastructure
slug: synapse-finops
source_filename: synapse-finops.yml
source_heading: FinOps Profile
source_url: https://element-hq.github.io/synapse/latest/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Synapse\nproviderId: synapse\npublisherName: Element (New Vector Ltd.) / matrix-org community\nserviceCategory: Open-Source Messaging Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Matrix\n  - Open Source\n  - Messaging\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Synapse - the software is free (AGPL-3.0) so all cost is operator-borne infrastructure. The billing surface is the operator's underlying compute, database, media storage, and federation egress invoice rather than a Synapse-issued invoice. Element Server Suite is a separately-priced commercial distribution.\nsources:\n  - https://element-hq.github.io/synapse/latest/\n\
  \  - https://github.com/element-hq/synapse\nbillingModel:\n  pricingCategory: Open-Source (Operator-Hosted)\n  billingFrequency: Continuous (Operator Infra)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Synapse Matrix Homeserver\n  ServiceCategory: Open-Source Messaging Infrastructure\n  ProviderName: Element / matrix-org\n  PublisherName: Element (New Vector Ltd.)\n  BillingCurrency: USD\nmeters:\n  - name: monthly_active_users\n    description: MAUs on the homeserver - the most useful unit for sizing compute and database load.\n    unit: user\n    aggregation: max\n    dimensions:\n      - server\n  - name: federation_traffic\n    description: Bytes exchanged over federation; drives egress and database growth on busy public rooms.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - server\n      - peer\n  - name: media_storage\n    description: Media repository storage (uploads, thumbnails) - persistent storage cost.\n    unit: GB-month\n\
  \    aggregation: max\n    dimensions:\n      - server\n  - name: postgres_storage\n    description: Postgres-backing database growth - the dominant operator cost on large deployments.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - server\n  - name: room_event_volume\n    description: Persisted room events; drives database write IO and disk consumption.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - server\n      - room\nprinciples:\n  - name: Visibility\n    description: Synapse exposes Prometheus metrics and an Admin API that surface MAUs, federation traffic, room-event rates, and media storage; pair these with the cloud bill to attribute Synapse-driven cost.\n  - name: Allocation\n    description: Operators allocate against the homeserver they run; multi-tenant operators can use room-level / appservice-level metrics to apportion infra cost to internal customers.\n  - name: Optimization\n    description: Tune `ratelimiting` defaults, enable workers\
  \ to scale federation independently, prune old media, archive old room state, and scope federation reachability to control egress.\n  - name: Accountability\n    description: The platform team running the Matrix homeserver owns Synapse cost; Element is the commercial counterparty only if ESS is purchased.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/synapse/refs/heads/main/finops/synapse-finops.yml
sources:
- https://element-hq.github.io/synapse/latest/
- https://github.com/element-hq/synapse
specification: FinOps Framework
tags:
- Matrix
- Open Source
- Messaging
- FinOps
- FOCUS
---
