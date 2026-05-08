---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: coredns-health-openapi.yml
  format: yaml
  label: CoreDNS Health API
  slug: coredns-health-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/openapi/coredns-health-openapi.yml
- filename: coredns-metrics-openapi.yml
  format: yaml
  label: CoreDNS Metrics API
  slug: coredns-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/openapi/coredns-metrics-openapi.yml
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A
  chargeCategories: []
  chargeFrequency: N/A
  pricingCategory: Open Source (No Charge)
description: FinOps shape for CoreDNS - an Apache 2.0 / CNCF Graduated open-source DNS server. There is no upstream invoice. Operator cost is borne by the underlying Kubernetes / cloud platform compute consumed by CoreDNS pods and any DNS-egress charges from upstream resolvers.
focus_columns:
  BillingCurrency: N/A
  ChargeCategory: N/A
  PricingCategory: Free
  ProviderName: CoreDNS Project
  PublisherName: CoreDNS Authors / CNCF
  ServiceCategory: Open Source DNS
  ServiceName: CoreDNS
layout: finops
meters:
- aggregation: sum
  description: CoreDNS pods running in the cluster (compute time consumed, billed by the underlying Kubernetes platform)
  dimensions:
  - cluster
  - namespace
  name: coredns_pods
  unit: pod-hour
- aggregation: sum
  description: DNS queries processed (operational metric exported via the Prometheus plugin; not directly billed by CoreDNS)
  dimensions:
  - cluster
  - zone
  - rcode
  name: dns_queries
  unit: query
- aggregation: sum
  description: Bytes egressed to upstream resolvers via the forward plugin (drives cloud-egress charges)
  dimensions:
  - cluster
  - upstream
  name: upstream_egress
  unit: GB
name: Coredns Finops
provider_name: CoreDNS
provider_slug: coredns
publisher_name: CoreDNS Authors / CNCF
service_category: Open Source DNS
slug: coredns-finops
source_filename: coredns-finops.yml
source_heading: FinOps Profile
source_url: https://coredns.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CoreDNS\nproviderId: coredns\npublisherName: CoreDNS Authors / CNCF\nserviceCategory: Open Source DNS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Apache 2.0\n  - CNCF\n  - DNS\n  - Kubernetes\n  - Networking\n  - Open Source\n  - Service Discovery\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for CoreDNS - an Apache 2.0 / CNCF Graduated open-source DNS server. There\n  is no upstream invoice. Operator cost is borne by the underlying Kubernetes / cloud platform compute\n  consumed by CoreDNS pods and any DNS-egress charges from upstream resolvers.\nsources:\n  - https://coredns.io/\n  - https://github.com/coredns/coredns\n\
  \  - https://www.cncf.io/projects/coredns/\nbillingModel:\n  pricingCategory: Open Source (No Charge)\n  billingFrequency: N/A\n  billingCurrency: N/A\n  chargeCategories: []\n  chargeFrequency: N/A\nfocusColumns:\n  ServiceName: CoreDNS\n  ServiceCategory: Open Source DNS\n  ProviderName: CoreDNS Project\n  PublisherName: CoreDNS Authors / CNCF\n  PricingCategory: Free\n  BillingCurrency: N/A\n  ChargeCategory: N/A\nmeters:\n  - name: coredns_pods\n    description: CoreDNS pods running in the cluster (compute time consumed, billed by the underlying\n      Kubernetes platform)\n    unit: pod-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\n  - name: dns_queries\n    description: DNS queries processed (operational metric exported via the Prometheus plugin; not\n      directly billed by CoreDNS)\n    unit: query\n    aggregation: sum\n    dimensions:\n      - cluster\n      - zone\n      - rcode\n  - name: upstream_egress\n    description: Bytes egressed to\
  \ upstream resolvers via the forward plugin (drives cloud-egress charges)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - cluster\n      - upstream\nprinciples:\n  - name: Visibility\n    description: CoreDNS itself is free; observe cost via the Prometheus /metrics endpoint (request\n      counters, latency histograms) joined to FOCUS-aligned cluster billing.\n  - name: Allocation\n    description: Allocate the cost of CoreDNS pods to platform / cluster-services budgets; the per-tenant\n      \"DNS cost\" is typically rolled into a shared platform charge rather than per-namespace.\n  - name: Optimization\n    description: Tune the cache plugin TTL to reduce upstream lookups; adjust replica count and resource\n      requests to actual QPS; use autopath / minimal to shorten search-domain lookups in Kubernetes;\n      throttle abusive sources with the ratelimit plugin to avoid CPU spikes.\n  - name: Accountability\n    description: Assign a platform-team owner for CoreDNS; alert\
  \ on SERVFAIL rate, cache-miss ratio,\n      and pod CPU saturation; review upgrade cadence aligned with CNCF release schedule.\nnotes: CoreDNS is open-source with no upstream commercial billing. FinOps for CoreDNS is really FinOps\n  for the Kubernetes / cloud platform that hosts it. Reconciled is false because there is no provider\n  rate card or invoice to reconcile against.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/finops/coredns-finops.yml
sources:
- https://coredns.io/
- https://github.com/coredns/coredns
- https://www.cncf.io/projects/coredns/
specification: FinOps Framework
tags:
- Apache 2.0
- CNCF
- DNS
- Kubernetes
- Networking
- Open Source
- Service Discovery
- FinOps
- FOCUS
---
