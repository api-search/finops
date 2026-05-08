---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.json
  format: json
  label: Adobe Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/AdobeDocs/analytics-2.0-apis/main/docs/swagger.json
- filename: adobe-analytics-bulk-data-insertion-api-openapi.yml
  format: yaml
  label: Adobe Analytics Bulk Data Insertion API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-analytics/refs/heads/main/openapi/adobe-analytics-bulk-data-insertion-api-openapi.yml
- filename: adobe-analytics-livestream-asyncapi.yml
  format: yaml
  label: Adobe Analytics Livestream API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-analytics/refs/heads/main/asyncapi/adobe-analytics-livestream-asyncapi.yml
- filename: adobe-analytics-data-repair-api-openapi.yml
  format: yaml
  label: Adobe Analytics Data Repair API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-analytics/refs/heads/main/openapi/adobe-analytics-data-repair-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: 'FOCUS-aligned FinOps shape for Adobe Analytics: enterprise contract licensing keyed to annual server-call commit, Workspace seats, and feature bundle (Select / Prime / Ultimate). API access is included.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Analytics
  ServiceName: Adobe Analytics
layout: finops
meters:
- aggregation: sum
  description: Tracked Adobe Analytics server calls against the annual commit
  dimensions:
  - report_suite
  - environment
  name: server_calls
  unit: server_call
- aggregation: sum
  description: Named Workspace user licenses
  dimensions:
  - role
  name: workspace_seats
  unit: seat-month
- aggregation: sum
  description: Reporting API 2.0 / Bulk Data Insertion / Livestream calls (no incremental charge; tracked for capacity)
  dimensions:
  - api
  - endpoint
  name: api_requests
  unit: request
name: Adobe Analytics Finops
provider_name: Adobe Analytics
provider_slug: adobe-analytics
publisher_name: Adobe Inc.
service_category: Analytics
slug: adobe-analytics-finops
source_filename: adobe-analytics-finops.yml
source_heading: FinOps Profile
source_url: https://business.adobe.com/products/analytics/adobe-analytics.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Analytics\nproviderId: adobe-analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Web Analytics\nnotes: >-\n  Adobe Analytics is contact-sales enterprise SaaS; line-item amounts are\n  contract-specific. FinOps levers focus on server-call commit management,\n  Workspace seat allocation, and unused-SKU consolidation rather than\n  on-demand metering.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe Analytics: enterprise contract\n  licensing keyed to annual server-call commit, Workspace seats, and feature\n  bundle (Select / Prime / Ultimate). API access is included.\nsources:\n  - https://business.adobe.com/products/analytics/adobe-analytics.html\n  - https://developer.adobe.com/analytics-apis/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\nserviceCategory: Analytics\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Adobe Analytics\n  ServiceCategory: Analytics\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: server_calls\n    description: Tracked Adobe Analytics server calls against the annual commit\n    unit: server_call\n    aggregation: sum\n    dimensions:\n      - report_suite\n      - environment\n  - name: workspace_seats\n    description: Named Workspace user licenses\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - role\n  - name: api_requests\n    description: Reporting API 2.0 / Bulk Data Insertion\
  \ / Livestream calls (no incremental charge; tracked for capacity)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Adobe Analytics Admin Console Server Call Usage report and\n      Workspace audit logs to track consumption against the annual commit.\n  - name: Allocation\n    description: >-\n      Allocate server-call cost to product or business unit using report-suite\n      naming conventions and the Workspace audit log.\n  - name: Optimization\n    description: >-\n      Audit unused Workspace seats quarterly; archive low-traffic report\n      suites; deduplicate client / server-side beacon implementations to\n      reduce wasted server calls; right-size the SKU at renewal.\n  - name: Accountability\n    description: >-\n      Adobe TAM and CSM run quarterly business reviews against the contracted\n      server-call commit; finance owns true-up reconciliation at year end.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-analytics/refs/heads/main/finops/adobe-analytics-finops.yml
sources:
- https://business.adobe.com/products/analytics/adobe-analytics.html
- https://developer.adobe.com/analytics-apis/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Web Analytics
---
