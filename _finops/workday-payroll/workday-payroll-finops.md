---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: workday-payroll-payroll-openapi.yml
  format: yaml
  label: Workday Payroll API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-payroll/refs/heads/main/openapi/workday-payroll-payroll-openapi.yml
- filename: workday-payroll-payroll-results-openapi.yml
  format: yaml
  label: Workday Payroll Results API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-payroll/refs/heads/main/openapi/workday-payroll-payroll-results-openapi.yml
- filename: workday-payroll-payroll-input-openapi.yml
  format: yaml
  label: Workday Payroll Input API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-payroll/refs/heads/main/openapi/workday-payroll-payroll-input-openapi.yml
- filename: workday-payroll-tax-openapi.yml
  format: yaml
  label: Workday Tax API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-payroll/refs/heads/main/openapi/workday-payroll-tax-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps stub for Workday Payroll. Payroll is sold as a Workday tenant module priced per supported country / employee population; per-API-call pricing and a public usage API are not exposed, so meters describe contractual entitlement rather than runtime billing.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: Payroll SaaS
  ServiceName: Workday Payroll
layout: finops
meters:
- aggregation: max
  description: Annual Workday Payroll module entitlement attached to the tenant subscription, scoped by supported country.
  dimensions:
  - tenant
  - country
  name: payroll_module_subscription
  unit: month
- aggregation: max
  description: Count of paid employees serviced by Workday Payroll; sized at contract time and used to scale the module fee at renewal rather than billed as runtime overage.
  dimensions:
  - tenant
  - country
  name: paid_workforce
  unit: employee
name: Workday Payroll Finops
provider_name: Workday Payroll
provider_slug: workday-payroll
publisher_name: Workday, Inc.
service_category: Payroll SaaS
slug: workday-payroll-finops
source_filename: workday-payroll-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/enterprise-resource-planning.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Payroll\nproviderId: workday-payroll\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Payroll\n  - HCM\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for Workday Payroll. Payroll is sold as a Workday tenant module priced per supported country / employee population; per-API-call pricing and a public usage API are not exposed, so meters describe contractual entitlement rather than runtime billing.\nsources:\n  - https://www.workday.com/en-us/enterprise-resource-planning.html\nnotes: No public pricing or billing API exists. Generic api_request and compute_seconds meters from the scaffold have been removed.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Workday, Inc.\nserviceCategory: Payroll SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Payroll\n  ServiceCategory: Payroll SaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: payroll_module_subscription\n    description: Annual Workday Payroll module entitlement attached to the tenant subscription, scoped by supported country.\n    unit: month\n    aggregation: max\n    dimensions:\n      - tenant\n      - country\n  - name: paid_workforce\n    description: Count of paid employees serviced by Workday Payroll; sized at contract time and used to scale the module fee at renewal rather than billed as runtime overage.\n    unit: employee\n    aggregation: max\n    dimensions:\n      - tenant\n      - country\nprinciples:\n  - name: Visibility\n    description:\
  \ Track Workday Payroll spend at the country / module level using signed order forms and Workday-provided pay-run telemetry; reconcile employee counts with the HCM tenant to validate licensed population.\n  - name: Allocation\n    description: Allocate the Payroll module fee to the global payroll function and chargeback to country payroll teams based on serviced headcount; treat Payroll Connect partner fees as a separate line item from the Workday subscription.\n  - name: Optimization\n    description: Right-size country footprint at renewal, retire unused legal entities, and consolidate redundant payroll partners or country-specific outsourced providers where Workday Payroll covers the geography natively.\n  - name: Accountability\n    description: A global payroll lead inside HR / Finance owns the Workday Payroll renewal, reviews country coverage with Workday Customer Success annually, and approves additions or removals of supported countries.\nmaintainers:\n  - FN: Kin Lane\n    email:\
  \ kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-payroll/refs/heads/main/finops/workday-payroll-finops.yml
sources:
- https://www.workday.com/en-us/enterprise-resource-planning.html
specification: FinOps Framework
tags:
- Payroll
- HCM
- FinOps
- FOCUS
---
