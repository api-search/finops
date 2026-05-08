---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel People API
  slug: deel-people-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Organizations API
  slug: deel-organizations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Contracts API
  slug: deel-contracts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Time Off API
  slug: deel-time-off-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Time Tracking API
  slug: deel-time-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Payroll API
  slug: deel-payroll-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Invoices API
  slug: deel-invoices-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Expenses API
  slug: deel-expenses-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel EOR API
  slug: deel-eor-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Background Checks API
  slug: deel-background-checks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Immigration API
  slug: deel-immigration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel IT API
  slug: deel-it-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel SCIM API
  slug: deel-scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel ATS API
  slug: deel-ats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Accounting API
  slug: deel-accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Lookups API
  slug: deel-lookups-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Webhooks API
  slug: deel-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel OAuth & Apps API
  slug: deel-oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel MCP Server
  slug: deel-mcp-server
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Tax
  pricingCategory: Subscription Per Seat
description: Deel's commercial billing model is predominantly per-worker-month pricing across Contractor, EOR, US PEO, Global/US Payroll, Deel HR, and Deel IT product lines, with pass-through costs for benefits, immigration, and recruitment events. This artifact maps Deel charges to FOCUS columns for FinOps allocation and reporting.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Deel
  ProviderName: Deel
  PublisherName: Deel
  ServiceCategory: HR
  ServiceName: Deel
layout: finops
meters:
- aggregation: sum
  description: Active contractors managed under Deel Contractor or CoR plans.
  dimensions:
  - legal_entity
  - country
  - cost_center
  name: contractor_seats
  unit: contractor-month
- aggregation: sum
  description: Active EOR employees billed at Standard or Enterprise tier.
  dimensions:
  - country
  - tier
  - cost_center
  name: eor_seats
  unit: employee-month
- aggregation: sum
  description: Active US PEO co-employees.
  dimensions:
  - state
  - cost_center
  name: us_peo_seats
  unit: employee-month
- aggregation: sum
  description: Active employees on Deel Global or US managed payroll.
  dimensions:
  - country
  - cost_center
  name: managed_payroll_seats
  unit: employee-month
- aggregation: sum
  description: Active employees with Deel HR Core / Recruit / Develop / Full bundles.
  dimensions:
  - module
  - cost_center
  name: hr_module_seats
  unit: employee-month
- aggregation: sum
  description: Active users on Deel IT plans (Platform / Starter / Growth / Scale).
  dimensions:
  - tier
  - cost_center
  name: it_seats
  unit: user-month
- aggregation: sum
  description: MDM, endpoint protection, and device lifecycle management add-ons.
  dimensions:
  - service
  - cost_center
  name: device_management
  unit: device-month
- aggregation: count
  description: One-time recruitment fees for sourced hires.
  dimensions:
  - role
  - country
  name: per_hire_fees
  unit: hires
- aggregation: sum
  description: Benefits premiums, immigration filings, background checks, and equipment costs.
  dimensions:
  - service
  - country
  name: pass_through_costs
  unit: events
name: Deel Finops
provider_name: Deel
provider_slug: deel
publisher_name: Deel
service_category: HR
slug: deel-finops
source_filename: deel-finops.yml
source_heading: FinOps Profile
source_url: https://www.deel.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Deel\nproviderId: deel\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - HR\n  - Payroll\n  - Global Hiring\n  - EOR\n  - Contractors\n  - FinOps\n  - FOCUS\ndescription: >-\n  Deel's commercial billing model is predominantly per-worker-month pricing\n  across Contractor, EOR, US PEO, Global/US Payroll, Deel HR, and Deel IT\n  product lines, with pass-through costs for benefits, immigration, and\n  recruitment events. This artifact maps Deel charges to FOCUS columns for\n  FinOps allocation and reporting.\nsources:\n  - https://www.deel.com/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Deel\nserviceCategory: HR\nbillingModel:\n  pricingCategory: Subscription Per Seat\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Deel\n  ServiceCategory: HR\n  ProviderName: Deel\n  PublisherName: Deel\n  InvoiceIssuerName: Deel\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: contractor_seats\n    description: Active contractors managed under Deel Contractor or CoR plans.\n    unit: contractor-month\n    aggregation: sum\n    dimensions:\n      - legal_entity\n      - country\n      - cost_center\n  - name: eor_seats\n    description: Active EOR employees billed at Standard or Enterprise tier.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - country\n      - tier\n      - cost_center\n  - name: us_peo_seats\n    description: Active US PEO co-employees.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n     \
  \ - state\n      - cost_center\n  - name: managed_payroll_seats\n    description: Active employees on Deel Global or US managed payroll.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - country\n      - cost_center\n  - name: hr_module_seats\n    description: Active employees with Deel HR Core / Recruit / Develop / Full bundles.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - module\n      - cost_center\n  - name: it_seats\n    description: Active users on Deel IT plans (Platform / Starter / Growth / Scale).\n    unit: user-month\n    aggregation: sum\n    dimensions:\n      - tier\n      - cost_center\n  - name: device_management\n    description: MDM, endpoint protection, and device lifecycle management add-ons.\n    unit: device-month\n    aggregation: sum\n    dimensions:\n      - service\n      - cost_center\n  - name: per_hire_fees\n    description: One-time recruitment fees for sourced hires.\n    unit: hires\n    aggregation: count\n\
  \    dimensions:\n      - role\n      - country\n  - name: pass_through_costs\n    description: Benefits premiums, immigration filings, background checks, and equipment costs.\n    unit: events\n    aggregation: sum\n    dimensions:\n      - service\n      - country\nprinciples:\n  - name: Visibility\n    description: >-\n      Pull Deel monthly invoices and usage exports; tag invoice line items by\n      legal entity, country, and cost center for attribution.\n  - name: Allocation\n    description: >-\n      Allocate per-seat charges to consuming business units via cost-center\n      tags; allocate pass-through costs (benefits, immigration) to the worker\n      and team.\n  - name: Optimization\n    description: >-\n      Audit headcount monthly to remove inactive contractors and right-size\n      EOR vs. local entity vs. CoR options; consolidate HR module bundles.\n  - name: Accountability\n    description: >-\n      Assign a Deel contract owner; review billing against negotiated terms,\n\
  \      especially Enterprise EOR thresholds and bundle discounts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/finops/deel-finops.yml
sources:
- https://www.deel.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- HR
- Payroll
- Global Hiring
- EOR
- Contractors
- FinOps
- FOCUS
---
