---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: traefik-api-openapi.yml
  format: yaml
  label: Traefik REST API
  slug: traefik-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/traefik/refs/heads/main/openapi/traefik-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Open Source + Contracted Subscription
description: 'FOCUS-aligned FinOps for Traefik Labs: an open-source Application Proxy with $0 license cost, plus two commercial tiers (API Gateway, API Management) where pricing is contracted via sales rather than published. Costs at customers consist of (a) infrastructure to run Traefik Proxy and (b) any commercial Traefik Hub subscription, neither of which Traefik bills metered per-request.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Traefik Labs
  PricingCategory: Subscription
  PricingUnit: contract
  ProviderName: Traefik
  PublisherName: Traefik Labs
  ServiceCategory: API Gateway Software
  ServiceName: Traefik
layout: finops
meters:
- aggregation: sum
  description: Annualized Traefik Hub commercial subscription (API Gateway or API Management tier). Quantity and price are contract-defined.
  dimensions:
  - tier
  - environment
  name: traefik_hub_subscription
  unit: contract
- aggregation: sum
  description: Infrastructure cost (compute, network, storage) of running Traefik Proxy on the customer's own platform. Not billed by Traefik Labs; tracked here for total-cost-of-ownership.
  dimensions:
  - cloud
  - region
  - environment
  name: self_hosted_infra_cost
  unit: varies
name: Traefik Finops
provider_name: Traefik
provider_slug: traefik
publisher_name: Traefik Labs
service_category: API Gateway / API Management Software
slug: traefik-finops
source_filename: traefik-finops.yml
source_heading: FinOps Profile
source_url: https://traefik.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Traefik\nproviderId: traefik\npublisherName: Traefik Labs\nserviceCategory: API Gateway / API Management Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - API Gateway\n  - Kubernetes\n  - Reverse Proxy\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Traefik Labs: an open-source Application Proxy with $0 license\n  cost, plus two commercial tiers (API Gateway, API Management) where pricing is contracted via sales\n  rather than published. Costs at customers consist of (a) infrastructure to run Traefik Proxy and (b)\n  any commercial Traefik Hub subscription, neither of which Traefik\
  \ bills metered per-request.'\nsources:\n  - https://traefik.io/pricing/\n  - https://traefik.io/traefik-hub/\nbillingModel:\n  pricingCategory: Open Source + Contracted Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Traefik\n  ServiceCategory: API Gateway Software\n  ProviderName: Traefik\n  PublisherName: Traefik Labs\n  InvoiceIssuerName: Traefik Labs\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\n  PricingUnit: contract\nmeters:\n  - name: traefik_hub_subscription\n    description: Annualized Traefik Hub commercial subscription (API Gateway or API Management tier).\n      Quantity and price are contract-defined.\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - tier\n      - environment\n  - name: self_hosted_infra_cost\n    description: Infrastructure cost (compute, network, storage) of running Traefik Proxy\
  \ on the customer's\n      own platform. Not billed by Traefik Labs; tracked here for total-cost-of-ownership.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - cloud\n      - region\n      - environment\nprinciples:\n  - name: Visibility\n    description: Pull subscription invoices from Traefik Labs for the Hub tier; pull infrastructure cost\n      from your cloud provider's FOCUS export to see total cost of running Traefik.\n  - name: Allocation\n    description: Tag the Kubernetes namespace, cluster, or VM running Traefik Proxy with the consuming\n      product/team so the proxy's compute/egress is allocated alongside the apps it fronts.\n  - name: Optimization\n    description: Use the open-source Application Proxy where the commercial features (WAF, OIDC, mocking)\n      are not required; right-size pod replicas and node pools so the proxy scales to actual ingress volume.\n  - name: Accountability\n    description: Designate a platform-team owner for the Traefik deployment\
  \ and the Hub contract; review\n      Hub seats/environments at each renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/traefik/refs/heads/main/finops/traefik-finops.yml
sources:
- https://traefik.io/pricing/
- https://traefik.io/traefik-hub/
specification: FinOps Framework
tags:
- API Gateway
- Kubernetes
- Reverse Proxy
- Open Source
- FinOps
- FOCUS
---
