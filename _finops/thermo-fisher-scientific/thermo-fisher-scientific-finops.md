---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: thermo-fisher-samplemanager-openapi.yml
  format: yaml
  label: Thermo Fisher SampleManager LIMS REST API
  slug: samplemanager-lims
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thermo-fisher-scientific/refs/heads/main/openapi/thermo-fisher-samplemanager-openapi.yml
- filename: thermo-fisher-nanodrop-openapi.yml
  format: yaml
  label: Thermo Fisher NanoDrop Ultra Web API
  slug: nanodrop-ultra
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/thermo-fisher-scientific/refs/heads/main/openapi/thermo-fisher-nanodrop-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps scaffold for Thermo Fisher Scientific. Commercial relationships are a mix of consumables catalog purchasing, instrument capex / services, and digital-science software subscriptions; there is no public usage-based price list to map cleanly to FOCUS columns until the engagement is in place.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Thermo Fisher Scientific Inc.
  ProviderName: Thermo Fisher Scientific
  PublisherName: Thermo Fisher Scientific Inc.
  ServiceCategory: Life Sciences
  ServiceName: Thermo Fisher Scientific
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product_line
  name: digital_science_subscription
  unit: varies
name: Thermo Fisher Scientific Finops
provider_name: Thermo Fisher Scientific
provider_slug: thermo-fisher-scientific
publisher_name: Thermo Fisher Scientific Inc.
service_category: Life Sciences
slug: thermo-fisher-scientific-finops
source_filename: thermo-fisher-scientific-finops.yml
source_heading: FinOps Profile
source_url: https://www.thermofisher.com/us/en/home/digital-science.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Thermo Fisher Scientific\nproviderId: thermo-fisher-scientific\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Life Sciences\n  - LIMS\ndescription: >-\n  FOCUS-aligned FinOps scaffold for Thermo Fisher Scientific. Commercial relationships are a mix of consumables\n  catalog purchasing, instrument capex / services, and digital-science software subscriptions; there is\n  no public usage-based price list to map cleanly to FOCUS columns until the engagement is in place.\nsources:\n  - https://www.thermofisher.com/us/en/home/digital-science.html\n  - https://www.thermofisher.com/us/en/home/contact-us.html\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: >-\n  No public usage-based price list. Reconciliation is engagement-specific.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl:\
  \ https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Thermo Fisher Scientific Inc.\nserviceCategory: Life Sciences\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Thermo Fisher Scientific\n  ServiceCategory: Life Sciences\n  ProviderName: Thermo Fisher Scientific\n  PublisherName: Thermo Fisher Scientific Inc.\n  InvoiceIssuerName: Thermo Fisher Scientific Inc.\n  BillingCurrency: USD\nmeters:\n  - name: digital_science_subscription\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product_line\nprinciples:\n  - name: Visibility\n    description: Visibility surfaces are Thermo Fisher invoices, customer portal order history, and any\n      LIMS / digital-science admin consoles included in the engagement.\n  - name: Allocation\n    description:\
  \ Allocate spend across labs / programs based on Thermo Fisher PO and invoice line items\n      keyed to lab cost centers.\n  - name: Optimization\n    description: Consolidate purchasing under negotiated agreements, retire unused digital-science modules\n      at renewal, and align reagent reorder cadence with consumption.\n  - name: Accountability\n    description: Lab / program owner inside the customer organization owns Thermo Fisher spend and reviews\n      against contractual baseline at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/thermo-fisher-scientific/refs/heads/main/finops/thermo-fisher-scientific-finops.yml
sources:
- https://www.thermofisher.com/us/en/home/digital-science.html
- https://www.thermofisher.com/us/en/home/contact-us.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Life Sciences
- LIMS
---
