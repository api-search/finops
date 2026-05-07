---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: trustradius-public-openapi.yml
  format: yaml
  label: TrustRadius Public API
  slug: trustradius-public-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trustradius/refs/heads/main/openapi/trustradius-public-openapi.yml
- filename: trustradius-reviews-openapi.yml
  format: yaml
  label: TrustRadius Reviews API
  slug: trustradius-reviews-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trustradius/refs/heads/main/openapi/trustradius-reviews-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: TrustRadius vendor packages are sold through direct sales, with no public pricing or metered usage API. FinOps surface is limited to the contracted subscription line — no per-unit meters or FOCUS-aligned usage export is published.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TrustRadius, LLC
  ProviderName: TrustRadius
  PublisherName: TrustRadius, LLC
  ServiceCategory: B2B Software Reviews
  ServiceName: TrustRadius
layout: finops
meters:
- aggregation: sum
  description: Contracted vendor subscription line; no public meter detail published.
  name: vendor_subscription
  unit: month
name: Trustradius Finops
provider_name: TrustRadius
provider_slug: trustradius
publisher_name: TrustRadius, LLC
service_category: B2B Software Reviews
slug: trustradius-finops
source_filename: trustradius-finops.yml
source_heading: FinOps Profile
source_url: https://www.trustradius.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TrustRadius\nproviderId: trustradius\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Reviews\n  - B2B Software\n  - FinOps\n  - FOCUS\ndescription: TrustRadius vendor packages are sold through direct sales, with no public pricing or metered\n  usage API. FinOps surface is limited to the contracted subscription line — no per-unit meters or FOCUS-aligned\n  usage export is published.\nsources:\n  - https://www.trustradius.com/\nnotes: No public pricing or usage telemetry. Trimmed to a Contact Sales shape until vendor-program details\n  are disclosed.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TrustRadius, LLC\nserviceCategory: B2B Software Reviews\n\
  billingModel:\n  pricingCategory: Contract\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TrustRadius\n  ServiceCategory: B2B Software Reviews\n  ProviderName: TrustRadius\n  PublisherName: TrustRadius, LLC\n  InvoiceIssuerName: TrustRadius, LLC\n  BillingCurrency: USD\nmeters:\n  - name: vendor_subscription\n    description: Contracted vendor subscription line; no public meter detail published.\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is limited to the contracted subscription invoice; TrustRadius does not expose\n      a usage API or FOCUS export for self-service consumption.\n  - name: Allocation\n    description: Allocate the vendor subscription to the marketing or product-marketing budget that owns\n      the listing and review program.\n  - name: Optimization\n    description: Optimization happens at renewal — review the package mix (reviews, syndication,\
  \ intent\n      data, awards) against attributable pipeline before resigning.\n  - name: Accountability\n    description: A marketing or CMO-organization owner manages the TrustRadius relationship and renewal;\n      finance approves the annual contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trustradius/refs/heads/main/finops/trustradius-finops.yml
sources:
- https://www.trustradius.com/
specification: FinOps Framework
tags:
- Reviews
- B2B Software
- FinOps
- FOCUS
---
