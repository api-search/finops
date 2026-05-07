---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Adjustment
  pricingCategory: Bundled with Relationship
description: 'FOCUS-aligned FinOps for The Carlyle Group: institutional asset management with no public API billing surface; portal access is bundled with the LP/portfolio-company relationship.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Carlyle Group Inc.
  ProviderName: The Carlyle Group
  PublisherName: The Carlyle Group Inc.
  ServiceCategory: Investor Portal / Institutional Relationship
  ServiceName: Carlyle Institutional Portals
layout: finops
meters:
- aggregation: max
  dimensions:
  - portal
  - relationship
  name: portal_users
  unit: seat-month
- aggregation: sum
  dimensions:
  - fund
  name: management_fees
  unit: USD
- aggregation: sum
  dimensions:
  - fund
  name: performance_fees
  unit: USD
name: Carlyle Group Finops
provider_name: The Carlyle Group
provider_slug: carlyle-group
publisher_name: The Carlyle Group Inc.
service_category: Investor Portal / Institutional Relationship
slug: carlyle-group-finops
source_filename: carlyle-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.carlyle.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: The Carlyle Group\nproviderId: carlyle-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Asset Management\n  - Investor Portal\n  - Private Equity\ndescription: 'FOCUS-aligned FinOps for The Carlyle Group: institutional asset management with no public\n  API billing surface; portal access is bundled with the LP/portfolio-company relationship.'\nnotes: Carlyle does not bill API or portal access as a metered service. FinOps mapping is included for\n  consistency; treat as informational rather than reconcilable.\nsources:\n  - https://www.carlyle.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Carlyle Group Inc.\nserviceCategory:\
  \ Investor Portal / Institutional Relationship\nbillingModel:\n  pricingCategory: Bundled with Relationship\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Carlyle Institutional Portals\n  ServiceCategory: Investor Portal / Institutional Relationship\n  ProviderName: The Carlyle Group\n  PublisherName: The Carlyle Group Inc.\n  InvoiceIssuerName: The Carlyle Group Inc.\n  BillingCurrency: USD\nmeters:\n  - name: portal_users\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - portal\n      - relationship\n  - name: management_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - fund\n  - name: performance_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - fund\nprinciples:\n  - name: Visibility\n    description: Visibility comes from fund reporting (capital account statements, K-1s, quarterly letters)\n      rather than API usage telemetry.\n  - name: Allocation\n\
  \    description: Allocate by fund and vintage; LP-side cost attribution is by capital commitment.\n  - name: Optimization\n    description: Optimization is at the LP-portfolio level (fee negotiation, co-invest participation)\n      rather than at API-call level.\n  - name: Accountability\n    description: LP relationship manager / portfolio operations team owns the relationship; quarterly\n      LP advisory committee reviews are typical.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carlyle-group/refs/heads/main/finops/carlyle-group-finops.yml
sources:
- https://www.carlyle.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Asset Management
- Investor Portal
- Private Equity
---
