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
  pricingCategory: Custom / Contact Sales
description: FinOps placeholder for Tapestry, Inc. No public API billing surface; commercial partner billing is invoiced under bilateral agreements per brand.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tapestry, Inc.
  ProviderName: Tapestry
  PublisherName: Tapestry, Inc.
  ServiceCategory: Apparel & Accessories Retail
  ServiceName: Tapestry
layout: finops
meters:
- aggregation: sum
  name: custom_engagement
  unit: varies
name: Tapestry Finops
provider_name: Tapestry
provider_slug: tapestry
publisher_name: Tapestry, Inc.
service_category: Apparel & Accessories Retail
slug: tapestry-finops
source_filename: tapestry-finops.yml
source_heading: FinOps Profile
source_url: https://www.tapestry.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tapestry\nproviderId: tapestry\npublisherName: Tapestry, Inc.\nserviceCategory: Apparel & Accessories Retail\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Apparel\n  - Retail\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Tapestry, Inc. No public API billing surface; commercial\n  partner billing is invoiced under bilateral agreements per brand.\nsources:\n  - https://www.tapestry.com/\nnotes: No public billing telemetry. Meter list collapsed to custom engagement.\nbillingModel:\n  pricingCategory: Custom / Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  \
  \  - Usage\nfocusColumns:\n  ServiceName: Tapestry\n  ServiceCategory: Apparel & Accessories Retail\n  ProviderName: Tapestry\n  PublisherName: Tapestry, Inc.\n  InvoiceIssuerName: Tapestry, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: custom_engagement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is provided through Tapestry's brand partnership and merchandising\n      teams; no public usage API ships.\n  - name: Allocation\n    description: Cost is allocated to the partnering team's own AP records against Tapestry brand\n      invoices.\n  - name: Optimization\n    description: Optimization is handled through commercial review with the brand partnership\n      manager.\n  - name: Accountability\n    description: Accountability sits with the partner-facing or merchandising owner of the Tapestry\n      relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tapestry/refs/heads/main/finops/tapestry-finops.yml
sources:
- https://www.tapestry.com/
specification: FinOps Framework
tags:
- Apparel
- Retail
- FinOps
- FOCUS
---
