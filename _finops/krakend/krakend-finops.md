---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: krakend-service-api-openapi.yml
  format: yaml
  label: KrakenD Service API
  slug: krakend-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/krakend/refs/heads/main/openapi/krakend-service-api-openapi.yml
billing_model:
  billingCurrency: EUR/USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Flat Subscription (Self-Hosted)
description: 'FOCUS-aligned FinOps for KrakenD: shipped software with a flat Enterprise license fee that is explicitly not metered by API count or throughput, plus zero-cost Community Edition. The largest FinOps lever is operator infrastructure (compute, network, observability) — not vendor charges.'
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: KrakenD SL
  ProviderName: KrakenD
  PublisherName: KrakenD SL
  ServiceCategory: Developer Tools
  ServiceName: KrakenD
  ServiceSubcategory: API Gateway
layout: finops
meters:
- aggregation: max
  dimensions:
  - environment
  name: enterprise_license
  unit: license-year
- aggregation: max
  dimensions:
  - environment
  - region
  name: gateway_instances
  notes: Operator-tracked, not billed by KrakenD; predict cost by sizing infra.
  unit: instance
- aggregation: sum
  dimensions:
  - environment
  - endpoint
  name: requests_processed
  notes: Tracked operationally, not billed by KrakenD.
  unit: request
- aggregation: sum
  name: support_hours
  notes: Engineering hours for custom plugins / architecture reviews under Enterprise contract.
  unit: hour
name: Krakend Finops
provider_name: KrakenD
provider_slug: krakend
publisher_name: KrakenD SL
service_category: API Management
slug: krakend-finops
source_filename: krakend-finops.yml
source_heading: FinOps Profile
source_url: https://www.krakend.io/enterprise/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: KrakenD\nproviderId: krakend\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Gateway\n  - Open Source\n  - API Management\ndescription: 'FOCUS-aligned FinOps for KrakenD: shipped software with a flat Enterprise license fee that\n  is explicitly not metered by API count or throughput, plus zero-cost Community Edition. The largest\n  FinOps lever is operator infrastructure (compute, network, observability) — not vendor charges.'\nsources:\n  - https://www.krakend.io/enterprise/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: KrakenD SL\nserviceCategory: API Management\nbillingModel:\n  pricingCategory: Flat Subscription (Self-Hosted)\n\
  \  billingFrequency: Annual\n  billingCurrency: EUR/USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: KrakenD\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: API Gateway\n  ProviderName: KrakenD\n  PublisherName: KrakenD SL\n  InvoiceIssuerName: KrakenD SL\n  BillingCurrency: EUR\nmeters:\n  - name: enterprise_license\n    unit: license-year\n    aggregation: max\n    dimensions:\n      - environment\n  - name: gateway_instances\n    unit: instance\n    aggregation: max\n    dimensions:\n      - environment\n      - region\n    notes: Operator-tracked, not billed by KrakenD; predict cost by sizing infra.\n  - name: requests_processed\n    unit: request\n    aggregation: sum\n    dimensions:\n      - environment\n      - endpoint\n    notes: Tracked operationally, not billed by KrakenD.\n  - name: support_hours\n    unit: hour\n    aggregation: sum\n    notes: Engineering hours for custom plugins / architecture reviews under Enterprise\
  \ contract.\nprinciples:\n  - name: Visibility\n    description: KrakenD does not bill on usage, but operators should still expose request count, latency,\n      and rejection metrics through KrakenD's telemetry exporters (OpenTelemetry, Prometheus) to manage\n      the underlying compute spend.\n  - name: Allocation\n    description: Tag KrakenD instances and endpoints by team / product so the underlying compute (Kubernetes\n      pods, VMs) can be charged back; the license itself is centrally owned.\n  - name: Optimization\n    description: Use KrakenD's stateless scaling and aggressive caching/aggregation to reduce backend\n      and egress cost; the gateway license is fixed, so all marginal optimization happens at the infra\n      layer.\n  - name: Accountability\n    description: Platform team owns the Enterprise contract renewal; product teams own backend cost and\n      are accountable for sizing their own gateway capacity through their infra budget.\nmaintainers:\n  - FN: Kin Lane\n\
  \    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/krakend/refs/heads/main/finops/krakend-finops.yml
sources:
- https://www.krakend.io/enterprise/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Gateway
- Open Source
- API Management
---
