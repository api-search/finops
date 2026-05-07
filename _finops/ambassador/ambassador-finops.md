---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ambassador-openapi.yml
  format: yaml
  label: Ambassador Edge Stack API Gateway
  slug: edge-stack-api-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ambassador/refs/heads/main/openapi/ambassador-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Ambassador Edge Stack (now under Gravitee): flat per-month subscription scaled by production-gateway count and event-broker count, with unlimited users and API calls. Open-source Emissary-Ingress and Telepresence are free; cost arises from the underlying Kubernetes cluster (compute, network, storage).'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Gravitee SAS
  ProviderName: Gravitee
  PublisherName: Gravitee SAS
  ServiceCategory: Developer Tools
  ServiceName: Ambassador Edge Stack
  ServiceSubcategory: API Gateway
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  name: subscription_months
  unit: month
- aggregation: max
  dimensions:
  - tier
  - cluster
  name: production_gateways
  unit: gateway
- aggregation: max
  dimensions:
  - tier
  - cluster
  name: event_brokers
  unit: broker
- aggregation: sum
  dimensions:
  - cluster
  - environment
  name: cluster_compute_underlying
  unit: vCPU-hour
name: Ambassador Finops
provider_name: Ambassador
provider_slug: ambassador
publisher_name: Gravitee SAS (formerly Ambassador Labs / Datawire)
service_category: API Management / Gateway
slug: ambassador-finops
source_filename: ambassador-finops.yml
source_heading: FinOps Profile
source_url: https://www.gravitee.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ambassador\nproviderId: ambassador\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Gateway\n  - Kubernetes\n  - Ambassador\n  - Gravitee\ndescription: 'FOCUS-aligned FinOps for Ambassador Edge Stack (now under Gravitee): flat per-month subscription\n  scaled by production-gateway count and event-broker count, with unlimited users and API calls. Open-source\n  Emissary-Ingress and Telepresence are free; cost arises from the underlying Kubernetes cluster (compute,\n  network, storage).'\nsources:\n  - https://www.gravitee.io/pricing\n  - https://www.getambassador.io\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Gravitee SAS\
  \ (formerly Ambassador Labs / Datawire)\nserviceCategory: API Management / Gateway\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Ambassador Edge Stack\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: API Gateway\n  ProviderName: Gravitee\n  PublisherName: Gravitee SAS\n  InvoiceIssuerName: Gravitee SAS\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_months\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: production_gateways\n    unit: gateway\n    aggregation: max\n    dimensions:\n      - tier\n      - cluster\n  - name: event_brokers\n    unit: broker\n    aggregation: max\n    dimensions:\n      - tier\n      - cluster\n  - name: cluster_compute_underlying\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - environment\n\
  principles:\n  - name: Visibility\n    description: Track Edge Stack subscription as a flat SaaS line; observe gateway resource usage via\n      Kubernetes metrics (Prometheus, OpenTelemetry) and the underlying cloud provider's CUR for cluster\n      cost attribution.\n  - name: Allocation\n    description: Tag the gateway namespace and event-broker deployments with team, environment, and product;\n      allocate flat subscription cost via gateway-count weighting.\n  - name: Optimization\n    description: Consolidate routes onto fewer production gateways to stay within the tier's gateway quota;\n      use Emissary-Ingress (OSS) for non-production / dev clusters; right-size gateway pods (HPA, requests/limits).\n  - name: Accountability\n    description: Owner of the platform team owns the subscription; chargeback gateway and cluster cost\n      to consuming product teams via namespace tagging.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n\
  \  - name: Gravitee (Ambassador Labs)\n    email: support@gravitee.io\n    url: https://www.gravitee.io\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ambassador/refs/heads/main/finops/ambassador-finops.yml
sources:
- https://www.gravitee.io/pricing
- https://www.getambassador.io
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Gateway
- Kubernetes
- Ambassador
- Gravitee
---
