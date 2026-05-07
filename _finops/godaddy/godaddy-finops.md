---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: godaddy-domains-openapi.json
  format: json
  label: GoDaddy Domains API
  slug: domains
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-domains-openapi.json
- filename: godaddy-certificates-openapi.json
  format: json
  label: GoDaddy Certificates API
  slug: certificates
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-certificates-openapi.json
- filename: godaddy-shoppers-openapi.json
  format: json
  label: GoDaddy Shoppers API
  slug: shoppers
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-shoppers-openapi.json
- filename: godaddy-subscriptions-openapi.json
  format: json
  label: GoDaddy Subscriptions API
  slug: subscriptions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-subscriptions-openapi.json
- filename: godaddy-orders-openapi.json
  format: json
  label: GoDaddy Orders API
  slug: orders
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-orders-openapi.json
- filename: godaddy-aftermarket-openapi.json
  format: json
  label: GoDaddy Aftermarket API
  slug: aftermarket
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-aftermarket-openapi.json
- filename: godaddy-abuse-openapi.json
  format: json
  label: GoDaddy Abuse API
  slug: abuse
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-abuse-openapi.json
- filename: godaddy-agreements-openapi.json
  format: json
  label: GoDaddy Agreements API
  slug: agreements
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-agreements-openapi.json
- filename: godaddy-countries-openapi.json
  format: json
  label: GoDaddy Countries API
  slug: countries
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/openapi/godaddy-countries-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Transaction
  chargeCategories:
  - Purchase
  - Tax
  - Refund
  - Adjustment
  pricingCategory: Pay-As-You-Go (Product Fees)
description: 'FOCUS-aligned FinOps for the GoDaddy API: API usage itself is free, but underlying product fees (domain registrations/renewals, SSL certificates, hosting) are charged per transaction against a Good as Gold funded account.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: GoDaddy.com, LLC
  ProviderName: GoDaddy
  PublisherName: GoDaddy.com, LLC
  ServiceCategory: Domains / Registrar
  ServiceName: GoDaddy API
layout: finops
meters:
- aggregation: sum
  description: Domain registrations and renewals purchased through the API
  dimensions:
  - tld
  - duration_years
  name: domain_registrations
  unit: domain-year
- aggregation: sum
  description: SSL/TLS certificate purchases and renewals
  dimensions:
  - certificate_type
  name: ssl_certificates
  unit: certificate-year
- aggregation: sum
  description: Premium / aftermarket domain acquisitions
  name: aftermarket_purchases
  unit: transaction
- aggregation: sum
  description: API call volume (informational - not billed)
  dimensions:
  - endpoint
  - environment
  name: api_requests
  unit: request
name: Godaddy Finops
provider_name: GoDaddy
provider_slug: godaddy
publisher_name: GoDaddy.com, LLC
service_category: Domains / DNS / Hosting
slug: godaddy-finops
source_filename: godaddy-finops.yml
source_heading: FinOps Profile
source_url: https://developer.godaddy.com/getstarted
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: GoDaddy\nproviderId: godaddy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\ntags:\n  - FinOps\n  - FOCUS\n  - Domains\n  - DNS\n  - Registrar\nreconciled: true\ndescription: 'FOCUS-aligned FinOps for the GoDaddy API: API usage itself is free, but underlying product\n  fees (domain registrations/renewals, SSL certificates, hosting) are charged per transaction against\n  a Good as Gold funded account.'\nsources:\n  - https://developer.godaddy.com/getstarted\n  - https://www.godaddy.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: GoDaddy.com, LLC\nserviceCategory: Domains / DNS / Hosting\nbillingModel:\n  pricingCategory: Pay-As-You-Go (Product Fees)\n  billingFrequency: Per-Transaction\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: GoDaddy API\n  ServiceCategory: Domains / Registrar\n  ProviderName: GoDaddy\n  PublisherName: GoDaddy.com, LLC\n  InvoiceIssuerName: GoDaddy.com, LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: domain_registrations\n    description: Domain registrations and renewals purchased through the API\n    unit: domain-year\n    aggregation: sum\n    dimensions:\n      - tld\n      - duration_years\n  - name: ssl_certificates\n    description: SSL/TLS certificate purchases and renewals\n    unit: certificate-year\n    aggregation: sum\n    dimensions:\n      - certificate_type\n  - name: aftermarket_purchases\n    description: Premium / aftermarket domain acquisitions\n    unit: transaction\n    aggregation: sum\n  - name: api_requests\n    description: API call volume (informational - not billed)\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - endpoint\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use the Orders, Subscriptions, and Shoppers APIs to programmatically reconcile spending\n      against the Good as Gold account ledger.\n  - name: Allocation\n    description: Tag domain purchases via account/sub-account structure when operating as a reseller;\n      attribute SSL purchases to the requesting service.\n  - name: Optimization\n    description: Use multi-year registration discounts; consolidate certificates into wildcards; capture\n      promo pricing surfaced in the Domains API rather than retail.\n  - name: Accountability\n    description: Domain owners or the platform team funding the Good as Gold account own renewal calendars\n      and budget approvals; surface upcoming renewals in monthly reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/godaddy/refs/heads/main/finops/godaddy-finops.yml
sources:
- https://developer.godaddy.com/getstarted
- https://www.godaddy.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Domains
- DNS
- Registrar
---
