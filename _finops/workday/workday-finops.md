---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hcm.yml
  format: yaml
  label: Workday HCM API
  slug: hcm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/hcm.yml
- filename: financialManagement.yml
  format: yaml
  label: Workday Financial Management API
  slug: financial-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/financialManagement.yml
- filename: recruiting.yml
  format: yaml
  label: Workday Recruiting API
  slug: recruiting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/recruiting.yml
- filename: timeTracking.yml
  format: yaml
  label: Workday Time Tracking API
  slug: time-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/timeTracking.yml
- filename: benefits.yml
  format: yaml
  label: Workday Benefits API
  slug: benefits-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/benefits.yml
- filename: absenceManagement.yml
  format: yaml
  label: Workday Absence Management API
  slug: absence-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/absenceManagement.yml
- filename: compensation.yml
  format: yaml
  label: Workday Compensation API
  slug: compensation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/compensation.yml
- filename: payroll.yml
  format: yaml
  label: Workday Payroll API
  slug: payroll-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/payroll.yml
- filename: person.yml
  format: yaml
  label: Workday Person API
  slug: person-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/person.yml
- filename: performanceManagement.yml
  format: yaml
  label: Workday Performance Management API
  slug: performance-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/performanceManagement.yml
- filename: talent.yml
  format: yaml
  label: Workday Talent Management API
  slug: talent-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/talent.yml
- filename: common.yml
  format: yaml
  label: Workday Common API
  slug: common-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/common.yml
- filename: staffing.yml
  format: yaml
  label: Workday Staffing API
  slug: staffing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/staffing.yml
- filename: prismAnalytics.yml
  format: yaml
  label: Workday Prism Analytics API
  slug: prism-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/prismAnalytics.yml
- filename: raas.yml
  format: yaml
  label: Workday Report-as-a-Service API
  slug: raas-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/raas.yml
- filename: wql.yml
  format: yaml
  label: Workday WQL API
  slug: wql-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/wql.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps stub for Workday's enterprise SaaS platform. Workday is sold as a multi-year per-customer subscription quoted by sales; per-API-call pricing and a self-serve usage API are not published, so meters and invoice line items here describe the contractual shape rather than runtime telemetry.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: Enterprise SaaS
  ServiceName: Workday
layout: finops
meters:
- aggregation: max
  description: Negotiated annual subscription for the Workday tenant covering HCM, Financial Management, and platform modules included in the contract.
  dimensions:
  - tenant
  - module
  name: tenant_subscription
  unit: month
- aggregation: max
  description: Licensed workforce count used to size the Workday subscription; included in the negotiated price rather than billed as overage.
  dimensions:
  - tenant
  - module
  name: workforce_seats
  unit: seat
name: Workday Finops
provider_name: Workday
provider_slug: workday
publisher_name: Workday, Inc.
service_category: Enterprise SaaS
slug: workday-finops
source_filename: workday-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/enterprise-resource-planning.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday\nproviderId: workday\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Enterprise Software\n  - HCM\n  - ERP\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for Workday's enterprise SaaS platform. Workday is sold as a multi-year per-customer subscription quoted by sales; per-API-call pricing and a self-serve usage API are not published, so meters and invoice line items here describe the contractual shape rather than runtime telemetry.\nsources:\n  - https://www.workday.com/en-us/enterprise-resource-planning.html\nnotes: Workday does not publish a public usage/billing API. Generic api_request / data_egress / compute_seconds meters from the scaffold have been removed; remaining meters describe the negotiated subscription shape.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday, Inc.\nserviceCategory: Enterprise SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday\n  ServiceCategory: Enterprise SaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tenant_subscription\n    description: Negotiated annual subscription for the Workday tenant covering HCM, Financial Management, and platform modules included in the contract.\n    unit: month\n    aggregation: max\n    dimensions:\n      - tenant\n      - module\n  - name: workforce_seats\n    description: Licensed workforce count used to size the Workday subscription; included in the negotiated price rather than billed as overage.\n    unit: seat\n    aggregation: max\n\
  \    dimensions:\n      - tenant\n      - module\nprinciples:\n  - name: Visibility\n    description: Treat Workday spend as a contract-level line item; reconcile against signed order forms and renewal worksheets rather than a usage API. Use the Workday tenant audit reports and Tenant Health dashboards to track entitlement consumption (modules deployed, integrations live).\n  - name: Allocation\n    description: Allocate the Workday subscription across HR, Finance, and IT cost centers based on the modules each function uses; integrations and Extend apps can be tagged at the project level for chargeback against the platform fee.\n  - name: Optimization\n    description: Optimize at renewal by right-sizing licensed workforce counts, retiring unused modules, consolidating sandbox tenants, and avoiding low-value Extend / Integration Cloud add-ons; tactical optimization at runtime is limited because pricing is not metered.\n  - name: Accountability\n    description: Designate a Workday HRIS\
  \ / ERP owner who reviews module utilization quarterly with Workday's Customer Success team and signs off on renewals, true-ups, and add-on SKUs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/finops/workday-finops.yml
sources:
- https://www.workday.com/en-us/enterprise-resource-planning.html
specification: FinOps Framework
tags:
- Enterprise Software
- HCM
- ERP
- FinOps
- FOCUS
---
