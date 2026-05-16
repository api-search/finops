---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: workday-report-writer-raas-openapi.yml
  format: yaml
  label: Workday Report-as-a-Service (RaaS) REST API
  slug: workday-report-as-a-service-raas-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-report-writer/refs/heads/main/openapi/workday-report-writer-raas-openapi.yml
- filename: workday-report-writer-wql-openapi.yml
  format: yaml
  label: Workday WQL API
  slug: workday-wql-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-report-writer/refs/heads/main/openapi/workday-report-writer-wql-openapi.yml
- filename: workday-report-writer-prism-analytics-openapi.yml
  format: yaml
  label: Workday Prism Analytics API
  slug: workday-prism-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-report-writer/refs/heads/main/openapi/workday-report-writer-prism-analytics-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps stub for Workday Report Writer. Report Writer is included in the Workday tenant subscription and is not separately metered or invoiced; meters here describe operational footprint rather than billable units.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: Reporting / Analytics
  ServiceName: Workday Report Writer
layout: finops
meters:
- aggregation: max
  description: Report Writer is bundled into the Workday tenant subscription rather than separately metered; this meter records that the capability is entitled with the tenant.
  dimensions:
  - tenant
  name: report_writer_capability
  unit: month
- aggregation: max
  description: Count of custom Report Writer reports published in the tenant; tracked for governance rather than billing.
  dimensions:
  - tenant
  - business_area
  name: published_reports
  unit: report
name: Workday Report Writer Finops
provider_name: Workday Report Writer
provider_slug: workday-report-writer
publisher_name: Workday, Inc.
service_category: Reporting / Analytics
slug: workday-report-writer-finops
source_filename: workday-report-writer-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/enterprise-resource-planning.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Report Writer\nproviderId: workday-report-writer\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Reporting\n  - Analytics\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for Workday Report Writer. Report Writer is included in the Workday tenant subscription and is not separately metered or invoiced; meters here describe operational footprint rather than billable units.\nsources:\n  - https://www.workday.com/en-us/enterprise-resource-planning.html\nnotes: Report Writer has no separate price. Generic api_request and compute_seconds meters from the scaffold have been removed.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday,\
  \ Inc.\nserviceCategory: Reporting / Analytics\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Report Writer\n  ServiceCategory: Reporting / Analytics\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: report_writer_capability\n    description: Report Writer is bundled into the Workday tenant subscription rather than separately metered; this meter records that the capability is entitled with the tenant.\n    unit: month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: published_reports\n    description: Count of custom Report Writer reports published in the tenant; tracked for governance rather than billing.\n    unit: report\n    aggregation: max\n    dimensions:\n      - tenant\n      - business_area\nprinciples:\n  - name: Visibility\n    description: Track\
  \ Report Writer usage through Workday's report catalog and the tenant's report execution telemetry; there is no separate invoice line, so visibility is operational rather than financial.\n  - name: Allocation\n    description: Allocate the cost of report-development work (not the platform capability, which is bundled) to the requesting business area; treat heavy report consumers as a tag for chargeback against the broader Workday subscription.\n  - name: Optimization\n    description: Retire stale or duplicate custom reports, prefer delivered reports over custom Report Writer where they fit, and route large extracts through scheduled background processes to avoid contention with interactive tenant traffic.\n  - name: Accountability\n    description: A reporting / analytics lead inside the Workday Center of Excellence governs the report catalog, publishes naming and review standards, and represents reporting workload at Workday tenant-health reviews.\nmaintainers:\n  - FN: Kin Lane\n  \
  \  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-report-writer/refs/heads/main/finops/workday-report-writer-finops.yml
sources:
- https://www.workday.com/en-us/enterprise-resource-planning.html
specification: FinOps Framework
tags:
- Reporting
- Analytics
- FinOps
- FOCUS
---
