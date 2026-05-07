---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: at-t-developer-hub-network-insights-api.yaml
  format: yaml
  label: AT&T Network Insights API
  slug: att-network-insights-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/openapi/at-t-developer-hub-network-insights-api.yaml
- filename: at-t-developer-hub-mobility-threat-anomaly-detection-api.yaml
  format: yaml
  label: AT&T Mobility Threat and Anomaly Detection API
  slug: att-mobility-threat-anomaly-detection-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/openapi/at-t-developer-hub-mobility-threat-anomaly-detection-api.yaml
- filename: at-t-developer-hub-sim-swap-api.yaml
  format: yaml
  label: AT&T SIM Swap API
  slug: att-sim-swap-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/openapi/at-t-developer-hub-sim-swap-api.yaml
- filename: at-t-developer-hub-device-status-api.yaml
  format: yaml
  label: AT&T Device Status API
  slug: att-device-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/openapi/at-t-developer-hub-device-status-api.yaml
- filename: at-t-developer-hub-quality-on-demand-api.yaml
  format: yaml
  label: AT&T Quality on Demand API
  slug: att-quality-on-demand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/openapi/at-t-developer-hub-quality-on-demand-api.yaml
- filename: at-t-developer-hub-number-verification-api.yaml
  format: yaml
  label: AT&T Number Verification API
  slug: att-number-verification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/openapi/at-t-developer-hub-number-verification-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (anticipated)
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Pay-As-You-Go (anticipated)
description: FOCUS-aligned FinOps shape for AT&T Network APIs (CAMARA). The program is invite-only and pre-GA; public pricing is not available. Consumers should anticipate per-call and/or volume-tier commercials common across CAMARA carriers and instrument meters in advance.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AT&T Services, Inc.
  PricingCategory: Pay-As-You-Go
  ProviderName: AT&T
  PublisherName: AT&T Services, Inc.
  ServiceCategory: Telecommunications
  ServiceName: AT&T Network APIs
  ServiceSubcategory: Network APIs (CAMARA)
layout: finops
meters:
- aggregation: sum
  description: Count of CAMARA API requests (Device Status, SIM Swap, Number Verification, etc.)
  dimensions:
  - api
  - country
  - partner
  name: api_calls
  unit: request
- aggregation: sum
  description: Successful network verifications (SIM swap, number verify) — likely a billable success-only line
  dimensions:
  - api
  - outcome
  name: verifications
  unit: verification
- aggregation: sum
  description: Quality-on-Demand session count and duration
  dimensions:
  - profile
  name: qod_sessions
  unit: session
- aggregation: sum
  description: Quality-on-Demand active duration
  dimensions:
  - profile
  name: qod_session_duration
  unit: minute
name: At T Developer Hub Finops
provider_name: AT&T Developer Hub
provider_slug: at-t-developer-hub
publisher_name: AT&T Services, Inc.
service_category: Telecommunications / Network APIs
slug: at-t-developer-hub-finops
source_filename: at-t-developer-hub-finops.yml
source_heading: FinOps Profile
source_url: https://developer.att.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AT&T Developer Hub\nproviderId: at-t-developer-hub\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - 5G\n  - Network APIs\n  - CAMARA\n  - Telecommunications\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for AT&T Network APIs (CAMARA). The program is invite-only\n  and pre-GA; public pricing is not available. Consumers should anticipate per-call and/or volume-tier\n  commercials common across CAMARA carriers and instrument meters in advance.\nsources:\n  - https://developer.att.com/\n  - https://camaraproject.org/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: Pre-GA / invite-only; commercials TBD. Meters below describe the expected billable axes for\n  CAMARA-style network APIs so consumers can build instrumentation before contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl:\
  \ https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AT&T Services, Inc.\nserviceCategory: Telecommunications / Network APIs\nbillingModel:\n  pricingCategory: Pay-As-You-Go (anticipated)\n  billingFrequency: Monthly (anticipated)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: AT&T Network APIs\n  ServiceCategory: Telecommunications\n  ServiceSubcategory: Network APIs (CAMARA)\n  ProviderName: AT&T\n  PublisherName: AT&T Services, Inc.\n  InvoiceIssuerName: AT&T Services, Inc.\n  BillingCurrency: USD\n  PricingCategory: Pay-As-You-Go\nmeters:\n  - name: api_calls\n    description: Count of CAMARA API requests (Device Status, SIM Swap, Number Verification, etc.)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - country\n      - partner\n  - name: verifications\n    description:\
  \ Successful network verifications (SIM swap, number verify) — likely a billable\n      success-only line\n    unit: verification\n    aggregation: sum\n    dimensions:\n      - api\n      - outcome\n  - name: qod_sessions\n    description: Quality-on-Demand session count and duration\n    unit: session\n    aggregation: sum\n    dimensions:\n      - profile\n  - name: qod_session_duration\n    description: Quality-on-Demand active duration\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - profile\nprinciples:\n  - name: Visibility\n    description: Once GA, expect AT&T to expose a developer console with usage dashboards; pre-GA,\n      maintain client-side counters per CAMARA API and per outcome.\n  - name: Allocation\n    description: Tag every CAMARA call with consuming product / fraud-prevention surface in your own\n      app telemetry to support showback before AT&T's invoice arrives.\n  - name: Optimization\n    description: For SIM-swap and number-verify, batch user\
  \ enrollment events; for QoD, tear down\n      sessions promptly. Avoid speculative pre-flight calls during low-risk transactions.\n  - name: Accountability\n    description: Fraud / risk and identity engineering teams typically own CAMARA spend; pair with\n      finance on per-verification ROI vs fraud loss avoided.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/finops/at-t-developer-hub-finops.yml
sources:
- https://developer.att.com/
- https://camaraproject.org/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- 5G
- Network APIs
- CAMARA
- Telecommunications
- FinOps
- FOCUS
---
