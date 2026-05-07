---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: Financial_Management.json
  format: json
  label: Workday Financial Management API
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Financial_Management/v38.2/Financial_Management.json
- filename: Revenue_Management.json
  format: json
  label: Workday Revenue Management API
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Revenue_Management/v38.2/Revenue_Management.json
- filename: Expenses.json
  format: json
  label: Workday Expenses API
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Expenses/v38.2/Expenses.json
- filename: Resource_Management.json
  format: json
  label: Workday Procurement API
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Resource_Management/v38.2/Resource_Management.json
- filename: Cash_Management.json
  format: json
  label: Workday Cash Management API
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Cash_Management/v38.2/Cash_Management.json
- filename: Financial_Management.json
  format: json
  label: Workday Financial Accounting API
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Financial_Management/v38.2/Financial_Management.json
- filename: Report_as_a_Service.json
  format: json
  label: Workday Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Report_as_a_Service/v38.2/Report_as_a_Service.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps stub for Workday Financials. The product is sold as a module of a Workday tenant subscription; per-API-call pricing and a public usage API are not exposed, so meters describe contractual entitlement rather than runtime telemetry.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: Cloud ERP
  ServiceName: Workday Financials
layout: finops
meters:
- aggregation: max
  description: Annual Workday Financials module entitlement attached to the tenant subscription.
  dimensions:
  - tenant
  name: financials_module_subscription
  unit: month
- aggregation: max
  description: Licensed user count entitled to the Workday Financials module, sized at contract time.
  dimensions:
  - tenant
  name: financials_workforce_seats
  unit: seat
name: Workday Financials Finops
provider_name: Workday Financials
provider_slug: workday-financials
publisher_name: Workday, Inc.
service_category: Cloud ERP
slug: workday-financials-finops
source_filename: workday-financials-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/enterprise-resource-planning.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Financials\nproviderId: workday-financials\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud ERP\n  - Financial Management\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for Workday Financials. The product is sold as a module of a Workday tenant subscription; per-API-call pricing and a public usage API are not exposed, so meters describe contractual entitlement rather than runtime telemetry.\nsources:\n  - https://www.workday.com/en-us/enterprise-resource-planning.html\nnotes: No public pricing or billing API exists. Generic api_request and compute meters from the scaffold have been removed.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Workday, Inc.\nserviceCategory: Cloud ERP\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Financials\n  ServiceCategory: Cloud ERP\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: financials_module_subscription\n    description: Annual Workday Financials module entitlement attached to the tenant subscription.\n    unit: month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: financials_workforce_seats\n    description: Licensed user count entitled to the Workday Financials module, sized at contract time.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Track Workday Financials spend at the contract / module level via signed order forms; complement with Workday Reports and\
  \ Audit Trails to confirm finance organizations are actively using the licensed module.\n  - name: Allocation\n    description: Allocate the Workday Financials fee to the CFO organization and any subsidiary entities consuming the general ledger; charge integration build-out back to the source-system owner.\n  - name: Optimization\n    description: At renewal, retire unused legal entities, retire unused dimensions, and consolidate satellite accounting tools where Workday Financials can absorb the workload.\n  - name: Accountability\n    description: The Workday Financials owner inside the Office of the CFO signs off on renewals and integration scope; review utilization with Workday Customer Success annually.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-financials/refs/heads/main/finops/workday-financials-finops.yml
sources:
- https://www.workday.com/en-us/enterprise-resource-planning.html
specification: FinOps Framework
tags:
- Cloud ERP
- Financial Management
- FinOps
- FOCUS
---
