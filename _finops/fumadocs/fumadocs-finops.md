---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fumadocs-search-openapi.yml
  format: yaml
  label: Fumadocs Search API
  slug: search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fumadocs/refs/heads/main/openapi/fumadocs-search-openapi.yml
- filename: fumadocs-openapi-proxy-openapi.yml
  format: yaml
  label: Fumadocs OpenAPI Proxy API
  slug: openapi-proxy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fumadocs/refs/heads/main/openapi/fumadocs-openapi-proxy-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Free / Open Source
description: Fumadocs has no commercial billing surface — it is a free, open-source npm package. The only FinOps-relevant cost is the underlying hosting/CDN of the consumer's documentation site, which is governed by the host's pricing rather than Fumadocs.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: not-applicable
  ProviderName: Fumadocs
  PublisherName: Fumadocs (open source community)
  ServiceCategory: Developer Tools
  ServiceName: Fumadocs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - host
  name: hosting_costs
  unit: varies
name: Fumadocs Finops
provider_name: Fumadocs
provider_slug: fumadocs
publisher_name: Fumadocs (open source community)
service_category: Developer Tools
slug: fumadocs-finops
source_filename: fumadocs-finops.yml
source_heading: FinOps Profile
source_url: https://fumadocs.dev/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Fumadocs\nproviderId: fumadocs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Open Source\n  - Documentation\ndescription: Fumadocs has no commercial billing surface — it is a free, open-source npm package.\n  The only FinOps-relevant cost is the underlying hosting/CDN of the consumer's documentation\n  site, which is governed by the host's pricing rather than Fumadocs.\nsources:\n  - https://fumadocs.dev/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fumadocs (open source community)\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Free / Open Source\n  billingFrequency: On-Demand\n  billingCurrency: USD\n\
  \  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Fumadocs\n  ServiceCategory: Developer Tools\n  ProviderName: Fumadocs\n  PublisherName: Fumadocs (open source community)\n  InvoiceIssuerName: not-applicable\n  BillingCurrency: USD\nmeters:\n  - name: hosting_costs\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - host\nprinciples:\n  - name: Visibility\n    description: Costs of running a Fumadocs site come from the underlying host (Vercel, Netlify,\n      Cloudflare Pages, etc.); track those provider bills rather than Fumadocs.\n  - name: Allocation\n    description: Allocate documentation-site hosting cost to the product or team that owns the\n      docs.\n  - name: Optimization\n    description: Use static export and CDN caching; pre-build search indexes; avoid dynamic\n      runtime where the static path suffices.\n  - name: Accountability\n    description: DevRel / docs owner is accountable for documentation hosting cost; no Fumadocs\n      invoice\
  \ exists.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fumadocs/refs/heads/main/finops/fumadocs-finops.yml
sources:
- https://fumadocs.dev/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Open Source
- Documentation
---
