---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: intel-trust-authority-api-openapi.yml
  format: yaml
  label: Intel Trust Authority API
  slug: trust-authority-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/intel/refs/heads/main/openapi/intel-trust-authority-api-openapi.yml
- filename: intel-oneapi-openapi.yml
  format: yaml
  label: Intel oneAPI
  slug: oneapi
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/intel/refs/heads/main/openapi/intel-oneapi-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Free + Optional Support
description: FOCUS-aligned FinOps shape for Intel developer APIs. Both Intel Trust Authority and Intel oneAPI are free at the API / toolkit level; the only invoiced lines are optional support subscriptions (Intel Trust Authority paid support, Intel Priority Support for oneAPI). FinOps practice for Intel APIs therefore focuses on operational telemetry (attestation request volume, rate-limit headroom) and on support-renewal accountability rather than per-call cost accounting.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Intel Corporation
  PricingCategory: Free
  PricingUnit: not-applicable
  ProviderName: Intel
  PublisherName: Intel Corporation
  ServiceCategory: Confidential Computing + Developer Tools
  ServiceName: Intel Developer APIs
layout: finops
meters:
- aggregation: sum
  description: Trust Authority attestation requests issued by the customer
  dimensions:
  - region
  - tee_type
  - workload
  name: attestation_requests
  unit: request
- aggregation: max
  description: Active paid support subscriptions (Trust Authority and oneAPI Priority Support)
  dimensions:
  - product
  - tier
  name: support_subscriptions
  unit: subscription-month
name: Intel Finops
provider_name: intel
provider_slug: intel
publisher_name: Intel Corporation
service_category: Confidential Computing + Developer Tools
slug: intel-finops
source_filename: intel-finops.yml
source_heading: FinOps Profile
source_url: https://docs.trustauthority.intel.com/main/articles/restapi-intro.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Intel\nproviderId: intel\npublisherName: Intel Corporation\nserviceCategory: Confidential Computing + Developer Tools\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Confidential Computing\n  - Attestation\n  - oneAPI\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Intel developer APIs. Both Intel Trust Authority and Intel\n  oneAPI are free at the API / toolkit level; the only invoiced lines are optional support subscriptions\n  (Intel Trust Authority paid support, Intel Priority Support for oneAPI). FinOps practice for Intel\n  APIs therefore focuses on operational telemetry (attestation request\
  \ volume, rate-limit headroom)\n  and on support-renewal accountability rather than per-call cost accounting.\nnotes: No usage-based invoice for the API itself. The 'cost' to track is operational - request volume,\n  region selection, and support entitlement utilization. Reconcile against the customer's Intel Priority\n  Support and Trust Authority support contracts.\nsources:\n  - https://docs.trustauthority.intel.com/main/articles/restapi-intro.html\n  - https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html\nprinciples:\n  - name: Visibility\n    description: Track Intel Trust Authority attestation request volume per workload and per region;\n      surface oneAPI Priority Support ticket usage in Intel's support portal.\n  - name: Allocation\n    description: Tag attestation requests by workload / cluster / cost-center so request volume can be\n      attributed; map oneAPI Priority Support entitlement to product teams.\n  - name: Optimization\n    description: Cache\
  \ attestation tokens for their full validity; co-locate workloads with the closest\n      Trust Authority region (US or EU) to reduce latency; align oneAPI support tier to active toolkit\n      usage at renewal.\n  - name: Accountability\n    description: Designate a confidential-computing owner for Trust Authority and a developer-experience\n      owner for oneAPI; review attestation-volume growth and support-ticket spend annually.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Free\
  \ + Optional Support\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Intel Developer APIs\n  ServiceCategory: Confidential Computing + Developer Tools\n  ProviderName: Intel\n  PublisherName: Intel Corporation\n  InvoiceIssuerName: Intel Corporation\n  PricingCategory: Free\n  PricingUnit: not-applicable\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: attestation_requests\n    description: Trust Authority attestation requests issued by the customer\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - tee_type\n      - workload\n  - name: support_subscriptions\n    description: Active paid support subscriptions (Trust Authority and oneAPI Priority Support)\n    unit: subscription-month\n    aggregation: max\n    dimensions:\n      - product\n      - tier\napis:\n  - name: Intel Trust Authority API\n    baseURL:\
  \ https://api.trustauthority.intel.com\n    serviceCategory: API\n  - name: Intel oneAPI\n    baseURL: https://api-portal.intel.com\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Active Workload\n    metric: support_cost / active_workloads\n    target: TBD\n  - name: Attestation Requests per Workload\n    metric: attestation_requests / active_workloads\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/intel/refs/heads/main/finops/intel-finops.yml
sources:
- https://docs.trustauthority.intel.com/main/articles/restapi-intro.html
- https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html
specification: FinOps Framework
tags:
- Confidential Computing
- Attestation
- oneAPI
- FinOps
- FOCUS
---
