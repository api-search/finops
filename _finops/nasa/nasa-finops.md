---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nasa-apod-openapi.yml
  format: yaml
  label: NASA Astronomy Picture of the Day (APOD) API
  slug: apod
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nasa/refs/heads/main/openapi/nasa-apod-openapi.yml
- filename: nasa-mars-rover-photos-openapi.yml
  format: yaml
  label: NASA Mars Rover Photos API
  slug: mars-rover-photos
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nasa/refs/heads/main/openapi/nasa-mars-rover-photos-openapi.yml
- filename: nasa-neo-openapi.yml
  format: yaml
  label: NASA NeoWs (Near Earth Object Web Service) API
  slug: neo
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nasa/refs/heads/main/openapi/nasa-neo-openapi.yml
- filename: nasa-donki-openapi.yml
  format: yaml
  label: NASA DONKI (Space Weather) API
  slug: donki
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nasa/refs/heads/main/openapi/nasa-donki-openapi.yml
- filename: nasa-epic-openapi.yml
  format: yaml
  label: NASA EPIC (Earth Polychromatic Imaging Camera) API
  slug: epic
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nasa/refs/heads/main/openapi/nasa-epic-openapi.yml
- filename: nasa-nasa-image-and-video-library-openapi.yml
  format: yaml
  label: NASA Image and Video Library API
  slug: image-and-video-library
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nasa/refs/heads/main/openapi/nasa-nasa-image-and-video-library-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories:
  - Usage
  pricingCategory: Free / Public Good
description: 'FOCUS-aligned FinOps for NASA Open APIs: zero-cost public-good APIs whose only meaningful consumption signal is request volume per key. No invoiced charges; cost concerns are limited to internal consumer-side observability and rate-limit avoidance.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (no invoicing)
  ProviderName: NASA
  PublisherName: National Aeronautics and Space Administration
  ServiceCategory: Open Data
  ServiceName: NASA Open APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - api_key
  - endpoint
  name: api_requests
  unit: request
- aggregation: count
  dimensions:
  - api_key
  - api
  name: ratelimit_blocks
  unit: event
- aggregation: sum
  dimensions:
  - source_ip
  - api
  name: demo_key_requests
  unit: request
name: Nasa Finops
provider_name: NASA
provider_slug: nasa
publisher_name: National Aeronautics and Space Administration
service_category: Open Data / Public Sector
slug: nasa-finops
source_filename: nasa-finops.yml
source_heading: FinOps Profile
source_url: https://api.nasa.gov/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: NASA\nproviderId: nasa\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Government\n  - Open Data\n  - Space\ndescription: 'FOCUS-aligned FinOps for NASA Open APIs: zero-cost public-good APIs whose only meaningful\n  consumption signal is request volume per key. No invoiced charges; cost concerns are limited to internal\n  consumer-side observability and rate-limit avoidance.'\nsources:\n  - https://api.nasa.gov/\n  - https://api.nasa.gov/assets/html/authentication.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: National Aeronautics and Space Administration\nserviceCategory: Open Data / Public Sector\nbillingModel:\n  pricingCategory:\
  \ Free / Public Good\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: NASA Open APIs\n  ServiceCategory: Open Data\n  ProviderName: NASA\n  PublisherName: National Aeronautics and Space Administration\n  InvoiceIssuerName: N/A (no invoicing)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - api_key\n      - endpoint\n  - name: ratelimit_blocks\n    unit: event\n    aggregation: count\n    dimensions:\n      - api_key\n      - api\n  - name: demo_key_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - source_ip\n      - api\nprinciples:\n  - name: Visibility\n    description: Inspect the X-RateLimit-Limit and X-RateLimit-Remaining response headers on every call;\n      log them per-consumer to track approach to the 1,000/hour cap.\n  - name: Allocation\n    description: Issue distinct api.nasa.gov\
  \ API keys per consuming application or team to attribute usage;\n      the platform itself does not provide chargeback because there is no charge.\n  - name: Optimization\n    description: Cache responses (especially APOD, EPIC, and NeoWs which change at most daily) to stay\n      well below the hourly cap; avoid the shared DEMO_KEY for any real workload.\n  - name: Accountability\n    description: Each consuming team owns its NASA API key, monitors rate-limit headers, and contacts\n      api@nasa.gov before scaling beyond 1,000 req/hour rather than retrying through 429 blocks.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nasa/refs/heads/main/finops/nasa-finops.yml
sources:
- https://api.nasa.gov/
- https://api.nasa.gov/assets/html/authentication.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Government
- Open Data
- Space
---
