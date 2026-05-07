---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rainbow-application-openapi.yml
  format: yaml
  label: Rainbow Application Portal API
  slug: rainbow-application-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rainbow/refs/heads/main/openapi/rainbow-application-openapi.yml
- filename: rainbow-messaging-openapi.yml
  format: yaml
  label: Rainbow Messaging API
  slug: rainbow-messaging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rainbow/refs/heads/main/openapi/rainbow-messaging-openapi.yml
- filename: rainbow-contacts-openapi.yml
  format: yaml
  label: Rainbow Contacts API
  slug: rainbow-contacts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rainbow/refs/heads/main/openapi/rainbow-contacts-openapi.yml
billing_model:
  billingCurrency: USD/EUR
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Enterprise CPaaS Contract
description: FOCUS-aligned FinOps for Rainbow CPaaS is contract-based; chat, voice, video, and telephony consumption is billed under the ALE customer agreement rather than a public per-API tariff.
focus_columns:
  BillingCurrency: USD/EUR
  InvoiceIssuerName: Alcatel-Lucent Enterprise
  ProviderName: Alcatel-Lucent Enterprise
  PublisherName: Alcatel-Lucent Enterprise
  ServiceCategory: Communications
  ServiceName: Rainbow
layout: finops
meters:
- aggregation: max
  description: Active Rainbow user accounts on the customer's CPaaS deployment.
  dimensions:
  - tenant
  - region
  name: licensed_users
  unit: seat
- aggregation: sum
  description: Voice and PBX minutes routed through the Rainbow telephony surface.
  dimensions:
  - tenant
  - destination_country
  name: telephony_minutes
  unit: minute
- aggregation: sum
  description: API and SDK usage covered under the ALE production contract; not exposed as a public per-call meter.
  dimensions:
  - tenant
  name: api_engagement
  unit: varies
name: Rainbow Finops
provider_name: Rainbow
provider_slug: rainbow
publisher_name: Alcatel-Lucent Enterprise
service_category: Communications
slug: rainbow-finops
source_filename: rainbow-finops.yml
source_heading: FinOps Profile
source_url: https://www.al-enterprise.com/en/products/communications/rainbow
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Rainbow\nproviderId: rainbow\npublisherName: Alcatel-Lucent Enterprise\nserviceCategory: Communications\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Communications\n  - CPaaS\n  - FinOps\n  - FOCUS\nnotes: Rainbow does not publish a per-API meter or invoice surface; FinOps mapping is anchored to the\n  ALE production contract.\ndescription: FOCUS-aligned FinOps for Rainbow CPaaS is contract-based; chat, voice, video, and telephony\n  consumption is billed under the ALE customer agreement rather than a public per-API tariff.\nsources:\n  - https://www.al-enterprise.com/en/products/communications/rainbow\n  - https://developers.openrainbow.com/\n\
  billingModel:\n  pricingCategory: Enterprise CPaaS Contract\n  billingFrequency: Monthly\n  billingCurrency: USD/EUR\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Rainbow\n  ServiceCategory: Communications\n  ProviderName: Alcatel-Lucent Enterprise\n  PublisherName: Alcatel-Lucent Enterprise\n  InvoiceIssuerName: Alcatel-Lucent Enterprise\n  BillingCurrency: USD/EUR\nmeters:\n  - name: licensed_users\n    description: Active Rainbow user accounts on the customer's CPaaS deployment.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n      - region\n  - name: telephony_minutes\n    description: Voice and PBX minutes routed through the Rainbow telephony surface.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - tenant\n      - destination_country\n  - name: api_engagement\n    description: API and SDK usage covered under the ALE production contract; not exposed as a public\n      per-call meter.\n    unit: varies\n  \
  \  aggregation: sum\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Pull licensed-user and telephony-minute reports from the ALE Rainbow administration\n      console; production deployments expose tenant-level usage to administrators.\n  - name: Allocation\n    description: Allocate Rainbow seat and telephony spend to the consuming business unit or location;\n      tenant scoping makes per-department attribution straightforward.\n  - name: Optimization\n    description: Right-size licensed-user counts at renewal and tune telephony routing to minimize cross-region\n      egress; consolidate developer hub experimentation under a shared sandbox tenant.\n  - name: Accountability\n    description: Communications IT owns the Rainbow contract; finance reviews seat and minute consumption\n      against the ALE agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rainbow/refs/heads/main/finops/rainbow-finops.yml
sources:
- https://www.al-enterprise.com/en/products/communications/rainbow
- https://developers.openrainbow.com/
specification: FinOps Framework
tags:
- Communications
- CPaaS
- FinOps
- FOCUS
---
