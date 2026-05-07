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
  label: Xceptor REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.xceptor.com/v1/openapi.json
- filename: workflows
  format: yaml
  label: Xceptor Workflow API
  slug: ''
  spec_type: Postman
  url: https://www.postman.com/xceptor/workspace/workflows
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps shape for Xceptor is opaque. The platform is sold via direct enterprise sales with no public price list, usage API, or FOCUS-aligned cost export. Spend is recorded at the platform-subscription level rather than per-API-call.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Xceptor Limited
  ProviderName: Xceptor
  PublisherName: Xceptor Limited
  ServiceCategory: Data Automation Platform
  ServiceName: Xceptor
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  name: platform_subscription
  unit: month
name: Xceptor Finops
provider_name: Xceptor
provider_slug: xceptor
publisher_name: Xceptor Limited
service_category: Data Automation Platform
slug: xceptor-finops
source_filename: xceptor-finops.yml
source_heading: FinOps Profile
source_url: https://www.xceptor.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Xceptor\nproviderId: xceptor\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Data Automation\n  - Document Processing\n  - Financial Services\ndescription: FinOps shape for Xceptor is opaque. The platform is sold via direct enterprise\n  sales with no public price list, usage API, or FOCUS-aligned cost export. Spend is recorded\n  at the platform-subscription level rather than per-API-call.\nsources:\n  - https://www.xceptor.com/\nnotes: Xceptor publishes no pricing or usage-billing documentation. Meters and FOCUS columns\n  reflect a single platform-subscription line until a customer engagement provides the\n  invoice-line detail.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Xceptor Limited\nserviceCategory: Data Automation Platform\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Xceptor\n  ServiceCategory: Data Automation Platform\n  ProviderName: Xceptor\n  PublisherName: Xceptor Limited\n  InvoiceIssuerName: Xceptor Limited\n  BillingCurrency: USD\nmeters:\n  - name: platform_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Visibility into Xceptor consumption is exposed inside the deployed Xceptor\n      tenant via its own pipeline-monitoring tools rather than a vendor-issued usage API.\n  - name: Allocation\n    description: Cost allocates to the business unit that owns the Xceptor subscription;\n      per-pipeline or per-document attribution depends on internal Xceptor reporting.\n  - name: Optimization\n    description: Levers are\
  \ pipeline-design choices (template reuse, batched ingestion,\n      reconciliation rule consolidation) rather than rate or commitment discounts.\n  - name: Accountability\n    description: Subscription is owned by the operations / data-automation team; document-\n      ingestion volume is owned by the upstream business processes that produce documents.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/xceptor/refs/heads/main/finops/xceptor-finops.yml
sources:
- https://www.xceptor.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Automation
- Document Processing
- Financial Services
---
