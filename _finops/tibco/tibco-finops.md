---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: TIBCO Cloud Integration API
  slug: ''
  spec_type: OpenAPI
  url: https://integration.cloud.tibco.com/docs/api/openapi.json
- filename: io-docs
  format: yaml
  label: TIBCO Mashery API Management
  slug: ''
  spec_type: OpenAPI
  url: https://developer.mashery.com/io-docs
- filename: tibco-businessevents-openapi.yml
  format: yaml
  label: TIBCO BusinessEvents API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tibco/refs/heads/main/openapi/tibco-businessevents-openapi.yml
- filename: tibco-messaging-asyncapi.yml
  format: yaml
  label: TIBCO Messaging API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/tibco/refs/heads/main/asyncapi/tibco-messaging-asyncapi.yml
- filename: tibco-spotfire-openapi.yml
  format: yaml
  label: TIBCO Spotfire Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tibco/refs/heads/main/openapi/tibco-spotfire-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Enterprise License / Subscription
description: 'FOCUS-aligned FinOps placeholder for TIBCO: enterprise-licensed integration, analytics, and API management products sold under quote-based contracts by Cloud Software Group.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Cloud Software Group, Inc.
  ProviderName: TIBCO
  PublisherName: Cloud Software Group, Inc.
  ServiceCategory: Integration & Analytics
  ServiceName: TIBCO
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - environment
  name: licensed_entitlement
  unit: varies
name: Tibco Finops
provider_name: TIBCO
provider_slug: tibco
publisher_name: Cloud Software Group, Inc.
service_category: Integration & Analytics
slug: tibco-finops
source_filename: tibco-finops.yml
source_heading: FinOps Profile
source_url: https://www.tibco.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TIBCO\nproviderId: tibco\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Integration\n  - Analytics\n  - API Management\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for TIBCO: enterprise-licensed integration, analytics,\n  and API management products sold under quote-based contracts by Cloud Software Group.'\nsources:\n  - https://www.tibco.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: TIBCO does not expose a public usage-based rate card or billing API. FinOps observability comes\n  from contract-line allocation, not per-call telemetry.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cloud Software Group,\
  \ Inc.\nserviceCategory: Integration & Analytics\nbillingModel:\n  pricingCategory: Enterprise License / Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TIBCO\n  ServiceCategory: Integration & Analytics\n  ProviderName: TIBCO\n  PublisherName: Cloud Software Group, Inc.\n  InvoiceIssuerName: Cloud Software Group, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: licensed_entitlement\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\n      - environment\nprinciples:\n  - name: Visibility\n    description: Map TIBCO contract entitlements (cores, instances, named users, API tier) to deployments;\n      pull usage from product-native dashboards (Spotfire, BusinessWorks, Mashery analytics).\n  - name: Allocation\n    description: Allocate the TIBCO contract cost to the integration, analytics, or API platform team\n      that owns each product line.\n  - name: Optimization\n    description:\
  \ At renewal, right-size cores/instances and consolidate duplicate environments; retire\n      unused Spotfire seats and BusinessWorks engines.\n  - name: Accountability\n    description: A platform owner is accountable for the TIBCO master agreement, true-up cycle, and renewal\n      negotiation with Cloud Software Group.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tibco/refs/heads/main/finops/tibco-finops.yml
sources:
- https://www.tibco.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Integration
- Analytics
- API Management
- FinOps
- FOCUS
---
