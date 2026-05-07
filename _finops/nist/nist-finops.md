---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nist-nvd-cve-openapi.yml
  format: yaml
  label: NIST National Vulnerability Database (NVD) API
  slug: nist-nvd-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nist/refs/heads/main/openapi/nist-nvd-cve-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories: []
  pricingCategory: Free Public Service
description: 'FOCUS-aligned FinOps for NIST: NIST APIs are free public-good services with no commercial billing. The "FinOps" surface is rate-limit budgeting and operational hygiene rather than dollar cost.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: N/A (free)
  PricingCategory: Free
  ProviderName: NIST
  PublisherName: U.S. National Institute of Standards and Technology
  ServiceCategory: Government Data
  ServiceName: NIST Public APIs
  ServiceSubcategory: Vulnerability + Standards Data
layout: finops
meters:
- aggregation: sum
  description: Calls to the NVD REST API (rate-limited, not billed).
  dimensions:
  - api_key
  - endpoint
  name: nvd_api_requests
  unit: request
- aggregation: sum
  description: CVE records ingested via paginated NVD sync.
  dimensions:
  - feed
  name: nvd_records_synced
  unit: record
- aggregation: sum
  description: Calls to NIST Chemistry WebBook API.
  dimensions:
  - dataset
  name: chemistry_webbook_requests
  unit: request
- aggregation: sum
  description: NIST Internet Time Service queries (NTP, daytime).
  dimensions:
  - protocol
  name: time_service_queries
  unit: query
name: Nist Finops
provider_name: National Institute of Standards and Technology (NIST)
provider_slug: nist
publisher_name: U.S. National Institute of Standards and Technology
service_category: Government Open Data
slug: nist-finops
source_filename: nist-finops.yml
source_heading: FinOps Profile
source_url: https://nvd.nist.gov/developers/start-here
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: National Institute of Standards and Technology (NIST)\nproviderId: nist\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Government\n  - Public Data\n  - Cybersecurity\ndescription: 'FOCUS-aligned FinOps for NIST: NIST APIs are free public-good services with no commercial\n  billing. The \"FinOps\" surface is rate-limit budgeting and operational hygiene rather than dollar cost.'\nsources:\n  - https://nvd.nist.gov/developers/start-here\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: U.S. National Institute of Standards and Technology\nserviceCategory: Government Open Data\nbillingModel:\n  pricingCategory: Free Public Service\n\
  \  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: NIST Public APIs\n  ServiceCategory: Government Data\n  ServiceSubcategory: Vulnerability + Standards Data\n  ProviderName: NIST\n  PublisherName: U.S. National Institute of Standards and Technology\n  InvoiceIssuerName: N/A (free)\n  BillingCurrency: USD\n  PricingCategory: Free\nmeters:\n  - name: nvd_api_requests\n    description: Calls to the NVD REST API (rate-limited, not billed).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - endpoint\n  - name: nvd_records_synced\n    description: CVE records ingested via paginated NVD sync.\n    unit: record\n    aggregation: sum\n    dimensions:\n      - feed\n  - name: chemistry_webbook_requests\n    description: Calls to NIST Chemistry WebBook API.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - dataset\n  - name: time_service_queries\n    description: NIST Internet Time Service queries\
  \ (NTP, daytime).\n    unit: query\n    aggregation: sum\n    dimensions:\n      - protocol\nprinciples:\n  - name: Visibility\n    description: Track per-key request counts client-side; NIST does not expose a usage dashboard. Log\n      response codes (200/403) and align to the 30-second rolling window.\n  - name: Allocation\n    description: Issue separate API keys per consuming application or environment so quota usage can\n      be attributed and one team's bug does not starve another.\n  - name: Optimization\n    description: Cache NVD CVE data locally and use lastModStartDate windowed sync; avoid re-fetching\n      static records. Honor the 6-second inter-request sleep to avoid 403s and unnecessary retries.\n  - name: Accountability\n    description: Designate a public-data steward per consuming team responsible for honoring the NIST\n      Terms of Use, key rotation, and uptime against the public quota.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nist/refs/heads/main/finops/nist-finops.yml
sources:
- https://nvd.nist.gov/developers/start-here
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Government
- Public Data
- Cybersecurity
---
