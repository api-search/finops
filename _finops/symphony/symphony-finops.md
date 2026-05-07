---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: symphony-pod-api-openapi.yml
  format: yaml
  label: Symphony Pod API
  slug: symphony-pod-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/symphony/refs/heads/main/openapi/symphony-pod-api-openapi.yml
- filename: agent-openapi-original.yml
  format: yaml
  label: Symphony Agent API
  slug: symphony-agent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/symphony/refs/heads/main/openapi/agent-openapi-original.yml
- filename: authenticator-openapi-original.yml
  format: yaml
  label: Symphony Authenticator API
  slug: symphony-authenticator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/symphony/refs/heads/main/openapi/authenticator-openapi-original.yml
- filename: login-openapi-original.yml
  format: yaml
  label: Symphony Login API
  slug: symphony-login-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/symphony/refs/heads/main/openapi/login-openapi-original.yml
- filename: profile-manager-openapi-original.yml
  format: yaml
  label: Symphony Profile Manager API
  slug: symphony-profile-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/symphony/refs/heads/main/openapi/profile-manager-openapi-original.yml
- filename: community-connect-openapi-original.yml
  format: yaml
  label: Symphony Community Connect API
  slug: symphony-community-connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/symphony/refs/heads/main/openapi/community-connect-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription (Enterprise)
description: Symphony is a contact-sales enterprise collaboration platform; APIs are included with the tenancy. There is no published per-call pricing or FOCUS-aligned cost export, so FinOps shape is approximated against the negotiated tenancy / seat invoice.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Symphony Communication Services, LLC
  ProviderName: Symphony
  PublisherName: Symphony Communication Services, LLC
  ServiceCategory: Secure Collaboration / Messaging
  ServiceName: Symphony
layout: finops
meters:
- aggregation: sum
  description: Symphony pod tenancy - the foundational commercial unit covering Pod and Agent API access.
  name: pod_tenancy
  unit: month
- aggregation: max
  description: Licensed user seats on the pod; the primary per-user commercial unit.
  name: licensed_seats
  unit: seat
- aggregation: count
  description: Cross-tenant Community Connect relationships, typically negotiated separately.
  name: community_connect_relationships
  unit: relationship
name: Symphony Finops
provider_name: Symphony
provider_slug: symphony
publisher_name: Symphony Communication Services, LLC
service_category: Secure Collaboration / Messaging
slug: symphony-finops
source_filename: symphony-finops.yml
source_heading: FinOps Profile
source_url: https://symphony.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Symphony\nproviderId: symphony\npublisherName: Symphony Communication Services, LLC\nserviceCategory: Secure Collaboration / Messaging\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Secure Messaging\n  - Financial Services\n  - Collaboration\n  - FinOps\n  - FOCUS\ndescription: Symphony is a contact-sales enterprise collaboration platform; APIs are included with the tenancy. There is no published per-call pricing or FOCUS-aligned cost export, so FinOps shape is approximated against the negotiated tenancy / seat invoice.\nsources:\n  - https://symphony.com\n  - https://docs.developers.symphony.com\nnotes: No public per-call\
  \ pricing or FOCUS-aligned billing export. Cost data must be reconciled from the negotiated Symphony tenancy invoice (typically per-pod plus per-seat).\nbillingModel:\n  pricingCategory: Subscription (Enterprise)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Symphony\n  ServiceCategory: Secure Collaboration / Messaging\n  ProviderName: Symphony\n  PublisherName: Symphony Communication Services, LLC\n  InvoiceIssuerName: Symphony Communication Services, LLC\n  BillingCurrency: USD\nmeters:\n  - name: pod_tenancy\n    description: Symphony pod tenancy - the foundational commercial unit covering Pod and Agent API access.\n    unit: month\n    aggregation: sum\n  - name: licensed_seats\n    description: Licensed user seats on the pod; the primary per-user commercial unit.\n    unit: seat\n    aggregation: max\n  - name: community_connect_relationships\n    description: Cross-tenant Community Connect relationships,\
  \ typically negotiated separately.\n    unit: relationship\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Pod administrators see seat consumption and bot/app inventory through the Symphony admin console; cost reconciliation happens against the negotiated invoice rather than a usage API.\n  - name: Allocation\n    description: Allocate by business unit to seat counts and named bots; Community Connect cost can be allocated to the cross-firm relationship that owns it.\n  - name: Optimization\n    description: Optimize by reclaiming inactive seats, consolidating bots that hold redundant entitlements, and bundling Community Connect relationships at contract renewal.\n  - name: Accountability\n    description: Pod owner (typically central IT or compliance) and the Symphony account team jointly own commercial reviews; line-of-business sponsors own seat allocations.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/symphony/refs/heads/main/finops/symphony-finops.yml
sources:
- https://symphony.com
- https://docs.developers.symphony.com
specification: FinOps Framework
tags:
- Secure Messaging
- Financial Services
- Collaboration
- FinOps
- FOCUS
---
