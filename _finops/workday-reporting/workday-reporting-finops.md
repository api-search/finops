---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: Reporting.yaml
  format: yaml
  label: Workday Report as a Service (RaaS)
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Reporting/v1/Reporting.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps shape for Workday Reporting is opaque. API consumption is included in a negotiated Workday tenant subscription with no published per-request meter or invoice line-item spec. Spend is tracked at the tenant/contract level rather than via FOCUS-style usage records.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: HR / Finance / Analytics SaaS
  ServiceName: Workday Reporting
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  name: tenant_subscription
  unit: month
name: Workday Reporting Finops
provider_name: Workday Reporting
provider_slug: workday-reporting
publisher_name: Workday, Inc.
service_category: HR / Finance / Analytics SaaS
slug: workday-reporting-finops
source_filename: workday-reporting-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/why-workday/about-us/contact-us.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Reporting\nproviderId: workday-reporting\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Reporting\n  - HR Data\ndescription: FinOps shape for Workday Reporting is opaque. API consumption is included in a\n  negotiated Workday tenant subscription with no published per-request meter or invoice line-item\n  spec. Spend is tracked at the tenant/contract level rather than via FOCUS-style usage records.\nsources:\n  - https://www.workday.com/en-us/why-workday/about-us/contact-us.html\n  - https://community.workday.com/api\nnotes: Workday does not publish a usage-billing API or FOCUS-aligned cost export. Meters and\n  charge categories cannot be reconciled without authenticated access to the customer's Workday\n  Community documentation and contract.\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday, Inc.\nserviceCategory: HR / Finance / Analytics SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Reporting\n  ServiceCategory: HR / Finance / Analytics SaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tenant_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: No public usage API. Customers rely on Workday's contract-level reporting and\n      internal Workday Reporting tools to surface integration consumption.\n  - name: Allocation\n    description: Workday spend allocates by tenant and\
  \ product subscription line; per-API or per-\n      consumer-team allocation requires custom integration metadata captured outside Workday.\n  - name: Optimization\n    description: Levers are integration design choices (RaaS over SOAP, WQL batching, Prism dataset\n      consolidation) rather than rate or commitment discounts.\n  - name: Accountability\n    description: Workday subscription is owned by HR/Finance procurement; integration teams own API\n      design choices that influence tenant load.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-reporting/refs/heads/main/finops/workday-reporting-finops.yml
sources:
- https://www.workday.com/en-us/why-workday/about-us/contact-us.html
- https://community.workday.com/api
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Reporting
- HR Data
---
