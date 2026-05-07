---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: usgs-earthquake-api-openapi.yaml
  format: yaml
  label: Earthquake Notifications, Feeds, and Web Services
  slug: earthquake-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/u-s-geological-survey/refs/heads/main/openapi/usgs-earthquake-api-openapi.yaml
- filename: usgs-water-data-api-openapi.yaml
  format: yaml
  label: USGS Water Data APIs
  slug: water-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/u-s-geological-survey/refs/heads/main/openapi/usgs-water-data-api-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories: []
  pricingCategory: No Charge (Public Open Data)
description: 'FOCUS-aligned FinOps for USGS: federal open-data services are zero-cost to consumers; FinOps exposure is on the consumer side (egress, downstream compute) rather than direct USGS billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: U.S. Geological Survey
  ProviderName: U.S. Geological Survey
  PublisherName: U.S. Geological Survey
  ServiceCategory: Public Open Data
  ServiceName: U.S. Geological Survey APIs
layout: finops
meters:
- aggregation: sum
  description: Count of requests to USGS web services (no monetary charge from USGS)
  dimensions:
  - service
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Volume of catalog / feed bulk downloads
  dimensions:
  - service
  name: bulk_download_volume
  unit: GB
name: U S Geological Survey Finops
provider_name: U.S. Geological Survey
provider_slug: u-s-geological-survey
publisher_name: U.S. Geological Survey
service_category: Public Open Data
slug: u-s-geological-survey-finops
source_filename: u-s-geological-survey-finops.yml
source_heading: FinOps Profile
source_url: https://www.usgs.gov/products/web-tools/apis
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: U.S. Geological Survey\nproviderId: u-s-geological-survey\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Federal Government\n  - Earth Science\n  - Open Data\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for USGS: federal open-data services are zero-cost to consumers; FinOps\n  exposure is on the consumer side (egress, downstream compute) rather than direct USGS billing.'\nsources:\n  - https://www.usgs.gov/products/web-tools/apis\n  - https://earthquake.usgs.gov/data/comcat/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: U.S. Geological Survey\nserviceCategory: Public Open Data\n\
  billingModel:\n  pricingCategory: No Charge (Public Open Data)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: U.S. Geological Survey APIs\n  ServiceCategory: Public Open Data\n  ProviderName: U.S. Geological Survey\n  PublisherName: U.S. Geological Survey\n  InvoiceIssuerName: U.S. Geological Survey\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of requests to USGS web services (no monetary charge from USGS)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - endpoint\n  - name: bulk_download_volume\n    description: Volume of catalog / feed bulk downloads\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track consumption inside your own application logs; USGS does not provide a per-consumer\n      usage dashboard.\n  - name: Allocation\n    description: USGS\
  \ access is free, so allocation is for capacity-planning rather than chargeback —\n      tag downstream compute and egress that result from USGS calls.\n  - name: Optimization\n    description: Cache stable catalog records, prefer the recommended GeoJSON / ATOM feeds over repeated\n      ad-hoc queries, and batch via the documented Python download scripts.\n  - name: Accountability\n    description: Application owners are responsible for being courteous federal-data citizens — avoiding\n      polling storms that could trigger network-edge throttling.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/u-s-geological-survey/refs/heads/main/finops/u-s-geological-survey-finops.yml
sources:
- https://www.usgs.gov/products/web-tools/apis
- https://earthquake.usgs.gov/data/comcat/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Federal Government
- Earth Science
- Open Data
- FinOps
- FOCUS
---
