---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Trellix Web Gateway REST API
  slug: trellix-web-gateway-rest-api
  spec_type: OpenAPI
  url: https://docs.trellix.com/api/web-gateway/openapi.json
- filename: trellix-web-gateway-reporting-openapi.yml
  format: yaml
  label: Trellix Web Gateway Reporting API
  slug: trellix-web-gateway-reporting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trellix-web-gateway/refs/heads/main/openapi/trellix-web-gateway-reporting-openapi.yml
- filename: trellix-web-gateway-policy-openapi.yml
  format: yaml
  label: Trellix Web Gateway Policy API
  slug: trellix-web-gateway-policy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trellix-web-gateway/refs/heads/main/openapi/trellix-web-gateway-policy-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Negotiated
description: FinOps shape for Trellix Web Gateway cannot be reconciled from public sources; pricing is contact-sales only and the management API ships under the customer's SWG license.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Skyhigh Security / Trellix
  ProviderName: Trellix
  PublisherName: Skyhigh Security / Trellix
  ServiceCategory: Cybersecurity
  ServiceName: Trellix Web Gateway
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  name: license_seats
  unit: seat
name: Trellix Web Gateway Finops
provider_name: Trellix Web Gateway
provider_slug: trellix-web-gateway
publisher_name: Skyhigh Security / Trellix
service_category: Cybersecurity
slug: trellix-web-gateway-finops
source_filename: trellix-web-gateway-finops.yml
source_heading: FinOps Profile
source_url: https://www.skyhighsecurity.com/products/secure-web-gateway.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Trellix Web Gateway\nproviderId: trellix-web-gateway\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cybersecurity\n  - Secure Web Gateway\n  - Network Security\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Trellix Web Gateway cannot be reconciled from public sources; pricing\n  is contact-sales only and the management API ships under the customer's SWG license.\nsources:\n  - https://www.skyhighsecurity.com/products/secure-web-gateway.html\nnotes: No public pricing or usage telemetry surfaces are published. Meters and FOCUS column values\n  can only be confirmed against the executed SWG license and the management console.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Skyhigh Security / Trellix\nserviceCategory: Cybersecurity\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Trellix Web Gateway\n  ServiceCategory: Cybersecurity\n  ProviderName: Trellix\n  PublisherName: Skyhigh Security / Trellix\n  InvoiceIssuerName: Skyhigh Security / Trellix\n  BillingCurrency: USD\nmeters:\n  - name: license_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Web traffic, policy decisions, and management-API call counts are exposed in the SWG\n      admin console; finance reconciles against the annual license contract.\n  - name: Allocation\n    description: Allocate cost by protected business unit / site and by policy template inside the SWG\n      tenant.\n  - name: Optimization\n    description: Optimization is contractual — right-size protected\
  \ user counts and consolidate cloud\n      vs on-prem deployments at renewal.\n  - name: Accountability\n    description: Network security / CISO organization owns the SWG contract; procurement manages\n      renewal and seat true-up.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trellix-web-gateway/refs/heads/main/finops/trellix-web-gateway-finops.yml
sources:
- https://www.skyhighsecurity.com/products/secure-web-gateway.html
specification: FinOps Framework
tags:
- Cybersecurity
- Secure Web Gateway
- Network Security
- FinOps
- FOCUS
---
