---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Sideko API
  slug: sideko-api
  spec_type: OpenAPI
  url: https://docs.sideko.dev/reference/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Tiered Subscription + Per-Language Upsell
description: FOCUS-aligned FinOps for Sideko. Sideko bills as a tiered SaaS subscription (Starter free, Pro $400/month annual, Enterprise custom) with per-additional-SDK-language metered upsell at $400/month each. Quota dimensions are SDK languages, included APIs, and documentation projects.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sideko, Inc.
  ProviderName: Sideko
  PublisherName: Sideko, Inc.
  ServiceCategory: Developer Tools
  ServiceName: Sideko
layout: finops
meters:
- aggregation: sum
  description: Monthly Sideko plan fee billed annually.
  dimensions:
  - plan
  name: subscription
  unit: month
- aggregation: sum
  description: Per-additional-SDK-language fee on the Pro plan ($400/month each).
  dimensions:
  - plan
  - language
  name: sdk_language_upsell
  unit: sdk-language
- aggregation: max
  description: Count of APIs onboarded against the plan ceiling (1 Starter, 10 Pro, unlimited Enterprise).
  dimensions:
  - plan
  name: apis_used
  unit: api
- aggregation: max
  description: Count of documentation projects against the plan ceiling.
  dimensions:
  - plan
  name: doc_projects_used
  unit: project
name: Sideko Finops
provider_name: Sideko
provider_slug: sideko
publisher_name: Sideko, Inc.
service_category: Developer Tools
slug: sideko-finops
source_filename: sideko-finops.yml
source_heading: FinOps Profile
source_url: https://sideko.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sideko\nproviderId: sideko\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - API Tooling\n  - SDK Generation\n  - Documentation\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Sideko. Sideko bills as a tiered SaaS subscription (Starter free,\n  Pro $400/month annual, Enterprise custom) with per-additional-SDK-language metered upsell at $400/month\n  each. Quota dimensions are SDK languages, included APIs, and documentation projects.\nsources:\n  - https://sideko.dev/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Sideko, Inc.\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Tiered Subscription + Per-Language Upsell\n\
  \  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Sideko\n  ServiceCategory: Developer Tools\n  ProviderName: Sideko\n  PublisherName: Sideko, Inc.\n  InvoiceIssuerName: Sideko, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription\n    description: Monthly Sideko plan fee billed annually.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: sdk_language_upsell\n    description: Per-additional-SDK-language fee on the Pro plan ($400/month each).\n    unit: sdk-language\n    aggregation: sum\n    dimensions:\n      - plan\n      - language\n  - name: apis_used\n    description: Count of APIs onboarded against the plan ceiling (1 Starter, 10 Pro, unlimited Enterprise).\n    unit: api\n    aggregation: max\n    dimensions:\n      - plan\n  - name: doc_projects_used\n    description: Count of documentation projects against the plan ceiling.\n    unit: project\n \
  \   aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Sideko spend is a known monthly subscription line; track via the company invoice and\n      compare APIs/SDK languages onboarded against the Pro plan ceilings to predict upsell triggers.\n  - name: Allocation\n    description: Allocate Sideko cost to the platform/devex team that owns SDK and documentation generation;\n      attribute additional-language fees to the consuming product team requesting that SDK.\n  - name: Optimization\n    description: Consolidate APIs and doc projects under the Pro tier ceilings (10 APIs, 5 doc projects)\n      before triggering Enterprise; only add a paid SDK language when there is real consumer demand.\n  - name: Accountability\n    description: Developer experience or platform engineering owns Sideko renewal; product owners approve\n      additional-SDK-language requests since each adds $400/month.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sideko/refs/heads/main/finops/sideko-finops.yml
sources:
- https://sideko.dev/pricing
specification: FinOps Framework
tags:
- API Tooling
- SDK Generation
- Documentation
- FinOps
- FOCUS
---
