---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: target-target-api-openapi.yml
  format: yaml
  label: Target API
  slug: target-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/target/refs/heads/main/openapi/target-target-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  pricingCategory: Custom / Contact Sales
description: FinOps placeholder for Target Corporation. No public developer billing surface; partner-program billing is governed by program-specific terms (vendor / Target+ / Roundel / Shipt) and falls under the partner's own AP reconciliation against Target invoices.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Target Corporation
  ProviderName: Target
  PublisherName: Target Corporation
  ServiceCategory: Retail
  ServiceName: Target
layout: finops
meters:
- aggregation: sum
  name: custom_engagement
  unit: varies
name: Target Finops
provider_name: target
provider_slug: target
publisher_name: Target Corporation
service_category: Retail
slug: target-finops
source_filename: target-finops.yml
source_heading: FinOps Profile
source_url: https://corporate.target.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: target\nproviderId: target\npublisherName: Target Corporation\nserviceCategory: Retail\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Retail\n  - Ecommerce\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Target Corporation. No public developer billing surface;\n  partner-program billing is governed by program-specific terms (vendor / Target+ / Roundel /\n  Shipt) and falls under the partner's own AP reconciliation against Target invoices.\nsources:\n  - https://corporate.target.com/\nnotes: No public billing telemetry for partner / developer programs. Meter list collapsed to\n  custom engagement pending\
  \ program-specific confirmation.\nbillingModel:\n  pricingCategory: Custom / Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Target\n  ServiceCategory: Retail\n  ProviderName: Target\n  PublisherName: Target Corporation\n  InvoiceIssuerName: Target Corporation\n  BillingCurrency: USD\nmeters:\n  - name: custom_engagement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is delivered through program-specific partner portals (vendor portal,\n      Target+, Roundel) rather than a unified public usage API.\n  - name: Allocation\n    description: Allocation is handled in the partner's own AP system against the program's invoice\n      line items.\n  - name: Optimization\n    description: Optimization is addressed in commercial review with the program team (assortment,\n      media spend, marketplace fees).\n  - name: Accountability\n    description: Accountability\
  \ sits with the partner team that owns the relevant Target program\n      relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/target/refs/heads/main/finops/target-finops.yml
sources:
- https://corporate.target.com/
specification: FinOps Framework
tags:
- Retail
- Ecommerce
- FinOps
- FOCUS
---
