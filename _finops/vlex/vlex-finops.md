---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vlex-iceberg-anonymization-openapi.yml
  format: yaml
  label: vLex Iceberg Anonymization API
  slug: iceberg-anonymization-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vlex/refs/heads/main/openapi/vlex-iceberg-anonymization-openapi.yml
- filename: vlex-iceberg-legal-research-openapi.yml
  format: yaml
  label: vLex Iceberg Legal Research API
  slug: iceberg-legal-research-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vlex/refs/heads/main/openapi/vlex-iceberg-legal-research-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Subscription + Custom Terms
description: FOCUS-aligned FinOps shape for vLex. Pricing is custom-quoted per organization and product; meters cover the canonical billable units on a vLex contract (seats and metered AI queries / document operations) without inventing public unit prices.
focus_columns:
  BillingCurrency: USD
  ProviderName: vLex
  PublisherName: vLex Justis
  ServiceCategory: Legal Research / Legal AI
  ServiceName: vLex
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  name: seats
  unit: seat
- aggregation: sum
  dimensions:
  - product
  name: ai_queries
  unit: query
- aggregation: sum
  dimensions:
  - product
  name: document_views
  unit: document
name: Vlex Finops
provider_name: vLex
provider_slug: vlex
publisher_name: vLex Justis
service_category: Legal Research / Legal AI
slug: vlex-finops
source_filename: vlex-finops.yml
source_heading: FinOps Profile
source_url: https://vlex.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: vLex\nproviderId: vlex\npublisherName: vLex Justis\nserviceCategory: Legal Research / Legal AI\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Legal\n  - Legal Research\n  - Legal AI\ndescription: FOCUS-aligned FinOps shape for vLex. Pricing is custom-quoted per organization and\n  product; meters cover the canonical billable units on a vLex contract (seats and metered AI\n  queries / document operations) without inventing public unit prices.\nsources:\n  - https://vlex.com/products\nnotes: No public unit prices were available; commercial terms are negotiated through vLex sales.\nbillingModel:\n  pricingCategory: Subscription + Custom Terms\n\
  \  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: vLex\n  ServiceCategory: Legal Research / Legal AI\n  ProviderName: vLex\n  PublisherName: vLex Justis\n  BillingCurrency: USD\nmeters:\n  - name: seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n  - name: ai_queries\n    unit: query\n    aggregation: sum\n    dimensions:\n      - product\n  - name: document_views\n    unit: document\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Visibility is delivered through the vLex admin console (per-seat usage, query\n      counts) and the contracted reporting cadence; there is no FOCUS export.\n  - name: Allocation\n    description: Allocate seat and query consumption to practice groups / matter codes via the\n      organization mapping in the vLex admin console.\n  - name: Optimization\n    description: Levers are\
  \ seat right-sizing across practice groups, retiring inactive accounts,\n      and selecting the product mix (Vincent vs Library vs Docket Alarm) that matches actual use.\n  - name: Accountability\n    description: Knowledge management / library services typically owns the vLex contract;\n      finance reconciles annually against the contracted seat count and any metered overages.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vlex/refs/heads/main/finops/vlex-finops.yml
sources:
- https://vlex.com/products
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Legal
- Legal Research
- Legal AI
---
