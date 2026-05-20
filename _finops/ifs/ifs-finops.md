---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ifs-cloud-erp-openapi.yml
  format: yaml
  label: IFS Cloud ERP API
  slug: ifs-cloud-erp-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ifs/refs/heads/main/openapi/ifs-cloud-erp-openapi.yml
billing_model:
  billingCurrency: USD/EUR/GBP
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Enterprise Subscription
description: FOCUS-aligned FinOps shape for IFS Cloud. Billing is enterprise-subscription with negotiated per-customer terms; APIs are bundled and not separately metered. FinOps practice for IFS focuses on license-and-subscription accountability rather than per-call telemetry.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Industrial and Financial Systems, IFS AB
  PricingCategory: Subscription
  PricingUnit: user-year
  ProviderName: IFS
  PublisherName: Industrial and Financial Systems, IFS AB
  ServiceCategory: Enterprise Software
  ServiceName: IFS Cloud
layout: finops
meters:
- aggregation: max
  description: Named users under license per module
  dimensions:
  - module
  - environment
  name: named_users
  unit: user-month
- aggregation: max
  description: Active IFS Cloud environments (production, test, development)
  dimensions:
  - environment_type
  - region
  name: environments
  unit: environment-month
- aggregation: max
  description: Licensed product modules
  dimensions:
  - product_line
  name: modules
  unit: module
name: Ifs Finops
provider_name: IFS
provider_slug: ifs
publisher_name: Industrial and Financial Systems, IFS AB
service_category: Enterprise Software
slug: ifs-finops
source_filename: ifs-finops.yml
source_heading: FinOps Profile
source_url: https://www.ifs.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: IFS\nproviderId: ifs\npublisherName: Industrial and Financial Systems, IFS AB\nserviceCategory: Enterprise Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - ERP\n  - EAM\n  - Field Service\n  - Enterprise Service Management\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for IFS Cloud. Billing is enterprise-subscription with negotiated\n  per-customer terms; APIs are bundled and not separately metered. FinOps practice for IFS focuses on\n  license-and-subscription accountability rather than per-call telemetry.\nnotes: No public usage-based meters; treat invoiced subscription cost and module utilization\
  \ as the primary\n  meters. Reconcile with the customer's own IFS Cloud Lifecycle Experience reporting.\nsources:\n  - https://www.ifs.com/\n  - https://www.ifs.com/products/cloud\nprinciples:\n  - name: Visibility\n    description: Surface IFS Cloud subscription costs in finance reporting; use IFS Lifecycle Experience\n      for module and environment usage telemetry.\n  - name: Allocation\n    description: Allocate the IFS subscription across business units by module entitlement, named user\n      counts, and active environments (production / test / development).\n  - name: Optimization\n    description: Right-size named-user counts, retire unused environments at renewal, and consolidate\n      modules where overlap exists between EAM, FSM, and ESM.\n  - name: Accountability\n    description: Designate an IFS application owner with a single annual budget line; review module and\n      user utilization quarterly with the IFS Customer Success Manager.\ndomains:\n  - name: Understand Usage\
  \ and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n      - Benchmarking\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD/EUR/GBP\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: IFS Cloud\n  ServiceCategory: Enterprise Software\n  ProviderName: IFS\n  PublisherName: Industrial and Financial Systems, IFS AB\n  InvoiceIssuerName: Industrial and Financial Systems, IFS AB\n  PricingCategory: Subscription\n  PricingUnit: user-year\n  BillingCurrency: USD\n  ChargeCategory:\
  \ Purchase\nmeters:\n  - name: named_users\n    description: Named users under license per module\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - module\n      - environment\n  - name: environments\n    description: Active IFS Cloud environments (production, test, development)\n    unit: environment-month\n    aggregation: max\n    dimensions:\n      - environment_type\n      - region\n  - name: modules\n    description: Licensed product modules\n    unit: module\n    aggregation: max\n    dimensions:\n      - product_line\napis:\n  - name: IFS Cloud ERP API\n    baseURL: https://api.ifs.com\n    tags:\n      - Cloud\n      - ERP\n      - Finance\n      - Manufacturing\n      - Supply Chain\n    serviceName: IFS Cloud ERP API\n    serviceCategory: API\n  - name: IFS Field Service Management API\n    baseURL: https://api.ifs.com\n    tags:\n      - Asset Management\n      - Field Service\n      - Mobile\n      - Scheduling\n      - Work Order\n    serviceName: IFS\
  \ Field Service Management API\n    serviceCategory: API\n  - name: IFS Enterprise Asset Management API\n    baseURL: https://api.ifs.com\n    tags:\n      - Asset Management\n      - EAM\n      - Energy\n      - Maintenance\n      - Manufacturing\n    serviceName: IFS Enterprise Asset Management API\n    serviceCategory: API\n  - name: IFS Enterprise Service Management API\n    baseURL: https://api.ifs.com\n    tags:\n      - Cloud\n      - Helpdesk\n      - ITSM\n      - Service Management\n    serviceName: IFS Enterprise Service Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Named User\n    metric: billed_cost / named_users\n    target: TBD\n  - name: Cost per Active Environment\n    metric: billed_cost / environments\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ifs/refs/heads/main/finops/ifs-finops.yml
sources:
- https://www.ifs.com/
- https://www.ifs.com/products/cloud
specification: FinOps Framework
tags:
- ERP
- EAM
- Field Service
- Enterprise Service Management
- FinOps
- FOCUS
---
