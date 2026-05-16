---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: workday-finance-financial-management-openapi.yml
  format: yaml
  label: Workday Financial Management API
  slug: workday-financial-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-finance/refs/heads/main/openapi/workday-finance-financial-management-openapi.yml
- filename: workday-finance-procurement-openapi.yml
  format: yaml
  label: Workday Resource Management API
  slug: workday-resource-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-finance/refs/heads/main/openapi/workday-finance-procurement-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps stub for Workday Finance. The product is sold as a module of a Workday tenant subscription; per-API-call pricing and a public usage API are not exposed, so meters describe contractual entitlement rather than runtime telemetry.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: Financial Management SaaS
  ServiceName: Workday Financial Management
layout: finops
meters:
- aggregation: max
  description: Annual Workday Financial Management module entitlement attached to the tenant subscription.
  dimensions:
  - tenant
  name: financial_management_subscription
  unit: month
- aggregation: max
  description: Licensed user count entitled to the Financial Management module; sized at contract time rather than billed as runtime overage.
  dimensions:
  - tenant
  name: financial_workforce_seats
  unit: seat
name: Workday Finance Finops
provider_name: Workday Finance
provider_slug: workday-finance
publisher_name: Workday, Inc.
service_category: Financial Management SaaS
slug: workday-finance-finops
source_filename: workday-finance-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/enterprise-resource-planning.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Finance\nproviderId: workday-finance\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial Management\n  - Accounting\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for Workday Finance. The product is sold as a module of a Workday tenant subscription; per-API-call pricing and a public usage API are not exposed, so meters describe contractual entitlement rather than runtime telemetry.\nsources:\n  - https://www.workday.com/en-us/enterprise-resource-planning.html\nnotes: No public pricing or billing API exists. Scaffold api_request and compute meters have been removed.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday,\
  \ Inc.\nserviceCategory: Financial Management SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Financial Management\n  ServiceCategory: Financial Management SaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: financial_management_subscription\n    description: Annual Workday Financial Management module entitlement attached to the tenant subscription.\n    unit: month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: financial_workforce_seats\n    description: Licensed user count entitled to the Financial Management module; sized at contract time rather than billed as runtime overage.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Track Workday Finance spend at the contract / module\
  \ level using signed order forms; supplement with internal usage analytics from Workday Reports and Audit Trails to monitor whether the licensed module is actually being used by the finance organization.\n  - name: Allocation\n    description: Allocate the Financial Management module fee to the CFO organization and any subsidiary cost centers consuming the ledger; integrations into Workday from external systems can be charged back to the source system owner.\n  - name: Optimization\n    description: At renewal, right-size licensed seats, retire unused legal entities or business processes, and consolidate satellite accounting tools where Workday Finance can absorb the workload.\n  - name: Accountability\n    description: The Workday Finance owner inside the Office of the CFO should sign off on renewals, module add-ons, and integration scope; review with Workday Customer Success at least annually.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-finance/refs/heads/main/finops/workday-finance-finops.yml
sources:
- https://www.workday.com/en-us/enterprise-resource-planning.html
specification: FinOps Framework
tags:
- Financial Management
- Accounting
- FinOps
- FOCUS
---
