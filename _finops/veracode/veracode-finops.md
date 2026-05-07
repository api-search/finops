---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veracode-applications-openapi.yml
  format: yaml
  label: Veracode Applications REST API
  slug: veracode-applications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veracode/refs/heads/main/openapi/veracode-applications-openapi.yml
- filename: veracode-findings-openapi.yml
  format: yaml
  label: Veracode Findings REST API
  slug: veracode-findings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veracode/refs/heads/main/openapi/veracode-findings-openapi.yml
- filename: veracode-identity-openapi.yml
  format: yaml
  label: Veracode Identity REST API
  slug: veracode-identity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veracode/refs/heads/main/openapi/veracode-identity-openapi.yml
- filename: veracode-reporting-openapi.yml
  format: yaml
  label: Veracode Reporting REST API
  slug: veracode-reporting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veracode/refs/heads/main/openapi/veracode-reporting-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Veracode: enterprise application-security SaaS subscription with no public pricing or usage/billing API. API access is bundled with the platform subscription.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Veracode, Inc.
  ProviderName: Veracode
  PublisherName: Veracode, Inc.
  ServiceCategory: Application Security
  ServiceName: Veracode Application Security Platform
layout: finops
meters:
- aggregation: sum
  description: Annual Veracode platform subscription line; entitlements for SAST / DAST / SCA scans and seats are scoped in the order form.
  name: platform_subscription
  unit: varies
name: Veracode Finops
provider_name: Veracode
provider_slug: veracode
publisher_name: Veracode, Inc.
service_category: Application Security
slug: veracode-finops
source_filename: veracode-finops.yml
source_heading: FinOps Profile
source_url: https://www.veracode.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veracode\nproviderId: veracode\npublisherName: Veracode, Inc.\nserviceCategory: Application Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Security\n  - DevSecOps\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Veracode: enterprise application-security SaaS subscription\n  with no public pricing or usage/billing API. API access is bundled with the platform subscription.'\nsources:\n  - https://www.veracode.com/pricing\n  - https://docs.veracode.com/r/About_Veracode_API_Best_Practices\nnotes: No public pricing. Meters are not invented; API call counts are operational telemetry\
  \ rather than\n  billable units. Reconciliation deferred pending customer-portal billing data.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Veracode Application Security Platform\n  ServiceCategory: Application Security\n  ProviderName: Veracode\n  PublisherName: Veracode, Inc.\n  InvoiceIssuerName: Veracode, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: platform_subscription\n    description: Annual Veracode platform subscription line; entitlements for SAST / DAST / SCA scans\n      and seats are scoped in the order form.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Veracode exposes scan and finding telemetry via the Reporting, Findings, and Summary\n      Report REST APIs; there is no public cost / usage API. Track entitlement consumption (scan-counts,\n      seats) against the order-form scope.\n  - name: Allocation\n\
  \    description: Allocation is contract-level (which application portfolios and teams are entitled).\n      Internal chargeback typically rides on application ownership tags applied in the Veracode platform.\n  - name: Optimization\n    description: Optimization levers include scoping which apps are scanned, scan cadence, and avoiding\n      wasted polling (the docs require 2-minute minimum spacing on status checks and cap retries at 5).\n  - name: Accountability\n    description: Accountability sits with the AppSec team that owns the Veracode tenant; finance owns\n      the annual subscription line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veracode/refs/heads/main/finops/veracode-finops.yml
sources:
- https://www.veracode.com/pricing
- https://docs.veracode.com/r/About_Veracode_API_Best_Practices
specification: FinOps Framework
tags:
- Application Security
- DevSecOps
- FinOps
- FOCUS
---
