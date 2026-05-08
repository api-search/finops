---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: index.html
  format: yaml
  label: Dataiku Public API
  slug: dataiku-public-api
  spec_type: OpenAPI
  url: https://doc.dataiku.com/dss/latest/publicapi/rest/index.html
- filename: dataiku-api-node-admin-openapi.yml
  format: yaml
  label: Dataiku API Node Administration API
  slug: dataiku-api-node-administration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dataiku/refs/heads/main/openapi/dataiku-api-node-admin-openapi.yml
- filename: dataiku-govern-api-openapi.yml
  format: yaml
  label: Dataiku Govern API
  slug: dataiku-govern-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dataiku/refs/heads/main/openapi/dataiku-govern-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Dataiku: enterprise SaaS / on-prem subscription billed primarily by user (seat) tier and node count, with optional Govern and LLM Mesh add-ons. Cloud Trial and Free Edition are no-charge. Commercial pricing is quoted by sales and is not public.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Dataiku
  PricingCategory: Subscription
  PricingUnit: seat
  ProviderName: Dataiku
  PublisherName: Dataiku
  ServiceCategory: AI Platform
  ServiceName: Dataiku
  ServiceSubcategory: Data Science Platform
layout: finops
meters:
- aggregation: max
  description: Active named-user seats by edition (Discover, Business, Enterprise). Primary billable line.
  dimensions:
  - edition
  - role
  - tenant
  name: user_seats
  unit: seat
- aggregation: max
  description: DSS design / automation / API nodes provisioned in the deployment.
  dimensions:
  - node_type
  - environment
  name: dss_nodes
  unit: node
- aggregation: sum
  description: Real-time scoring compute consumed by API Node services.
  dimensions:
  - service
  - environment
  name: api_node_compute
  unit: instance-hour
- aggregation: max
  description: Dataiku Govern add-on subscription.
  dimensions:
  - tenant
  name: govern_addon
  unit: month
- aggregation: sum
  description: LLM token consumption routed through advanced LLM Mesh (passthrough to upstream providers; LLM Mesh itself is a feature-add).
  dimensions:
  - model
  - upstream_provider
  name: llm_mesh_tokens
  unit: token
name: Dataiku Finops
provider_name: Dataiku
provider_slug: dataiku
publisher_name: Dataiku
service_category: AI Platform
slug: dataiku-finops
source_filename: dataiku-finops.yml
source_heading: FinOps Profile
source_url: https://www.dataiku.com/product/get-started/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dataiku\nproviderId: dataiku\npublisherName: Dataiku\nserviceCategory: AI Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Analytics\n  - Artificial Intelligence\n  - Data Platform\n  - Machine Learning\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Dataiku: enterprise SaaS / on-prem subscription billed\n  primarily by user (seat) tier and node count, with optional Govern and LLM Mesh add-ons. Cloud\n  Trial and Free Edition are no-charge. Commercial pricing is quoted by sales and is not public.'\nsources:\n  - https://www.dataiku.com/product/get-started/\n  - https://www.dataiku.com\nnotes: No\
  \ public commercial pricing. Meters reflect the typical Dataiku billing shape (seats,\n  nodes, compute) but dollar values are contract-specific.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Dataiku\n  ServiceCategory: AI Platform\n  ServiceSubcategory: Data Science Platform\n  ProviderName: Dataiku\n  PublisherName: Dataiku\n  InvoiceIssuerName: Dataiku\n  PricingCategory: Subscription\n  PricingUnit: seat\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: user_seats\n    description: Active named-user seats by edition (Discover, Business, Enterprise). Primary\n      billable line.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - edition\n      - role\n      - tenant\n  - name: dss_nodes\n    description: DSS design / automation / API nodes provisioned in the deployment.\n    unit: node\n    aggregation:\
  \ max\n    dimensions:\n      - node_type\n      - environment\n  - name: api_node_compute\n    description: Real-time scoring compute consumed by API Node services.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - environment\n  - name: govern_addon\n    description: Dataiku Govern add-on subscription.\n    unit: month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: llm_mesh_tokens\n    description: LLM token consumption routed through advanced LLM Mesh (passthrough to upstream\n      providers; LLM Mesh itself is a feature-add).\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - upstream_provider\nprinciples:\n  - name: Visibility\n    description: Use the DSS administration UI for active-user counts, node inventory, and project\n      activity. Reconcile against the Dataiku invoice quarterly. For LLM Mesh, attribute upstream\n      provider charges back to the calling project.\n  - name: Allocation\n\
  \    description: Use Dataiku project ownership and group membership to attribute seats and node\n      hours back to consuming teams. Tag API Node services with environment and team.\n  - name: Optimization\n    description: Reclaim inactive seats during renewal, right-size design vs automation node\n      counts, schedule API Node downscaling for low-traffic windows, and prefer batch scoring for\n      non-real-time workloads.\n  - name: Accountability\n    description: Designate a Dataiku platform owner who reviews seat utilization, node sprawl, and\n      LLM Mesh spend monthly; align renewals with team-level ROI evidence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.dataiku.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dataiku/refs/heads/main/finops/dataiku-finops.yml
sources:
- https://www.dataiku.com/product/get-started/
- https://www.dataiku.com
specification: FinOps Framework
tags:
- Analytics
- Artificial Intelligence
- Data Platform
- Machine Learning
- FinOps
- FOCUS
---
