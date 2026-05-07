---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Crystal Reports REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://api.sap.com/crystal/openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: One-Time + Recurring
  pricingCategory: Perpetual License + Maintenance
description: 'FOCUS-aligned FinOps for SAP Crystal Reports: per-named-user desktop license plus server / BI Platform license. Pricing is partner-quoted; APIs are entitlements of the underlying license rather than separately metered.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: SAP SE
  PricingCategory: Perpetual License
  PricingUnit: seat
  ProviderName: SAP
  PublisherName: SAP SE
  ServiceCategory: Business Intelligence
  ServiceName: SAP Crystal Reports
layout: finops
meters:
- aggregation: max
  description: Crystal Reports designer / authoring seats
  dimensions:
  - department
  name: designer_seats
  unit: seat-year
- aggregation: max
  description: BI Platform / Crystal Server named or concurrent user seats
  dimensions:
  - department
  - environment
  name: server_seats
  unit: seat-year
- aggregation: sum
  description: Annual SAP support / maintenance entitlement
  dimensions:
  - product
  name: maintenance_fees
  unit: year
name: Crystal Reports Finops
provider_name: Crystal Reports
provider_slug: crystal-reports
publisher_name: SAP SE
service_category: Business Intelligence
slug: crystal-reports-finops
source_filename: crystal-reports-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com/products/technology-platform/crystal-reports.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Crystal Reports\nproviderId: crystal-reports\npublisherName: SAP SE\nserviceCategory: Business Intelligence\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Business Intelligence\n  - Reporting\n  - SAP\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for SAP Crystal Reports: per-named-user desktop license plus server\n  / BI Platform license. Pricing is partner-quoted; APIs are entitlements of the underlying license rather\n  than separately metered.'\nsources:\n  - https://www.sap.com/products/technology-platform/crystal-reports.html\nnotes: Pricing is not public; reconcile per-seat and per-CPU costs from\
  \ the active SAP partner contract.\nprinciples:\n  - name: Visibility\n    description: Use the SAP BI Platform CMS to inventory deployed Crystal Reports designers and report\n      authors; reconcile against the SAP entitlement portal.\n  - name: Allocation\n    description: Tag report authors and folders by department to attribute Crystal Reports designer and\n      server seat costs.\n  - name: Optimization\n    description: Reclaim dormant designer seats; prefer concurrent-user licensing over named-user when\n      utilization is low; consolidate to BI Platform shared services.\n  - name: Accountability\n    description: BI / data-platform org owns the SAP contract; finance reviews annual maintenance and\n      true-up at SAP renewal.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n      - Budgeting\n  - name: Optimize Usage and Cost\n \
  \   capabilities:\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\nbillingModel:\n  pricingCategory: Perpetual License + Maintenance\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: One-Time + Recurring\nfocusColumns:\n  ServiceName: SAP Crystal Reports\n  ServiceCategory: Business Intelligence\n  ProviderName: SAP\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  PricingCategory: Perpetual License\n  PricingUnit: seat\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: designer_seats\n    description: Crystal Reports designer / authoring seats\n    unit: seat-year\n    aggregation: max\n    dimensions:\n      - department\n  - name: server_seats\n    description: BI Platform / Crystal Server named or concurrent user seats\n    unit: seat-year\n    aggregation: max\n    dimensions:\n      - department\n\
  \      - environment\n  - name: maintenance_fees\n    description: Annual SAP support / maintenance entitlement\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product\napis:\n  - name: Crystal Reports REST API\n    baseURL: https://api.sap.com/crystal/v1\n    tags:\n      - Business Intelligence\n      - Data Visualization\n      - Enterprise\n      - Reports\n    serviceName: Crystal Reports REST API\n    serviceCategory: API\n  - name: Crystal Reports SDK\n    baseURL: https://www.sap.com/sdk/crystal\n    tags:\n      - .NET\n      - Embedding\n      - Java\n      - SDK\n    serviceName: Crystal Reports SDK\n    serviceCategory: API\n  - name: Crystal Reports Server REST API\n    baseURL: https://server:port/biprws\n    tags:\n      - Administration\n      - BI Platform\n      - Report Management\n      - Server\n    serviceName: Crystal Reports Server REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Designer Seat\n    metric: billed_cost / designer_seats\n\
  \    target: TBD\n  - name: Cost per Active Report Author\n    metric: billed_cost / active_authors\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/crystal-reports/refs/heads/main/finops/crystal-reports-finops.yml
sources:
- https://www.sap.com/products/technology-platform/crystal-reports.html
specification: FinOps Framework
tags:
- Business Intelligence
- Reporting
- SAP
- FinOps
- FOCUS
---
