---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: domains-openapi-original.yml
  format: yaml
  label: Gandi Domain API
  slug: domains
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gandi/refs/heads/main/openapi/domains-openapi-original.yml
- filename: livedns-openapi-original.yml
  format: yaml
  label: Gandi LiveDNS API
  slug: livedns
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gandi/refs/heads/main/openapi/livedns-openapi-original.yml
billing_model:
  billingCurrency: USD/EUR
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Tax
  - Refund
  - Adjustment
  pricingCategory: Per-Resource Purchase
description: 'FOCUS-aligned FinOps for Gandi: per-resource purchase model. Charges accrue on domain registration / renewal / transfer (per TLD per year), mailbox subscriptions, and any optional add-ons. The Public API itself is free for account holders.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Gandi SAS
  ProviderName: Gandi
  PublisherName: Gandi SAS
  ServiceCategory: Domain Registrar & DNS
  ServiceName: Gandi
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tld
  - action
  name: domain_registrations
  unit: domain-year
- aggregation: max
  dimensions:
  - plan
  name: mailboxes
  unit: mailbox-month
- aggregation: sum
  dimensions:
  - type
  name: ssl_certificates
  unit: certificate
- aggregation: sum
  dimensions:
  - api_product
  name: api_calls
  unit: request
name: Gandi Finops
provider_name: Gandi
provider_slug: gandi
publisher_name: Gandi SAS
service_category: Domain Registrar & DNS
slug: gandi-finops
source_filename: gandi-finops.yml
source_heading: FinOps Profile
source_url: https://www.gandi.net/en/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Gandi\nproviderId: gandi\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Domains\n  - DNS\n  - Registrar\ndescription: 'FOCUS-aligned FinOps for Gandi: per-resource purchase model. Charges accrue on\n  domain registration / renewal / transfer (per TLD per year), mailbox subscriptions, and any\n  optional add-ons. The Public API itself is free for account holders.'\nsources:\n  - https://www.gandi.net/en/pricing\n  - https://api.gandi.net/docs/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Gandi SAS\nserviceCategory: Domain Registrar & DNS\nbillingModel:\n  pricingCategory: Per-Resource Purchase\n  billingFrequency: Per-Invoice\n\
  \  billingCurrency: USD/EUR\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: Gandi\n  ServiceCategory: Domain Registrar & DNS\n  ProviderName: Gandi\n  PublisherName: Gandi SAS\n  InvoiceIssuerName: Gandi SAS\n  BillingCurrency: USD\nmeters:\n  - name: domain_registrations\n    unit: domain-year\n    aggregation: sum\n    dimensions:\n      - tld\n      - action\n  - name: mailboxes\n    unit: mailbox-month\n    aggregation: max\n    dimensions:\n      - plan\n  - name: ssl_certificates\n    unit: certificate\n    aggregation: sum\n    dimensions:\n      - type\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_product\nprinciples:\n  - name: Visibility\n    description: Use the Gandi Billing API and the account billing dashboard to enumerate\n      registered resources and upcoming renewals; reconcile against invoices.\n  - name: Allocation\n    description: Tag domains to projects/teams\
  \ via Gandi's organization model; segregate API\n      tokens (PATs) per consumer to attribute API-driven purchases.\n  - name: Optimization\n    description: Take advantage of promotional first-year TLDs; consolidate renewal cycles;\n      use included free SSL and DNS rather than separate vendors.\n  - name: Accountability\n    description: Domain ops owns renewal calendar; finance reviews TLD-mix and registrar-fee\n      variance at quarter-end.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gandi/refs/heads/main/finops/gandi-finops.yml
sources:
- https://www.gandi.net/en/pricing
- https://api.gandi.net/docs/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Domains
- DNS
- Registrar
---
