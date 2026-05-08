---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: contour-httpproxy-openapi.yml
  format: yaml
  label: Contour HTTPProxy API
  slug: contour-httpproxy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contour/refs/heads/main/openapi/contour-httpproxy-openapi.yml
- filename: contour-gateway-openapi.yml
  format: yaml
  label: Contour Gateway API
  slug: contour-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contour/refs/heads/main/openapi/contour-gateway-openapi.yml
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A
  chargeCategories: []
  chargeFrequency: N/A
  pricingCategory: Open Source (No Charge)
description: FinOps shape for Contour - an Apache 2.0 / CNCF Incubating open-source project. There is no upstream Contour invoice. Operator FinOps cost is borne by the underlying Kubernetes platform (compute, network egress, observability) and any commercial Kubernetes-distribution support contract the operator chooses to layer on.
focus_columns:
  BillingCurrency: N/A
  ChargeCategory: N/A
  PricingCategory: Free
  ProviderName: Project Contour
  PublisherName: Project Contour Authors
  ServiceCategory: Open Source Networking
  ServiceName: Contour
layout: finops
meters:
- aggregation: sum
  description: Contour control-plane pods running in the cluster (compute time consumed, billed by the underlying Kubernetes platform)
  dimensions:
  - cluster
  - namespace
  name: contour_pods
  unit: pod-hour
- aggregation: sum
  description: Envoy data-plane pods running as DaemonSet / Deployment under Contour
  dimensions:
  - cluster
  - node_pool
  name: envoy_pods
  unit: pod-hour
- aggregation: sum
  description: HTTP / TLS ingress traffic processed by Envoy (drives load-balancer and egress charges on the underlying cloud)
  dimensions:
  - cluster
  - vhost
  - direction
  name: ingress_traffic
  unit: GB
name: Contour Finops
provider_name: Contour
provider_slug: contour
publisher_name: Project Contour Authors
service_category: Open Source Networking
slug: contour-finops
source_filename: contour-finops.yml
source_heading: FinOps Profile
source_url: https://projectcontour.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Contour\nproviderId: contour\npublisherName: Project Contour Authors\nserviceCategory: Open Source Networking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Envoy\n  - Ingress Controller\n  - Kubernetes\n  - Networking\n  - Open Source\n  - Proxy\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Contour - an Apache 2.0 / CNCF Incubating open-source project. There\n  is no upstream Contour invoice. Operator FinOps cost is borne by the underlying Kubernetes platform\n  (compute, network egress, observability) and any commercial Kubernetes-distribution support contract\n  the operator chooses to layer on.\nsources:\n\
  \  - https://projectcontour.io/\n  - https://github.com/projectcontour/contour\n  - https://www.cncf.io/projects/contour/\nbillingModel:\n  pricingCategory: Open Source (No Charge)\n  billingFrequency: N/A\n  billingCurrency: N/A\n  chargeCategories: []\n  chargeFrequency: N/A\nfocusColumns:\n  ServiceName: Contour\n  ServiceCategory: Open Source Networking\n  ProviderName: Project Contour\n  PublisherName: Project Contour Authors\n  PricingCategory: Free\n  BillingCurrency: N/A\n  ChargeCategory: N/A\nmeters:\n  - name: contour_pods\n    description: Contour control-plane pods running in the cluster (compute time consumed, billed by\n      the underlying Kubernetes platform)\n    unit: pod-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\n  - name: envoy_pods\n    description: Envoy data-plane pods running as DaemonSet / Deployment under Contour\n    unit: pod-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - node_pool\n  - name: ingress_traffic\n\
  \    description: HTTP / TLS ingress traffic processed by Envoy (drives load-balancer and egress charges\n      on the underlying cloud)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - cluster\n      - vhost\n      - direction\nprinciples:\n  - name: Visibility\n    description: Contour itself is free; observe cost through the underlying Kubernetes / cloud provider\n      using Envoy's Prometheus metrics (envoy_cluster_upstream_rq, response sizes) joined to FOCUS-\n      aligned cluster billing.\n  - name: Allocation\n    description: Allocate the cost of Contour pods, Envoy pods, and load-balancer / egress traffic\n      to teams via Kubernetes namespace and HTTPProxy ownership labels. Treat each HTTPProxy as a chargeback\n      unit.\n  - name: Optimization\n    description: Right-size Envoy DaemonSet vs Deployment topology; enable HTTP/2 and connection pooling;\n      use Envoy local rate limiting to curb runaway traffic before it triggers egress / load-balancer\n    \
  \  cost; consolidate low-traffic vhosts onto shared Contour deployments.\n  - name: Accountability\n    description: Assign each HTTPProxy to a team owner via Kubernetes labels; review traffic spikes\n      and 5xx rates against budgeted egress; treat operational toil on Contour upgrades as a real cost\n      input.\nnotes: Contour is open-source with no upstream commercial billing. FinOps for Contour is really FinOps\n  for the Kubernetes platform that hosts it - compute, load balancers, and egress. Reconciled is false\n  because there is no provider-issued invoice or rate card to reconcile against.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/contour/refs/heads/main/finops/contour-finops.yml
sources:
- https://projectcontour.io/
- https://github.com/projectcontour/contour
- https://www.cncf.io/projects/contour/
specification: FinOps Framework
tags:
- Envoy
- Ingress Controller
- Kubernetes
- Networking
- Open Source
- Proxy
- FinOps
- FOCUS
---
