---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: azure-log-analytics-query-api.yaml
  format: yaml
  label: Azure Log Analytics Query API
  slug: azure-log-analytics-query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-log-analytics/refs/heads/main/openapi/azure-log-analytics-query-api.yaml
- filename: azure-log-analytics-management-api.yaml
  format: yaml
  label: Azure Log Analytics Management API
  slug: azure-log-analytics-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-log-analytics/refs/heads/main/openapi/azure-log-analytics-management-api.yaml
- filename: azure-log-analytics-ingestion-api.yaml
  format: yaml
  label: Azure Log Analytics Ingestion API
  slug: azure-log-analytics-ingestion-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-log-analytics/refs/heads/main/openapi/azure-log-analytics-ingestion-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Azure Log Analytics: per-GB ingest is the dominant meter, with daily-commit tiers, table-tier optimization (Analytics vs Basic vs Auxiliary), retention beyond 31 days, and search/restore from archive as additional billable lines. Ingest tier and table choice are the primary cost levers.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Pay-As-You-Go
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Observability
  ServiceName: Azure Monitor / Log Analytics
layout: finops
meters:
- aggregation: sum
  description: Standard Analytics-tier table ingest
  dimensions:
  - workspace
  - region
  - table
  name: analytics_logs_ingest
  unit: GB
- aggregation: sum
  description: Basic-tier ingest (cheaper, query-restricted)
  dimensions:
  - workspace
  - table
  name: basic_logs_ingest
  unit: GB
- aggregation: sum
  description: Auxiliary-tier ingest (cheapest, archival-only)
  dimensions:
  - workspace
  - table
  name: auxiliary_logs_ingest
  unit: GB
- aggregation: avg
  description: Per-GB-month for retention beyond the included 31 days
  dimensions:
  - workspace
  - table
  name: interactive_retention
  unit: GB-month
- aggregation: avg
  description: Long-term archive storage up to 12 years
  dimensions:
  - workspace
  - table
  name: long_term_archive
  unit: GB-month
- aggregation: sum
  description: Per-GB scanned by Basic/Auxiliary search and archive restore
  dimensions:
  - workspace
  - table
  name: search_scan
  unit: GB
name: Azure Log Analytics Finops
provider_name: Azure Log Analytics
provider_slug: azure-log-analytics
publisher_name: Microsoft Corporation
service_category: Observability
slug: azure-log-analytics-finops
source_filename: azure-log-analytics-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/monitor/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Log Analytics\nproviderId: azure-log-analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Observability\n  - Logs\n  - Monitoring\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Azure Log Analytics: per-GB ingest is the dominant meter, with\n  daily-commit tiers, table-tier optimization (Analytics vs Basic vs Auxiliary), retention beyond 31\n  days, and search/restore from archive as additional billable lines. Ingest tier and table choice are\n  the primary cost levers.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/monitor/\n  - https://learn.microsoft.com/en-us/azure/azure-monitor/logs/cost-logs\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Microsoft Corporation\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Azure Monitor / Log Analytics\n  ServiceCategory: Observability\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Pay-As-You-Go\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: analytics_logs_ingest\n    description: Standard Analytics-tier table ingest\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - workspace\n      - region\n      - table\n  - name: basic_logs_ingest\n    description: Basic-tier ingest (cheaper, query-restricted)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - workspace\n      - table\n  - name: auxiliary_logs_ingest\n    description: Auxiliary-tier\
  \ ingest (cheapest, archival-only)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - workspace\n      - table\n  - name: interactive_retention\n    description: Per-GB-month for retention beyond the included 31 days\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - workspace\n      - table\n  - name: long_term_archive\n    description: Long-term archive storage up to 12 years\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - workspace\n      - table\n  - name: search_scan\n    description: Per-GB scanned by Basic/Auxiliary search and archive restore\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - workspace\n      - table\nprinciples:\n  - name: Visibility\n    description: Use the Usage and Estimated Costs blade in the workspace and Azure Cost Management\n      to see ingest by table and Solutions; build Workbooks for ingest trend by source.\n  - name: Allocation\n    description: Use one workspace per business unit / environment\
  \ for clean attribution; tag workspaces;\n      use Resource Context RBAC and table-level access for chargeback.\n  - name: Optimization\n    description: Move high-volume / low-query tables to Basic or Auxiliary; configure table-level retention;\n      drop noisy fields with ingestion-time transforms; use daily caps; commit to a tier matching steady-state\n      ingest; review verbose diagnostic settings (especially AzureDiagnostics) for waste.\n  - name: Accountability\n    description: Set workspace daily cap alerts; assign workspace owners; review monthly per-table ingest\n      growth; investigate sudden spikes for misconfigured logging.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-log-analytics/refs/heads/main/finops/azure-log-analytics-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/monitor/
- https://learn.microsoft.com/en-us/azure/azure-monitor/logs/cost-logs
specification: FinOps Framework
tags:
- Observability
- Logs
- Monitoring
- FinOps
- FOCUS
---
