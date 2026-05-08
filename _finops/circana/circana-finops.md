---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: circana-liquid-data.yaml
  format: yaml
  label: Circana Liquid Data API
  slug: liquid-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/circana/refs/heads/main/openapi/circana-liquid-data.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Tax
  pricingCategory: Enterprise Subscription
description: 'FOCUS-aligned FinOps for Circana: enterprise subscription with custom contract economics — fee is shaped by data scope (categories, geographies, panels), seat count, refresh cadence, and integration channel (point API vs Snowflake / BigQuery / Databricks data share). There is no per-API-call price.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Circana, LLC
  PricingCategory: Subscription
  ProviderName: Circana
  PublisherName: Circana, LLC
  ServiceCategory: Market Intelligence / Consumer Data
  ServiceName: Circana Liquid Data / Unify+
layout: finops
meters:
- aggregation: sum
  description: Annual platform subscription line(s) by solution family
  dimensions:
  - solution
  - region
  name: subscription
  unit: year
- aggregation: count
  description: Contracted categories, geographies, and panels
  dimensions:
  - category
  - geography
  - panel
  name: data_scope
  unit: scope
- aggregation: max
  description: User seats provisioned for Unify+ and partner platforms
  dimensions:
  - solution
  - team
  name: seats
  unit: seat
- aggregation: sum
  description: Customer-side warehouse compute used to query Circana data shares (when applicable)
  dimensions:
  - warehouse
  - share
  name: warehouse_compute
  unit: compute-credit
name: Circana Finops
provider_name: Circana
provider_slug: circana
publisher_name: Circana, LLC
service_category: Market Intelligence / Consumer Data
slug: circana-finops
source_filename: circana-finops.yml
source_heading: FinOps Profile
source_url: https://www.circana.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Circana\nproviderId: circana\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Analytics\n  - Business Intelligence\n  - Consumer Data\n  - CPG\n  - Market Research\n  - Retail\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Circana: enterprise subscription with custom contract\n  economics — fee is shaped by data scope (categories, geographies, panels), seat count, refresh\n  cadence, and integration channel (point API vs Snowflake / BigQuery / Databricks data share).\n  There is no per-API-call price.'\nnotes: Circana does not expose a metered usage billing surface. The FinOps shape below describes\n  the enterprise subscription cost surface.\nsources:\n  - https://www.circana.com/\n  - https://www.circana.com/solutions\n  - https://www.circana.com/company/technology\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Circana, LLC\nserviceCategory: Market Intelligence / Consumer Data\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Circana Liquid Data / Unify+\n  ServiceCategory: Market Intelligence / Consumer Data\n  ProviderName: Circana\n  PublisherName: Circana, LLC\n  InvoiceIssuerName: Circana, LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\nmeters:\n  - name: subscription\n    description: Annual platform subscription line(s) by solution family\n    unit: year\n    aggregation: sum\n    dimensions:\n      - solution\n      - region\n  - name: data_scope\n    description: Contracted categories, geographies, and panels\n\
  \    unit: scope\n    aggregation: count\n    dimensions:\n      - category\n      - geography\n      - panel\n  - name: seats\n    description: User seats provisioned for Unify+ and partner platforms\n    unit: seat\n    aggregation: max\n    dimensions:\n      - solution\n      - team\n  - name: warehouse_compute\n    description: Customer-side warehouse compute used to query Circana data shares (when applicable)\n    unit: compute-credit\n    aggregation: sum\n    dimensions:\n      - warehouse\n      - share\nprinciples:\n  - name: Visibility\n    description: Track Circana spend through annual contract line items, seat utilization in Unify+,\n      and warehouse-side query volume for any cloud-share deployments.\n  - name: Allocation\n    description: Allocate Circana subscription cost to the brand, category, or commercial team that\n      drives the analytical demand so insights teams can be P&L'd against decision impact.\n  - name: Optimization\n    description: Right-size data\
  \ scope at renewal (drop unused categories / geographies), prefer\n      cloud-share consumption over point APIs to control warehouse compute, and consolidate seats on\n      shared workspaces where multiple teams co-consume.\n  - name: Accountability\n    description: Insights / analytics owns the demand signal and renewal scope; data engineering\n      owns warehouse cost; finance reconciles annual subscription invoices against utilization\n      evidence at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/circana/refs/heads/main/finops/circana-finops.yml
sources:
- https://www.circana.com/
- https://www.circana.com/solutions
- https://www.circana.com/company/technology
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Consumer Data
- CPG
- Market Research
- Retail
- FinOps
- FOCUS
---
