---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: policy-api.yml
  format: yaml
  label: Open Policy Agent Policy API
  slug: open-policy-agent-policy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/policy-api.yml
- filename: data-api.yml
  format: yaml
  label: Open Policy Agent Data API
  slug: open-policy-agent-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/data-api.yml
- filename: query-api.yml
  format: yaml
  label: Open Policy Agent Query API
  slug: open-policy-agent-query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/query-api.yml
- filename: compile-api.yml
  format: yaml
  label: Open Policy Agent Compile API
  slug: open-policy-agent-compile-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/compile-api.yml
- filename: health-api.yml
  format: yaml
  label: Open Policy Agent Health API
  slug: open-policy-agent-health-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/health-api.yml
- filename: config-api.yml
  format: yaml
  label: Open Policy Agent Config API
  slug: open-policy-agent-config-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/config-api.yml
- filename: status-api.yml
  format: yaml
  label: Open Policy Agent Status API
  slug: open-policy-agent-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/status-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Self-Hosted Open Source
description: 'FOCUS-aligned FinOps for self-hosted Open Policy Agent: there is no software licensing line item; cost is dominated by underlying compute, memory, and decision-log storage in the operator''s own infrastructure.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: N/A (open source)
  ProviderName: Open Policy Agent
  PublisherName: Open Policy Agent (CNCF)
  ServiceCategory: Identity / Authorization
  ServiceName: Open Policy Agent
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - environment
  name: compute_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - cluster
  - sink
  name: decision_log_volume
  unit: GB
- aggregation: sum
  dimensions:
  - policy
  - cluster
  name: policy_evaluations
  unit: request
name: Open Policy Agent Finops
provider_name: Open Policy Agent
provider_slug: open-policy-agent
publisher_name: Open Policy Agent (CNCF)
service_category: Identity / Authorization
slug: open-policy-agent-finops
source_filename: open-policy-agent-finops.yml
source_heading: FinOps Profile
source_url: https://www.openpolicyagent.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Open Policy Agent\nproviderId: open-policy-agent\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Policies\n  - Standards\n  - FinOps\n  - FOCUS\n  - Open Source\nnotes: OPA is open-source software with no licensing fees. FinOps shape here describes the cost of running\n  OPA (compute, observability) rather than a vendor invoice. Commercial alternatives (Styra DAS) would\n  produce a vendor-billed surface modeled separately.\ndescription: 'FOCUS-aligned FinOps for self-hosted Open Policy Agent: there is no software licensing line\n  item; cost is dominated by underlying compute, memory, and decision-log storage in the operator''s own\n  infrastructure.'\nsources:\n  - https://www.openpolicyagent.org/\n  - https://github.com/open-policy-agent/opa\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Open Policy Agent (CNCF)\nserviceCategory: Identity / Authorization\nbillingModel:\n  pricingCategory: Self-Hosted Open Source\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Open Policy Agent\n  ServiceCategory: Identity / Authorization\n  ProviderName: Open Policy Agent\n  PublisherName: Open Policy Agent (CNCF)\n  InvoiceIssuerName: N/A (open source)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - environment\n  - name: decision_log_volume\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - cluster\n      - sink\n  - name: policy_evaluations\n    unit: request\n    aggregation: sum\n    dimensions:\n      - policy\n      - cluster\nprinciples:\n  - name: Visibility\n    description: Capture\
  \ decision logs and Prometheus metrics from each OPA instance to attribute query\n      load and latency by policy and cluster.\n  - name: Allocation\n    description: Tag the underlying compute (Kubernetes namespaces, nodes) running OPA so that infrastructure\n      cost can be attributed to the policies it serves.\n  - name: Optimization\n    description: Right-size OPA replicas, enable bundle caching, and consolidate policies to reduce CPU\n      and decision-log egress.\n  - name: Accountability\n    description: Platform / security teams typically own the OPA deployment; ensure decision-log storage\n      and OPA compute appear in their cost reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/finops/open-policy-agent-finops.yml
sources:
- https://www.openpolicyagent.org/
- https://github.com/open-policy-agent/opa
specification: FinOps Framework
tags:
- Policies
- Standards
- FinOps
- FOCUS
- Open Source
---
