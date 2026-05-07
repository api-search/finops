---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for ADP: subscription-based HCM platform billing with per-employee fees and partner contract terms. API access is bundled into the customer''s ADP product subscription; partners do not see per-call charges.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ADP, Inc.
  ProviderName: ADP
  PublisherName: ADP, Inc.
  ServiceCategory: HCM / Payroll
  ServiceName: ADP
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - country
  name: payroll_employees
  unit: seat
- aggregation: count
  dimensions:
  - product
  - country
  name: payroll_runs
  unit: run
- aggregation: sum
  dimensions:
  - partner
  - product
  name: api_partner_subscription
  unit: month
- aggregation: sum
  dimensions:
  - jurisdiction
  name: tax_filings
  unit: filing
name: Automatic Data Processing Finops
provider_name: Automatic Data Processing (ADP)
provider_slug: automatic-data-processing
publisher_name: ADP, Inc.
service_category: HCM / Payroll
slug: automatic-data-processing-finops
source_filename: automatic-data-processing-finops.yml
source_heading: FinOps Profile
source_url: https://www.adp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Automatic Data Processing (ADP)\nproviderId: automatic-data-processing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: ADP API access is bundled into the ADP product subscription rather than separately metered. This\n  artifact models the FinOps shape of an ADP integration partner; concrete invoice line items require a\n  signed partner agreement.\ntags:\n  - FinOps\n  - FOCUS\n  - HCM\n  - Payroll\n  - HR\ndescription: 'FOCUS-aligned FinOps for ADP: subscription-based HCM platform billing with per-employee\n  fees and partner contract terms. API access is bundled into the customer''s ADP product subscription;\n  partners do not see per-call charges.'\nsources:\n  - https://www.adp.com/\n  - https://apps.adp.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ADP, Inc.\nserviceCategory: HCM / Payroll\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: ADP\n  ServiceCategory: HCM / Payroll\n  ProviderName: ADP\n  PublisherName: ADP, Inc.\n  InvoiceIssuerName: ADP, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: payroll_employees\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n      - country\n  - name: payroll_runs\n    unit: run\n    aggregation: count\n    dimensions:\n      - product\n      - country\n  - name: api_partner_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - partner\n      - product\n  - name: tax_filings\n    unit: filing\n    aggregation: sum\n    dimensions:\n      - jurisdiction\nprinciples:\n\
  \  - name: Visibility\n    description: ADP invoices are issued at the customer (employer) level. Partners do not directly see\n      consumption — they negotiate a separate partner fee. Use ADP customer admin reports to attribute\n      spend.\n  - name: Allocation\n    description: Allocate ADP spend by department / cost center using ADP's payroll-codes structure;\n      tag integrations by partner application and consenting customer.\n  - name: Optimization\n    description: Right-size by ADP product (RUN for SMB, Workforce Now for mid-market, Vantage / GlobalView\n      for enterprise). Consolidate per-employee charges across legal entities where ADP allows it.\n  - name: Accountability\n    description: HR Operations or Payroll Ops typically owns the ADP relationship; integration partners\n      assign budget ownership to the consuming product team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/automatic-data-processing/refs/heads/main/finops/automatic-data-processing-finops.yml
sources:
- https://www.adp.com/
- https://apps.adp.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- HCM
- Payroll
- HR
---
