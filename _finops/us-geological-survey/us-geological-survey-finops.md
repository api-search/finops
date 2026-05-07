---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: usgs-earthquake-catalog-openapi.yml
  format: yaml
  label: USGS Earthquake Catalog API
  slug: earthquake-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/us-geological-survey/refs/heads/main/openapi/usgs-earthquake-catalog-openapi.yml
- filename: openapi
  format: yaml
  label: USGS Water Data OGC API
  slug: water-data-api
  spec_type: OpenAPI
  url: https://api.waterdata.usgs.gov/ogcapi/v0/openapi?f=json
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories: []
  pricingCategory: Free Public Service
description: 'FinOps shape for the U.S. Geological Survey: free public earth-science APIs (earthquakes, water, geomagnetism, ScienceBase). There is no commercial billing surface; FinOps focuses on stewardship of shared public infrastructure rather than dollar cost.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: U.S. Geological Survey
  ProviderName: U.S. Geological Survey
  PublisherName: U.S. Geological Survey
  ServiceCategory: Government Open Data
  ServiceName: USGS APIs
layout: finops
meters:
- aggregation: sum
  description: Requests to USGS web services; counted against api.data.gov per-key budget when fronted, otherwise unmetered
  dimensions:
  - service
  - api_key
  name: api_requests
  unit: request
- aggregation: sum
  description: Real-time GeoJSON feed retrievals (recommended pattern for automated consumers)
  dimensions:
  - feed
  name: feed_pulls
  unit: request
name: Us Geological Survey Finops
provider_name: US Geological Survey
provider_slug: us-geological-survey
publisher_name: U.S. Geological Survey
service_category: Government Open Data
slug: us-geological-survey-finops
source_filename: us-geological-survey-finops.yml
source_heading: FinOps Profile
source_url: https://www.usgs.gov/products/web-tools/apis
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: US Geological Survey\nproviderId: us-geological-survey\npublisherName: U.S. Geological Survey\nserviceCategory: Government Open Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Federal Government\n  - Earth Science\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for the U.S. Geological Survey: free public earth-science APIs (earthquakes, water, geomagnetism, ScienceBase). There is no commercial billing surface; FinOps focuses on stewardship of shared public infrastructure rather than dollar cost.'\nsources:\n  - https://www.usgs.gov/products/web-tools/apis\n  - https://earthquake.usgs.gov/fdsnws/event/1/\nbillingModel:\n\
  \  pricingCategory: Free Public Service\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: USGS APIs\n  ServiceCategory: Government Open Data\n  ProviderName: U.S. Geological Survey\n  PublisherName: U.S. Geological Survey\n  InvoiceIssuerName: U.S. Geological Survey\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Requests to USGS web services; counted against api.data.gov per-key budget when fronted, otherwise unmetered\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - api_key\n  - name: feed_pulls\n    description: Real-time GeoJSON feed retrievals (recommended pattern for automated consumers)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - feed\nprinciples:\n  - name: Visibility\n    description: There is no USGS-issued usage dashboard; consumers monitor 400 (over 20K results) and 429 responses themselves and inspect api.data.gov\
  \ rate-limit headers when applicable.\n  - name: Allocation\n    description: Allocate by application by issuing distinct api.data.gov API keys per team or app for endpoints that authenticate; for unauthenticated endpoints, use User-Agent identification.\n  - name: Optimization\n    description: Switch from polling to the real-time GeoJSON feeds; cache results client-side; page large queries to stay under the 20,000-result cap.\n  - name: Accountability\n    description: Owner is the application team; abusive polling can be throttled by USGS at the infrastructure layer, so monitoring 4xx/5xx response rates is the practical accountability signal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/us-geological-survey/refs/heads/main/finops/us-geological-survey-finops.yml
sources:
- https://www.usgs.gov/products/web-tools/apis
- https://earthquake.usgs.gov/fdsnws/event/1/
specification: FinOps Framework
tags:
- Federal Government
- Earth Science
- FinOps
- FOCUS
---
