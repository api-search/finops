---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sec-edgar-submissions-openapi.yml
  format: yaml
  label: SEC EDGAR Full-Text Search API
  slug: sec-edgar-full-text-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sec-edgar/refs/heads/main/openapi/sec-edgar-submissions-openapi.yml
- filename: sec-edgar-submissions-openapi.yml
  format: yaml
  label: SEC EDGAR Submissions API
  slug: sec-edgar-submissions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sec-edgar/refs/heads/main/openapi/sec-edgar-submissions-openapi.yml
- filename: sec-edgar-submissions-openapi.yml
  format: yaml
  label: SEC EDGAR XBRL Company Facts API
  slug: sec-edgar-xbrl-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sec-edgar/refs/heads/main/openapi/sec-edgar-submissions-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Free / Public Data
description: SEC EDGAR is free U.S. Government public data — there is no provider charge. FinOps focus is therefore on internal cost-to-serve (egress, compute to parse filings, downstream storage) rather than vendor spend. No FOCUS BillingCost line items exist for SEC; meters track operational consumption for showback inside the consuming organization.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: N/A
  ProviderName: U.S. Securities and Exchange Commission
  PublisherName: U.S. Securities and Exchange Commission
  ServiceCategory: Open Government Data
  ServiceName: SEC EDGAR
layout: finops
meters:
- aggregation: sum
  description: Count of HTTP requests sent to SEC EDGAR endpoints (internal observability meter; not billed)
  dimensions:
  - endpoint
  - consumer
  name: edgar_requests
  unit: request
- aggregation: sum
  description: Bytes downloaded from SEC EDGAR (filings, XBRL, search results)
  dimensions:
  - endpoint
  - consumer
  name: edgar_egress_bytes
  unit: GB
- aggregation: sum
  description: Filings or XBRL documents parsed downstream (drives compute / storage cost-to-serve)
  dimensions:
  - form_type
  - consumer
  name: filings_parsed
  unit: document
name: Sec Edgar Finops
provider_name: sec-edgar
provider_slug: sec-edgar
publisher_name: U.S. Securities and Exchange Commission
service_category: Open Government Data
slug: sec-edgar-finops
source_filename: sec-edgar-finops.yml
source_heading: FinOps Profile
source_url: https://www.sec.gov/os/accessing-edgar-data
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SEC EDGAR\nproviderId: sec-edgar\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - SEC\n  - Filings\n  - Regulatory\n  - Open Data\n  - FinOps\n  - FOCUS\ndescription: SEC EDGAR is free U.S. Government public data — there is no provider charge. FinOps focus\n  is therefore on internal cost-to-serve (egress, compute to parse filings, downstream storage) rather\n  than vendor spend. No FOCUS BillingCost line items exist for SEC; meters track operational consumption\n  for showback inside the consuming organization.\nsources:\n  - https://www.sec.gov/os/accessing-edgar-data\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: U.S. Securities and Exchange Commission\n\
  serviceCategory: Open Government Data\nbillingModel:\n  pricingCategory: Free / Public Data\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: SEC EDGAR\n  ServiceCategory: Open Government Data\n  ProviderName: U.S. Securities and Exchange Commission\n  PublisherName: U.S. Securities and Exchange Commission\n  InvoiceIssuerName: N/A\n  BillingCurrency: USD\nmeters:\n  - name: edgar_requests\n    description: Count of HTTP requests sent to SEC EDGAR endpoints (internal observability meter; not\n      billed)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - consumer\n  - name: edgar_egress_bytes\n    description: Bytes downloaded from SEC EDGAR (filings, XBRL, search results)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - consumer\n  - name: filings_parsed\n    description: Filings or XBRL documents parsed downstream (drives compute / storage cost-to-serve)\n\
  \    unit: document\n    aggregation: sum\n    dimensions:\n      - form_type\n      - consumer\nprinciples:\n  - name: Visibility\n    description: SEC EDGAR has no vendor invoice. Track internal usage by capturing the User-Agent in\n      logs, metering request counts and downloaded bytes per consuming team, and reporting these as showback\n      indicators.\n  - name: Allocation\n    description: Allocate downstream storage and compute (for parsing filings, indexing XBRL) to the consuming\n      team via the same User-Agent / consumer-id dimension.\n  - name: Optimization\n    description: Stay under the 10 req/s cap; cache filings locally, use bulk index/ZIP downloads for\n      backfills instead of hitting submissions endpoints, and dedupe by accession number.\n  - name: Accountability\n    description: Engineering owners of the consuming application are accountable for User-Agent compliance\n      and for not getting the source IP blocked by SEC; finance accountability is limited\
  \ to internal\n      cost-to-serve.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sec-edgar/refs/heads/main/finops/sec-edgar-finops.yml
sources:
- https://www.sec.gov/os/accessing-edgar-data
specification: FinOps Framework
tags:
- SEC
- Filings
- Regulatory
- Open Data
- FinOps
- FOCUS
---
