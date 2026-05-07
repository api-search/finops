---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom / Contract
description: FinOps placeholder for Century Communities. No public API surface, billing model, or pricing documentation has been identified; FOCUS columns and meters are illustrative defaults.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Century Communities, Inc.
  ProviderName: Century Communities
  PublisherName: Century Communities, Inc.
  ServiceCategory: Real Estate
  ServiceName: Century Communities
layout: finops
meters:
- aggregation: sum
  name: partner_integrations
  unit: varies
name: Century Communities Finops
provider_name: Century Communities
provider_slug: century-communities
publisher_name: Century Communities, Inc.
service_category: Real Estate
slug: century-communities-finops
source_filename: century-communities-finops.yml
source_heading: FinOps Profile
source_url: https://www.centurycommunities.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Century Communities\nproviderId: century-communities\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Real Estate\n  - Homebuilding\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Century Communities. No public API surface, billing model, or pricing\n  documentation has been identified; FOCUS columns and meters are illustrative defaults.\nnotes: No public API or billing documentation located. Retained as placeholder pending partner integration\n  discovery.\nsources:\n  - https://www.centurycommunities.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Century Communities, Inc.\nserviceCategory: Real Estate\nbillingModel:\n  pricingCategory:\
  \ Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Century Communities\n  ServiceCategory: Real Estate\n  ProviderName: Century Communities\n  PublisherName: Century Communities, Inc.\n  InvoiceIssuerName: Century Communities, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: partner_integrations\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public consumption telemetry is documented; rely on partner contract reporting if\n      a relationship is established.\n  - name: Allocation\n    description: Allocate any partner integration costs against the team owning the Century Communities\n      relationship.\n  - name: Optimization\n    description: Negotiate volume terms in any partner contract; consolidate data feeds where possible.\n  - name: Accountability\n    description: Partner relationship owner is accountable\
  \ for any contractual costs and renewal review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/century-communities/refs/heads/main/finops/century-communities-finops.yml
sources:
- https://www.centurycommunities.com
specification: FinOps Framework
tags:
- Real Estate
- Homebuilding
- FinOps
- FOCUS
---
