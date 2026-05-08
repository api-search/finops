---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Usage
  pricingCategory: Free Public Data
description: FOCUS-aligned FinOps for Antero Resources data access. The reachable endpoint is SEC EDGAR, which is free public data; there is no charge to reconcile. FinOps practitioners track only the consumer-side compute / egress cost of polling EDGAR, not a vendor invoice from Antero or the SEC.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Not Applicable (free public data)
  ProviderName: U.S. Securities and Exchange Commission
  PublisherName: U.S. Securities and Exchange Commission
  ServiceCategory: Public Filings
  ServiceName: Antero Resources SEC EDGAR Filings
layout: finops
meters:
- aggregation: sum
  description: Count of requests to data.sec.gov for Antero Resources filings (free)
  dimensions:
  - endpoint
  - cik
  - filing_type
  name: edgar_requests
  unit: request
- aggregation: count
  description: Distinct filing artifacts processed downstream
  dimensions:
  - filing_type
  - period
  name: filings_ingested
  unit: filing
name: Antero Resources Finops
provider_name: Antero Resources
provider_slug: antero-resources
publisher_name: U.S. Securities and Exchange Commission (data publisher) / Antero Resources Corporation (filer)
service_category: Public Filings
slug: antero-resources-finops
source_filename: antero-resources-finops.yml
source_heading: FinOps Profile
source_url: https://www.sec.gov/developer
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Antero Resources\nproviderId: antero-resources\npublisherName: U.S. Securities and Exchange Commission (data publisher) / Antero Resources Corporation (filer)\nserviceCategory: Public Filings\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Public Filings\n  - SEC EDGAR\n  - Energy\ndescription: >-\n  FOCUS-aligned FinOps for Antero Resources data access. The reachable\n  endpoint is SEC EDGAR, which is free public data; there is no charge to\n  reconcile. FinOps practitioners track only the consumer-side compute /\n  egress cost of polling EDGAR, not a vendor invoice from Antero or the SEC.\nnotes:\
  \ >-\n  No vendor invoice. Spend is consumer-side infrastructure (egress, storage,\n  ETL).\nsources:\n  - https://www.sec.gov/developer\n  - https://data.sec.gov/submissions/CIK0001433270.json\nbillingModel:\n  pricingCategory: Free Public Data\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Antero Resources SEC EDGAR Filings\n  ServiceCategory: Public Filings\n  ProviderName: U.S. Securities and Exchange Commission\n  PublisherName: U.S. Securities and Exchange Commission\n  InvoiceIssuerName: Not Applicable (free public data)\n  BillingCurrency: USD\nmeters:\n  - name: edgar_requests\n    description: Count of requests to data.sec.gov for Antero Resources filings (free)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - cik\n      - filing_type\n  - name: filings_ingested\n    description: Distinct filing artifacts processed downstream\n    unit: filing\n    aggregation: count\n\
  \    dimensions:\n      - filing_type\n      - period\nprinciples:\n  - name: Visibility\n    description: >-\n      Track EDGAR consumption client-side via consumer logs / metrics, since\n      the SEC does not issue per-account telemetry.\n  - name: Allocation\n    description: >-\n      Allocate consumer-side ETL costs to the team that owns the financial\n      data pipeline ingesting Antero filings.\n  - name: Optimization\n    description: >-\n      Cache filings (immutable once published), poll the submissions index\n      daily rather than per filing type, and respect the 10 req/sec ceiling.\n  - name: Accountability\n    description: >-\n      Data engineering owns the pipeline; finance / research owns the use of\n      the data downstream.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/antero-resources/refs/heads/main/finops/antero-resources-finops.yml
sources:
- https://www.sec.gov/developer
- https://data.sec.gov/submissions/CIK0001433270.json
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Public Filings
- SEC EDGAR
- Energy
---
