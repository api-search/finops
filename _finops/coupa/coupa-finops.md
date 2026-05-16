---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api_docs
  format: yaml
  label: Coupa Core API
  slug: coupa-core-api
  spec_type: OpenAPI
  url: https://compass.coupa.com/en-us/api_docs
billing_model:
  billingCurrency: USD/EUR/GBP
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription (Custom)
description: FOCUS-aligned FinOps for Coupa - enterprise SaaS sold under custom annual contracts that bundle module licenses, user counts, and transaction / spend volume. APIs are included in the platform subscription rather than priced separately. Public per-unit pricing is not disclosed.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Coupa Software Incorporated
  PricingCategory: Subscription
  ProviderName: Coupa
  PublisherName: Coupa Software Incorporated
  ServiceCategory: Business Spend Management
  ServiceName: Coupa
layout: finops
meters:
- aggregation: max
  description: Annual Coupa platform subscription baseline
  dimensions:
  - module
  - region
  name: platform_subscription
  unit: month
- aggregation: max
  description: Per-module licensing (Procurement, Invoicing, Expenses, Pay, Sourcing, CLM, Treasury, Supply Chain Design, Analytics)
  dimensions:
  - module
  - business_unit
  name: module_licensing
  unit: month
- aggregation: max
  description: Named or transactional user seats included in the Coupa contract
  dimensions:
  - role
  - module
  - business_unit
  name: user_seats
  unit: seat
- aggregation: sum
  description: Transactional volume (POs, invoices, expense reports, payment volume) used as a sizing input to the Coupa contract
  dimensions:
  - module
  - business_unit
  - region
  name: transaction_volume
  unit: transaction
- aggregation: max
  description: Active suppliers managed in Coupa, often a sizing input for the Supplier and Procurement modules
  dimensions:
  - business_unit
  - region
  name: supplier_count
  unit: supplier
name: Coupa Finops
provider_name: Coupa
provider_slug: coupa
publisher_name: Coupa Software Incorporated
service_category: Business Spend Management
slug: coupa-finops
source_filename: coupa-finops.yml
source_heading: FinOps Profile
source_url: https://www.coupa.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Coupa\nproviderId: coupa\npublisherName: Coupa Software Incorporated\nserviceCategory: Business Spend Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - BSM\n  - Business Spend Management\n  - Cloud Platform\n  - Enterprise\n  - Financial Management\n  - Procurement\n  - Supply Chain\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Coupa - enterprise SaaS sold under custom annual contracts that\n  bundle module licenses, user counts, and transaction / spend volume. APIs are included in the platform\n  subscription rather than priced separately. Public per-unit pricing is not\
  \ disclosed.\nsources:\n  - https://www.coupa.com/products\n  - https://compass.coupa.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription (Custom)\n  billingFrequency: Annual\n  billingCurrency: USD/EUR/GBP\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Coupa\n  ServiceCategory: Business Spend Management\n  ProviderName: Coupa\n  PublisherName: Coupa Software Incorporated\n  InvoiceIssuerName: Coupa Software Incorporated\n  PricingCategory: Subscription\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: platform_subscription\n    description: Annual Coupa platform subscription baseline\n    unit: month\n    aggregation: max\n    dimensions:\n      - module\n      - region\n  - name: module_licensing\n    description: Per-module licensing (Procurement, Invoicing, Expenses, Pay, Sourcing, CLM, Treasury,\n\
  \      Supply Chain Design, Analytics)\n    unit: month\n    aggregation: max\n    dimensions:\n      - module\n      - business_unit\n  - name: user_seats\n    description: Named or transactional user seats included in the Coupa contract\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n      - module\n      - business_unit\n  - name: transaction_volume\n    description: Transactional volume (POs, invoices, expense reports, payment volume) used as a sizing\n      input to the Coupa contract\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - module\n      - business_unit\n      - region\n  - name: supplier_count\n    description: Active suppliers managed in Coupa, often a sizing input for the Supplier and Procurement\n      modules\n    unit: supplier\n    aggregation: max\n    dimensions:\n      - business_unit\n      - region\nprinciples:\n  - name: Visibility\n    description: Track Coupa platform consumption (transactions, active users, supplier\
  \ counts, integrations)\n      via Coupa Analytics and the Integration / Audit APIs. The same telemetry is the input that drives\n      the next contract renewal sizing.\n  - name: Allocation\n    description: Allocate Coupa cost across business units using the chart-of-accounts and cost-object\n      tags applied to POs, invoices, expense reports, and contracts. Coupa's own spend-classification\n      surface is the natural allocation engine.\n  - name: Optimization\n    description: Right-size module subscriptions against actual module usage; consolidate redundant\n      integration users; use bulk loaders instead of per-record REST calls; renegotiate volume bands\n      against actual transaction volume at renewal; retire low-utilization modules (Treasury, Supply\n      Chain Design) when not actively in use.\n  - name: Accountability\n    description: Assign a Coupa application owner inside finance / procurement; review module utilization\n      and integration health quarterly; tie\
  \ Coupa ROI metrics (cycle-time reduction, captured savings,\n      processed-spend) into FinOps reviews to justify renewal sizing.\nnotes: Coupa does not publish public list pricing. FOCUS columns and meters are modeled around the\n  documented commercial structure (modules, seats, transactions, suppliers); reconciled is false until\n  customer contract terms are referenced directly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coupa/refs/heads/main/finops/coupa-finops.yml
sources:
- https://www.coupa.com/products
- https://compass.coupa.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- BSM
- Business Spend Management
- Cloud Platform
- Enterprise
- Financial Management
- Procurement
- Supply Chain
- FinOps
- Cost Management
- FOCUS
---
