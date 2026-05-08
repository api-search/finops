---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: envoy-admin-api-openapi.yml
  format: yaml
  label: Envoy Admin API
  slug: envoy-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envoy/refs/heads/main/openapi/envoy-admin-api-openapi.yml
- filename: envoy-ai-gateway-openapi.yml
  format: yaml
  label: Envoy AI Gateway API
  slug: envoy-ai-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envoy/refs/heads/main/openapi/envoy-ai-gateway-openapi.yml
billing_model:
  billingCurrency: USD (operator's cloud bill, if any)
  billingFrequency: N/A (project is free)
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Open Source (Infra Pass-Through)
description: FOCUS-aligned FinOps view for Envoy. The Envoy software is free (Apache 2.0), so there is no SaaS-style invoice from the project. Cost shows up on the operator's cloud bill — compute, networking, egress, and observability — and on any third-party vendor invoices (Tetrate, Solo.io, cloud-provider managed mesh) chosen for support or managed deployment.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Operator's cloud / vendor (project itself does not invoice)
  ProviderName: Envoy (CNCF)
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Open-Source Networking / Service Mesh
  ServiceName: Envoy
layout: finops
meters:
- aggregation: sum
  description: Compute consumed by Envoy proxies and the Envoy Gateway/AI Gateway control plane on the operator's cloud.
  dimensions:
  - cluster
  - workload
  - region
  name: compute_hours
  unit: instance-hour
- aggregation: sum
  description: Egress traffic mediated by Envoy that the underlying cloud bills the operator.
  dimensions:
  - cluster
  - region
  name: network_egress
  unit: GB
- aggregation: sum
  description: Optional third-party support / managed-service subscription fees.
  dimensions:
  - vendor
  - tier
  name: vendor_support_subscription
  unit: month
name: Envoy Finops
provider_name: Envoy
provider_slug: envoy
publisher_name: Cloud Native Computing Foundation (Envoy is a CNCF graduated project)
service_category: Open-Source Networking / Service Mesh
slug: envoy-finops
source_filename: envoy-finops.yml
source_heading: FinOps Profile
source_url: https://www.envoyproxy.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Envoy\nproviderId: envoy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud Native\n  - Proxy\n  - Service Mesh\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps view for Envoy. The Envoy software is free (Apache 2.0), so there is\n  no SaaS-style invoice from the project. Cost shows up on the operator's cloud bill — compute, networking,\n  egress, and observability — and on any third-party vendor invoices (Tetrate, Solo.io, cloud-provider\n  managed mesh) chosen for support or managed deployment.\nsources:\n  - https://www.envoyproxy.io/\n  - https://github.com/envoyproxy/envoy\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Cloud Native Computing Foundation (Envoy is a CNCF graduated project)\nserviceCategory: Open-Source Networking / Service Mesh\nbillingModel:\n  pricingCategory: Open Source (Infra Pass-Through)\n  billingFrequency: N/A (project is free)\n  billingCurrency: USD (operator's cloud bill, if any)\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Envoy\n  ServiceCategory: Open-Source Networking / Service Mesh\n  ProviderName: Envoy (CNCF)\n  PublisherName: Cloud Native Computing Foundation\n  InvoiceIssuerName: Operator's cloud / vendor (project itself does not invoice)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - workload\n      - region\n    description: Compute consumed by Envoy proxies and the Envoy Gateway/AI Gateway control plane on the\n      operator's cloud.\n  - name: network_egress\n    unit: GB\n    aggregation: sum\n   \
  \ dimensions:\n      - cluster\n      - region\n    description: Egress traffic mediated by Envoy that the underlying cloud bills the operator.\n  - name: vendor_support_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - vendor\n      - tier\n    description: Optional third-party support / managed-service subscription fees.\nprinciples:\n  - name: Visibility\n    description: Pull cloud cost (compute, egress, observability) tagged to the Envoy/Gateway workload\n      from your CSP's billing data; pull vendor invoices for any commercial support you've engaged.\n  - name: Allocation\n    description: Tag each Envoy/Gateway deployment with cluster, namespace, and owning team so cloud-side\n      cost can be attributed back.\n  - name: Optimization\n    description: Right-size Envoy deployments, tune connection pools and concurrency, use sidecarless /\n      ambient patterns where appropriate, and revisit per-region replica counts. There is no project-side\n    \
  \  license cost to optimize.\n  - name: Accountability\n    description: The platform team running Envoy / Envoy Gateway owns the underlying cloud spend and any\n      vendor support subscription; reviews follow the operator's normal cloud FinOps cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/envoy/refs/heads/main/finops/envoy-finops.yml
sources:
- https://www.envoyproxy.io/
- https://github.com/envoyproxy/envoy
specification: FinOps Framework
tags:
- Cloud Native
- Proxy
- Service Mesh
- Open Source
- FinOps
- FOCUS
---
