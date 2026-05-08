---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for H.B. Fuller: enterprise / partner API access bundled into a commercial agreement, not metered as a standalone SaaS line. Meters describe partner-integration volume rather than billable units.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: H.B. Fuller Company
  PricingCategory: Subscription
  PricingUnit: partner-agreement
  ProviderName: H.B. Fuller Company
  PublisherName: H.B. Fuller Company
  ServiceCategory: Industrial / Manufacturer Partner API
  ServiceName: H.B. Fuller Company API
layout: finops
meters:
- aggregation: sum
  description: Partner-integration request volume (allocation meter)
  dimensions:
  - partner
  - endpoint
  - business_unit
  name: api_requests
  unit: request
- aggregation: sum
  description: Order-related transactions submitted via the API
  dimensions:
  - partner
  - product_line
  name: orders_submitted
  unit: order
name: H B Fuller Finops
provider_name: H.B. Fuller Company
provider_slug: h-b-fuller
publisher_name: H.B. Fuller Company
service_category: Industrial / Manufacturer Partner API
slug: h-b-fuller-finops
source_filename: h-b-fuller-finops.yml
source_heading: FinOps Profile
source_url: https://www.hbfuller.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: H.B. Fuller Company\nproviderId: h-b-fuller\npublisherName: H.B. Fuller Company\nserviceCategory: Industrial / Manufacturer Partner API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Adhesives\n  - Sealants\n  - Chemical\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for H.B. Fuller: enterprise / partner API access\n  bundled into a commercial agreement, not metered as a standalone SaaS line. Meters describe\n  partner-integration volume rather than billable units.'\nnotes: No public commercial model is published. The shape below treats API consumption as a\n  partner-allocation\
  \ surface; replace meters when a billable model is documented.\nsources:\n  - https://www.hbfuller.com/\nprinciples:\n  - name: Visibility\n    description: Track partner-integration volume via the H.B. Fuller partner gateway logs and\n      reconcile against the partner agreement.\n  - name: Allocation\n    description: Allocate integration cost across business units (packaging, hygiene, engineering\n      adhesives, construction) using the calling partner system.\n  - name: Optimization\n    description: Cache product / SDS / availability lookups; batch order-status polls; consolidate\n      partner integrations through a single gateway.\n  - name: Accountability\n    description: Assign a partner-program owner; review API usage quarterly against contract terms.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n\
  \      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: H.B. Fuller Company API\n  ServiceCategory: Industrial / Manufacturer Partner API\n  ProviderName: H.B. Fuller Company\n  PublisherName: H.B. Fuller Company\n  InvoiceIssuerName: H.B. Fuller Company\n  PricingCategory: Subscription\n\
  \  PricingUnit: partner-agreement\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_requests\n    description: Partner-integration request volume (allocation meter)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - endpoint\n      - business_unit\n  - name: orders_submitted\n    description: Order-related transactions submitted via the API\n    unit: order\n    aggregation: sum\n    dimensions:\n      - partner\n      - product_line\napis:\n  - name: H.B. Fuller Company API\n    baseURL: https://api.hbfuller.com\n    tags:\n      - Adhesives\n      - Sealants\n      - Chemical\n    serviceName: H.B. Fuller Company API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Partner Integration\n    metric: billed_cost / active_partners\n    target: TBD\n  - name: Cost per Order Transaction\n    metric: billed_cost / orders_submitted\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/h-b-fuller/refs/heads/main/finops/h-b-fuller-finops.yml
sources:
- https://www.hbfuller.com/
specification: FinOps Framework
tags:
- Adhesives
- Sealants
- Chemical
- FinOps
- Cost Management
- FOCUS
---
