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
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Custom / Contract
description: FinOps placeholder for CF Industries Holdings. CF is a fertilizer and clean-hydrogen manufacturer with no public API surface or developer billing model; FOCUS columns and meters reflect a hypothetical partner integration billing surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CF Industries Holdings, Inc.
  ProviderName: CF Industries Holdings
  PublisherName: CF Industries Holdings, Inc.
  ServiceCategory: Manufacturing
  ServiceName: CF Industries
layout: finops
meters:
- aggregation: sum
  name: partner_integrations
  unit: varies
name: Cf Industries Holdings Finops
provider_name: CF Industries Holdings
provider_slug: cf-industries-holdings
publisher_name: CF Industries Holdings, Inc.
service_category: Manufacturing / Fertilizer
slug: cf-industries-holdings-finops
source_filename: cf-industries-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.cfindustries.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CF Industries Holdings\nproviderId: cf-industries-holdings\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Fertilizer\n  - Manufacturing\ndescription: FinOps placeholder for CF Industries Holdings. CF is a fertilizer and clean-hydrogen manufacturer\n  with no public API surface or developer billing model; FOCUS columns and meters reflect a hypothetical\n  partner integration billing surface.\nnotes: No public API/billing surface; placeholder retained.\nsources:\n  - https://www.cfindustries.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CF Industries Holdings, Inc.\nserviceCategory: Manufacturing / Fertilizer\nbillingModel:\n\
  \  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: CF Industries\n  ServiceCategory: Manufacturing\n  ProviderName: CF Industries Holdings\n  PublisherName: CF Industries Holdings, Inc.\n  InvoiceIssuerName: CF Industries Holdings, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: partner_integrations\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public consumption telemetry; rely on contractual reporting from CF commercial team.\n  - name: Allocation\n    description: Allocate partner integration costs against the supply chain or procurement team owning\n      the CF relationship.\n  - name: Optimization\n    description: Negotiate volume terms, consolidate EDI feeds, and coordinate logistics scheduling against\n      CF distribution windows.\n  - name: Accountability\n    description: Procurement\
  \ / supply chain owner reviews CF invoices and contract renewals.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cf-industries-holdings/refs/heads/main/finops/cf-industries-holdings-finops.yml
sources:
- https://www.cfindustries.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Fertilizer
- Manufacturing
---
