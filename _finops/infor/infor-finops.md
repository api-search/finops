---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: infor-ion-api-gateway-openapi.yml
  format: yaml
  label: Infor ION API Gateway
  slug: infor-ion-api-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/infor/refs/heads/main/openapi/infor-ion-api-gateway-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Enterprise Subscription
description: FOCUS-aligned FinOps shape for Infor. Billing is enterprise subscription with negotiated per-customer terms; APIs are bundled into Infor OS / ION rather than separately metered. FinOps practice for Infor focuses on subscription accountability, environment / module right-sizing at renewal, and named-user hygiene.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Infor, Inc.
  PricingCategory: Subscription
  PricingUnit: user-year
  ProviderName: Infor
  PublisherName: Infor, Inc.
  ServiceCategory: Enterprise Software
  ServiceName: Infor CloudSuite
layout: finops
meters:
- aggregation: max
  description: Named users licensed per module
  dimensions:
  - module
  - environment
  name: named_users
  unit: user-month
- aggregation: max
  description: Active CloudSuite environments (production, test, development)
  dimensions:
  - environment_type
  - region
  name: environments
  unit: environment-month
- aggregation: sum
  description: Document flows processed through Infor ION
  dimensions:
  - flow
  - source_app
  - target_app
  name: ion_documents
  unit: document
name: Infor Finops
provider_name: Infor
provider_slug: infor
publisher_name: Infor, Inc.
service_category: Enterprise Software
slug: infor-finops
source_filename: infor-finops.yml
source_heading: FinOps Profile
source_url: https://www.infor.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Infor\nproviderId: infor\npublisherName: Infor, Inc.\nserviceCategory: Enterprise Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - ERP\n  - CloudSuite\n  - Industry Cloud\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Infor. Billing is enterprise subscription with negotiated\n  per-customer terms; APIs are bundled into Infor OS / ION rather than separately metered. FinOps practice\n  for Infor focuses on subscription accountability, environment / module right-sizing at renewal, and\n  named-user hygiene.\nnotes: No public usage-based meters. Reconcile against the customer's own Infor invoice\
  \ and Infor OS\n  utilization telemetry.\nsources:\n  - https://www.infor.com/products\n  - https://www.infor.com/contact-us\nprinciples:\n  - name: Visibility\n    description: Use Infor OS Homepages and ION monitoring to see API and document-flow utilization;\n      surface annual subscription costs in finance reporting.\n  - name: Allocation\n    description: Allocate the Infor subscription across business units by module entitlement, named-user\n      counts, and active environments (production / test / development).\n  - name: Optimization\n    description: Right-size named-user counts at renewal, retire unused environments and modules, consolidate\n      ION integrations to reduce shared-services pressure.\n  - name: Accountability\n    description: Designate an Infor application owner with a single annual budget line; review module\n      and user utilization quarterly with the Infor Customer Success Manager.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n  \
  \    - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n      - Benchmarking\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Infor CloudSuite\n  ServiceCategory: Enterprise Software\n  ProviderName: Infor\n  PublisherName: Infor, Inc.\n  InvoiceIssuerName: Infor, Inc.\n  PricingCategory: Subscription\n  PricingUnit: user-year\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: named_users\n    description: Named users licensed\
  \ per module\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - module\n      - environment\n  - name: environments\n    description: Active CloudSuite environments (production, test, development)\n    unit: environment-month\n    aggregation: max\n    dimensions:\n      - environment_type\n      - region\n  - name: ion_documents\n    description: Document flows processed through Infor ION\n    unit: document\n    aggregation: sum\n    dimensions:\n      - flow\n      - source_app\n      - target_app\napis:\n  - name: Infor ION API\n    baseURL: https://mingle-ionapi.{region}.inforcloudsuite.com\n    serviceCategory: API\n  - name: Infor CloudSuite APIs\n    baseURL: https://mingle-ionapi.{region}.inforcloudsuite.com\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Named User\n    metric: billed_cost / named_users\n    target: TBD\n  - name: Cost per Active Environment\n    metric: billed_cost / environments\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n\
  \    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/infor/refs/heads/main/finops/infor-finops.yml
sources:
- https://www.infor.com/products
- https://www.infor.com/contact-us
specification: FinOps Framework
tags:
- ERP
- CloudSuite
- Industry Cloud
- FinOps
- FOCUS
---
