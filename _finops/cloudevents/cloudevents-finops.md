---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cloudevents-http-asyncapi.yml
  format: yaml
  label: CloudEvents Specification
  slug: cloudevents-spec
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudevents/refs/heads/main/asyncapi/cloudevents-http-asyncapi.yml
- filename: cloudevents-subscriptions-openapi.yml
  format: yaml
  label: CloudEvents Subscriptions API
  slug: cloudevents-subscriptions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudevents/refs/heads/main/openapi/cloudevents-subscriptions-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: not applicable
  chargeCategories: []
  pricingCategory: Free / Open Source
description: CloudEvents itself is a free, open-source CNCF specification with no commercial cost surface. FinOps observation should focus on the platforms that emit or receive CloudEvents.
focus_columns:
  BillingCurrency: USD
  PricingCategory: Free
  ProviderName: CloudEvents
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Open Source Specification
  ServiceName: CloudEvents
layout: finops
meters:
- aggregation: sum
  description: CloudEvents has no billable meters. Track consumption on the implementing platform (EventBridge, Event Grid, Eventarc, NATS, Kafka, etc.).
  name: not_applicable
  unit: varies
name: Cloudevents Finops
provider_name: CloudEvents
provider_slug: cloudevents
publisher_name: Cloud Native Computing Foundation
service_category: Open Source Specification
slug: cloudevents-finops
source_filename: cloudevents-finops.yml
source_heading: FinOps Profile
source_url: https://cloudevents.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CloudEvents\nproviderId: cloudevents\npublisherName: Cloud Native Computing Foundation\nserviceCategory: Open Source Specification\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud Native\n  - Open Source\n  - CNCF\nnotes: CloudEvents is a free CNCF Graduated specification. There is no invoice, no usage meter, no commercial\n  surface to allocate. The shape below preserves the FinOps Framework structure but flags the artifact\n  as informational only — the meaningful FinOps surface is on the platforms that implement CloudEvents\n  (EventBridge, Event Grid, Eventarc, etc.).\ndescription: CloudEvents\
  \ itself is a free, open-source CNCF specification with no commercial cost surface.\n  FinOps observation should focus on the platforms that emit or receive CloudEvents.\nsources:\n  - https://cloudevents.io/\n  - https://github.com/cloudevents/spec\nbillingModel:\n  pricingCategory: Free / Open Source\n  billingFrequency: not applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: CloudEvents\n  ServiceCategory: Open Source Specification\n  ProviderName: CloudEvents\n  PublisherName: Cloud Native Computing Foundation\n  PricingCategory: Free\n  BillingCurrency: USD\nmeters:\n  - name: not_applicable\n    description: CloudEvents has no billable meters. Track consumption on the implementing platform (EventBridge,\n      Event Grid, Eventarc, NATS, Kafka, etc.).\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Observe CloudEvents traffic on the implementing platform's billing and metering surface;\n      CloudEvents\
  \ itself produces no spend.\n  - name: Allocation\n    description: Tag the implementing platform's resources (event buses, subscriptions, brokers) to teams\n      consuming or producing CloudEvents.\n  - name: Optimization\n    description: Right-size payload sizes and event fan-out on the implementing platform; CloudEvents structure\n      itself is overhead-light by design.\n  - name: Accountability\n    description: Ownership flows to the team operating the implementing event platform, not CloudEvents\n      itself.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudevents/refs/heads/main/finops/cloudevents-finops.yml
sources:
- https://cloudevents.io/
- https://github.com/cloudevents/spec
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud Native
- Open Source
- CNCF
---
