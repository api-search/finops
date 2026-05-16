---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: traefik-proxy-openapi.yml
  format: yaml
  label: Traefik Proxy
  slug: traefik-proxy
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/traefik/refs/heads/main/openapi/traefik-proxy-openapi.yml
- filename: traefik-proxy-openapi.yml
  format: yaml
  label: Traefik Proxy REST API
  slug: traefik-proxy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/traefik/refs/heads/main/openapi/traefik-proxy-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Open Source + Contracted Subscription
description: FOCUS 1.3 / FinOps Framework 1.0 alignment for Traefik Labs. Traefik Proxy is open-source software with $0 license cost - the only customer spend is the Kubernetes / VM infrastructure that runs it. The four commercial tiers (Hub API Gateway, Hub API Management, AI Gateway add-on, MCP Gateway add-on) are sold via annual contract; pricing is gated and not published. Customer FinOps therefore tracks two cost streams - the Hub subscription invoice (charge_category Purchase, pricing_category Subscription) and the self-hosted infrastructure footprint exported from the cloud provider's own FOCUS data. `reconciled` is false because the commercial subscription unit pricing was not visible at the time of fetch.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Traefik Labs
  PricingCategory: Subscription
  PricingUnit: contract
  ProviderName: Traefik
  PublisherName: Traefik Labs
  ServiceCategory: API Gateway Software
  ServiceName: Traefik Hub
layout: finops
meters:
- aggregation: sum
  description: Annualized Traefik Hub commercial subscription (API Gateway or API Management tier). Quantity and price are contract-defined.
  dimensions:
  - tier
  - environment
  - region
  name: traefik_hub_subscription
  unit: contract
- aggregation: max
  description: Number of Kubernetes clusters connected to the Hub control plane. Multi-cluster management is one axis of the Hub commercial entitlement; operators should track cluster count to anticipate renewal sizing.
  dimensions:
  - environment
  - cloud
  - region
  name: traefik_hub_clusters
  unit: cluster
- aggregation: max
  description: Hub administrative seats - portal admins, GitOps operators, multi-cluster dashboard users. Often a contract input.
  dimensions:
  - role
  name: traefik_hub_seats
  unit: seat
- aggregation: max
  description: Count of Hub-managed API CRDs deployed across all connected clusters. Useful for showback against the API Management tier value.
  dimensions:
  - namespace
  - cluster
  name: traefik_hub_managed_apis
  unit: api
- aggregation: sum
  description: Tokens proxied through the AI Gateway add-on. Even though Traefik does not bill per-token, this meter is required for upstream LLM cost attribution and for sizing the AI Gateway entitlement.
  dimensions:
  - model
  - upstream_provider
  - application
  name: traefik_ai_gateway_throughput
  unit: tokens
- aggregation: sum
  description: Infrastructure cost (compute, network, storage) of running Traefik Proxy or Hub data plane on the customer's own platform. Not billed by Traefik Labs; tracked here for total-cost-of-ownership.
  dimensions:
  - cloud
  - region
  - environment
  - cluster
  name: self_hosted_infra_cost
  unit: varies
name: Traefik Finops
provider_name: Traefik Labs
provider_slug: traefik
publisher_name: Traefik Labs
service_category: API Gateway / API Management Software
slug: traefik-finops
source_filename: traefik-finops.yml
source_heading: FinOps Profile
source_url: https://traefik.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Traefik Labs\nproviderId: traefik\npublisherName: Traefik Labs\nserviceCategory: API Gateway / API Management Software\ncreated: '2026-05-04'\nmodified: '2026-05-15'\nreconciled: false\ntags:\n  - AI Gateway\n  - API Gateway\n  - API Management\n  - FOCUS\n  - FinOps\n  - Kubernetes\n  - MCP Gateway\n  - Open Source\n  - Reverse Proxy\ndescription: >-\n  FOCUS 1.3 / FinOps Framework 1.0 alignment for Traefik Labs. Traefik Proxy\n  is open-source software with $0 license cost - the only customer spend is\n  the Kubernetes / VM infrastructure that runs it. The four commercial tiers\n  (Hub API Gateway, Hub API Management, AI Gateway add-on, MCP Gateway\n\
  \  add-on) are sold via annual contract; pricing is gated and not published.\n  Customer FinOps therefore tracks two cost streams - the Hub subscription\n  invoice (charge_category Purchase, pricing_category Subscription) and the\n  self-hosted infrastructure footprint exported from the cloud provider's\n  own FOCUS data. `reconciled` is false because the commercial subscription\n  unit pricing was not visible at the time of fetch.\nsources:\n  - https://traefik.io/pricing/\n  - https://traefik.io/traefik-hub/\n  - https://traefik.io/solutions/ai-gateway/\nbillingModel:\n  pricingCategory: Open Source + Contracted Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Traefik Hub\n  ServiceCategory: API Gateway Software\n  ProviderName: Traefik\n  PublisherName: Traefik Labs\n  InvoiceIssuerName: Traefik Labs\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory:\
  \ Subscription\n  PricingUnit: contract\nmeters:\n  - name: traefik_hub_subscription\n    description: >-\n      Annualized Traefik Hub commercial subscription (API Gateway or API\n      Management tier). Quantity and price are contract-defined.\n    unit: contract\n    aggregation: sum\n    dimensions: [tier, environment, region]\n  - name: traefik_hub_clusters\n    description: >-\n      Number of Kubernetes clusters connected to the Hub control plane.\n      Multi-cluster management is one axis of the Hub commercial entitlement;\n      operators should track cluster count to anticipate renewal sizing.\n    unit: cluster\n    aggregation: max\n    dimensions: [environment, cloud, region]\n  - name: traefik_hub_seats\n    description: >-\n      Hub administrative seats - portal admins, GitOps operators, multi-cluster\n      dashboard users. Often a contract input.\n    unit: seat\n    aggregation: max\n    dimensions: [role]\n  - name: traefik_hub_managed_apis\n    description: >-\n \
  \     Count of Hub-managed API CRDs deployed across all connected clusters.\n      Useful for showback against the API Management tier value.\n    unit: api\n    aggregation: max\n    dimensions: [namespace, cluster]\n  - name: traefik_ai_gateway_throughput\n    description: >-\n      Tokens proxied through the AI Gateway add-on. Even though Traefik does\n      not bill per-token, this meter is required for upstream LLM cost\n      attribution and for sizing the AI Gateway entitlement.\n    unit: tokens\n    aggregation: sum\n    dimensions: [model, upstream_provider, application]\n  - name: self_hosted_infra_cost\n    description: >-\n      Infrastructure cost (compute, network, storage) of running Traefik\n      Proxy or Hub data plane on the customer's own platform. Not billed by\n      Traefik Labs; tracked here for total-cost-of-ownership.\n    unit: varies\n    aggregation: sum\n    dimensions: [cloud, region, environment, cluster]\nprinciples:\n  - name: Visibility\n    description:\
  \ >-\n      Pull subscription invoices from Traefik Labs for the Hub tier and\n      cross-reference against the cloud-provider FOCUS export covering the\n      Kubernetes nodes running Traefik. The combined view is your total cost\n      of operating Traefik.\n  - name: Allocation\n    description: >-\n      Tag the Kubernetes namespace, node pool, or VM running Traefik with the\n      consuming product / team identifier so the proxy's compute and egress\n      cost can be allocated to the workloads it fronts. For Hub, allocate the\n      subscription cost across managed APIs using the traefik_hub_managed_apis\n      meter.\n  - name: Optimization\n    description: >-\n      Use open-source Traefik Proxy when the commercial features (WAF, OIDC,\n      portal, AI guardrails, MCP governance) are not required. Right-size pod\n      replicas and node pools to actual ingress volume. Enable semantic\n      caching on the AI Gateway - the vendor claims a 40-70% reduction in\n      LLM cost.\n\
  \  - name: Accountability\n    description: >-\n      Designate a platform-engineering owner for the Traefik deployment and\n      the Hub contract. Review Hub cluster count, seats, and subscription\n      tier at each renewal. Tag each ManagedSubscription and APIPlan with\n      its business owner so quota usage is visible to FinOps and product\n      stakeholders.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/traefik/refs/heads/main/finops/traefik-finops.yml
sources:
- https://traefik.io/pricing/
- https://traefik.io/traefik-hub/
- https://traefik.io/solutions/ai-gateway/
specification: FinOps Framework
tags:
- AI Gateway
- API Gateway
- API Management
- FOCUS
- FinOps
- Kubernetes
- MCP Gateway
- Open Source
- Reverse Proxy
---
