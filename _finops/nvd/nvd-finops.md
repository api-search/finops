---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nvd-cve-openapi.yml
  format: yaml
  label: NVD CVE API
  slug: nvd-cve
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nvd/refs/heads/main/openapi/nvd-cve-openapi.yml
- filename: nvd-cve-openapi.yml
  format: yaml
  label: NVD CVE Change History API
  slug: nvd-cve-history
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nvd/refs/heads/main/openapi/nvd-cve-openapi.yml
- filename: nvd-cve-openapi.yml
  format: yaml
  label: NVD CPE API
  slug: nvd-cpe
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nvd/refs/heads/main/openapi/nvd-cve-openapi.yml
- filename: nvd-cve-openapi.yml
  format: yaml
  label: NVD CPE Match Criteria API
  slug: nvd-cpe-match
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nvd/refs/heads/main/openapi/nvd-cve-openapi.yml
- filename: nvd-cve-openapi.yml
  format: yaml
  label: NVD Source API
  slug: nvd-source
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nvd/refs/heads/main/openapi/nvd-cve-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories:
  - Usage
  chargeFrequency: None
  pricingCategory: Free / Public Service
description: 'FOCUS-aligned FinOps for the National Vulnerability Database: APIs are free of charge from NIST. Cost optimization is about request efficiency (caching, the recommended 6-second sleep, and the free API key for 10x throughput) rather than dollars on an invoice.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (free service)
  PricingCategory: Free
  PricingUnit: request
  ProviderName: NIST National Vulnerability Database
  PublisherName: National Institute of Standards and Technology (NIST)
  ServiceCategory: Public Sector / Security Data
  ServiceName: NVD
layout: finops
meters:
- aggregation: sum
  description: Total NVD API requests; tracked against the rolling 30-second rate limit
  dimensions:
  - api
  - api_key
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: CVE records returned (used for delta sync planning)
  dimensions:
  - api
  name: cve_records_fetched
  unit: record
- aggregation: sum
  description: CPE records returned (used for delta sync planning)
  dimensions:
  - api
  name: cpe_records_fetched
  unit: record
name: Nvd Finops
provider_name: NVD
provider_slug: nvd
publisher_name: National Institute of Standards and Technology (NIST)
service_category: Public Sector / Security Data
slug: nvd-finops
source_filename: nvd-finops.yml
source_heading: FinOps Profile
source_url: https://nvd.nist.gov/developers/start-here
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: NVD\nproviderId: nvd\npublisherName: National Institute of Standards and Technology (NIST)\nserviceCategory: Public Sector / Security Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Security\n  - CVE\n  - CPE\n  - Vulnerability\n  - CVSS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for the National Vulnerability Database: APIs are free of charge from\n  NIST. Cost optimization is about request efficiency (caching, the recommended 6-second sleep, and the\n  free API key for 10x throughput) rather than dollars on an invoice.'\nsources:\n  - https://nvd.nist.gov/developers/start-here\n\
  \  - https://nvd.nist.gov/developers/request-an-api-key\nprinciples:\n  - name: Visibility\n    description: NVD does not invoice consumers; visibility is about consumption patterns. Track requests/30s\n      against the 5 (anonymous) or 50 (API-keyed) limit and CVE/CPE result counts in client-side telemetry.\n  - name: Allocation\n    description: Allocate the single shared API key per consuming application or team to keep request\n      budgets isolated. Tag downstream uses (vulnerability scanner, SBOM tool, dependency monitor) so\n      each owner can see their share of the per-key budget.\n  - name: Optimization\n    description: Always run with an API key (10x rate limit, free). Cache CVE and CPE responses; use the\n      lastModStartDate / lastModEndDate parameters to fetch only deltas instead of the full corpus. Mirror\n      to internal storage rather than refetching for every internal scan.\n  - name: Accountability\n    description: Even though there is no $ cost, throttling\
  \ impacts consuming product SLAs. Assign an\n      owner for the API key and the data refresh pipeline; review monthly for stale or runaway clients.\nbillingModel:\n  pricingCategory: Free / Public Service\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  chargeFrequency: None\nfocusColumns:\n  ServiceName: NVD\n  ServiceCategory: Public Sector / Security Data\n  ProviderName: NIST National Vulnerability Database\n  PublisherName: National Institute of Standards and Technology (NIST)\n  InvoiceIssuerName: N/A (free service)\n  PricingCategory: Free\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Total NVD API requests; tracked against the rolling 30-second rate limit\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - api_key\n      - endpoint\n  - name: cve_records_fetched\n    description: CVE records returned (used for delta sync planning)\n  \
  \  unit: record\n    aggregation: sum\n    dimensions:\n      - api\n  - name: cpe_records_fetched\n    description: CPE records returned (used for delta sync planning)\n    unit: record\n    aggregation: sum\n    dimensions:\n      - api\napis:\n  - name: NVD CVE API\n    baseURL: https://services.nvd.nist.gov/rest/json/cves/2.0\n    tags:\n      - Security\n      - CVE\n      - Vulnerability\n      - CVSS\n    serviceName: NVD CVE API\n    serviceCategory: Security Data\n  - name: NVD CVE Change History API\n    baseURL: https://services.nvd.nist.gov/rest/json/cvehistory/2.0\n    tags:\n      - Security\n      - CVE\n      - Vulnerability\n      - Change History\n    serviceName: NVD CVE Change History API\n    serviceCategory: Security Data\n  - name: NVD CPE API\n    baseURL: https://services.nvd.nist.gov/rest/json/cpes/2.0\n    tags:\n      - Security\n      - CPE\n      - Product Enumeration\n    serviceName: NVD CPE API\n    serviceCategory: Security Data\n  - name: NVD CPE Match\
  \ Criteria API\n    baseURL: https://services.nvd.nist.gov/rest/json/cpematch/2.0\n    tags:\n      - Security\n      - CPE\n      - Match Criteria\n    serviceName: NVD CPE Match Criteria API\n    serviceCategory: Security Data\n  - name: NVD Source API\n    baseURL: https://services.nvd.nist.gov/rest/json/source/2.0\n    tags:\n      - Security\n      - Data Sources\n      - Organizations\n    serviceName: NVD Source API\n    serviceCategory: Security Data\nunitEconomics:\n  - name: Requests per CVE refresh\n    metric: api_requests / cve_records_fetched\n    target: minimize via lastModStartDate delta sync\n  - name: Cache hit ratio\n    metric: cache_hits / (cache_hits + api_requests)\n    target: '> 0.9 for steady-state CVE/CPE lookups'\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nvd/refs/heads/main/finops/nvd-finops.yml
sources:
- https://nvd.nist.gov/developers/start-here
- https://nvd.nist.gov/developers/request-an-api-key
specification: FinOps Framework
tags:
- Security
- CVE
- CPE
- Vulnerability
- CVSS
- FinOps
- Cost Management
- FOCUS
---
