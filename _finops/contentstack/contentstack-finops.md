---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: contentstack-content-delivery-api-openapi.yml
  format: yaml
  label: Contentstack Content Delivery API
  slug: content-delivery-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-content-delivery-api-openapi.yml
- filename: contentstack-content-management-api-openapi.yml
  format: yaml
  label: Contentstack Content Management API
  slug: content-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-content-management-api-openapi.yml
- filename: contentstack-personalize-management-api-openapi.yml
  format: yaml
  label: Contentstack Personalize Management API
  slug: personalize-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-personalize-management-api-openapi.yml
- filename: contentstack-personalize-edge-api-openapi.yml
  format: yaml
  label: Contentstack Personalize Edge API
  slug: personalize-edge-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-personalize-edge-api-openapi.yml
- filename: contentstack-automate-management-api-openapi.yml
  format: yaml
  label: Contentstack Automate Management API
  slug: automate-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-automate-management-api-openapi.yml
- filename: contentstack-analytics-api-openapi.yml
  format: yaml
  label: Contentstack Analytics API
  slug: analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-analytics-api-openapi.yml
- filename: contentstack-scim-api-openapi.yml
  format: yaml
  label: Contentstack SCIM API
  slug: scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-scim-api-openapi.yml
- filename: contentstack-brand-kit-management-api-openapi.yml
  format: yaml
  label: Contentstack Brand Kit Management API
  slug: brand-kit-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-brand-kit-management-api-openapi.yml
- filename: contentstack-knowledge-vault-api-openapi.yml
  format: yaml
  label: Contentstack Knowledge Vault API
  slug: knowledge-vault-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-knowledge-vault-api-openapi.yml
- filename: contentstack-generative-ai-api-openapi.yml
  format: yaml
  label: Contentstack Generative AI API
  slug: generative-ai-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-generative-ai-api-openapi.yml
- filename: contentstack-launch-api-openapi.yml
  format: yaml
  label: Contentstack Launch API
  slug: launch-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-launch-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Subscription
description: 'FOCUS-aligned FinOps for Contentstack: enterprise SaaS subscription where the headless CMS, personalization, real-time CDP, and agentic capabilities are bundled into a Contentstack AXP plan. Contentstack does not publish per-call API pricing; spend is anchored to the annual contract plus per-stack / per-user / per-environment expansion charges negotiated with sales.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Contentstack Inc.
  ProviderName: Contentstack
  PublisherName: Contentstack Inc.
  ServiceCategory: Headless CMS / Digital Experience Platform
  ServiceName: Contentstack
layout: finops
meters:
- aggregation: max
  description: Annual Contentstack subscription (Business / Enterprise / AXP)
  dimensions:
  - tier
  - organization
  name: subscription
  unit: month
- aggregation: max
  description: Number of provisioned content stacks against the contract
  dimensions:
  - organization
  - environment
  name: stacks
  unit: stack
- aggregation: max
  description: Active CMS user seats
  dimensions:
  - organization
  - role
  name: users
  unit: seat
- aggregation: sum
  description: Content Management API request volume (10 read/sec + 10 write/sec default ceiling per organization)
  dimensions:
  - organization
  - stack
  - operation
  name: cm_api_requests
  unit: request
- aggregation: sum
  description: Content Delivery API request volume served to client applications
  dimensions:
  - organization
  - stack
  - environment
  name: cd_api_requests
  unit: request
- aggregation: sum
  description: Egress bandwidth from the Content Delivery API and asset CDN
  dimensions:
  - organization
  - region
  name: bandwidth
  unit: GB
name: Contentstack Finops
provider_name: contentstack
provider_slug: contentstack
publisher_name: Contentstack Inc.
service_category: Headless CMS / Digital Experience Platform
slug: contentstack-finops
source_filename: contentstack-finops.yml
source_heading: FinOps Profile
source_url: https://www.contentstack.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Contentstack\nproviderId: contentstack\npublisherName: Contentstack Inc.\nserviceCategory: Headless CMS / Digital Experience Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Headless CMS\n  - Content Management\n  - Personalization\n  - AI\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Contentstack: enterprise SaaS subscription where the headless\n  CMS, personalization, real-time CDP, and agentic capabilities are bundled into a Contentstack AXP plan.\n  Contentstack does not publish per-call API pricing; spend is anchored to the annual contract plus per-stack\n  / per-user / per-environment expansion\
  \ charges negotiated with sales.'\nnotes: Per-tier pricing is sales-led and not publicly published. Meters in this artifact reflect the\n  consumption signals consumers should track for chargeback even though Contentstack bills as a bundled\n  subscription.\nsources:\n  - https://www.contentstack.com/pricing\n  - https://www.contentstack.com/docs/developers/apis/content-management-api\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Contentstack\n  ServiceCategory: Headless CMS / Digital Experience Platform\n  ProviderName: Contentstack\n  PublisherName: Contentstack Inc.\n  InvoiceIssuerName: Contentstack Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription\n    description: Annual Contentstack subscription (Business / Enterprise / AXP)\n    unit: month\n    aggregation: max\n  \
  \  dimensions:\n      - tier\n      - organization\n  - name: stacks\n    description: Number of provisioned content stacks against the contract\n    unit: stack\n    aggregation: max\n    dimensions:\n      - organization\n      - environment\n  - name: users\n    description: Active CMS user seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - organization\n      - role\n  - name: cm_api_requests\n    description: Content Management API request volume (10 read/sec + 10 write/sec default ceiling per\n      organization)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - organization\n      - stack\n      - operation\n  - name: cd_api_requests\n    description: Content Delivery API request volume served to client applications\n    unit: request\n    aggregation: sum\n    dimensions:\n      - organization\n      - stack\n      - environment\n  - name: bandwidth\n    description: Egress bandwidth from the Content Delivery API and asset CDN\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - organization\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the Contentstack Audit Logs and per-stack usage views; correlate Content Management\n      API call volume against the documented per-organization rate ceiling to detect when the plan needs\n      to be raised.\n  - name: Allocation\n    description: Allocate the bundled subscription across business units by stack ownership and active\n      user-seat counts; tag API tokens by consuming application for downstream chargeback.\n  - name: Optimization\n    description: Cache Content Delivery API responses at the CDN / edge; consolidate stacks where business-unit\n      isolation isn't required; batch Content Management writes via bulk endpoints (mind the separate\n      1 req/s bulk ceiling); right-size environment count.\n  - name: Accountability\n    description: Digital-experience / marketing-engineering teams typically own the Contentstack subscription;\n\
  \      individual product teams accountable for stack-level usage and per-application API churn.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/finops/contentstack-finops.yml
sources:
- https://www.contentstack.com/pricing
- https://www.contentstack.com/docs/developers/apis/content-management-api
specification: FinOps Framework
tags:
- Headless CMS
- Content Management
- Personalization
- AI
- FinOps
- FOCUS
---
