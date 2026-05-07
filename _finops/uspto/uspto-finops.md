---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: uspto-patent-api-openapi.yml
  format: yaml
  label: USPTO Patent & Trademark API
  slug: patent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uspto/refs/heads/main/openapi/uspto-patent-api-openapi.yml
- filename: index.html
  format: yaml
  label: USPTO Patent Trial and Appeal Board (PTAB) API
  slug: ptab-api
  spec_type: OpenAPI
  url: https://data.uspto.gov/swagger/index.html
- filename: tsdr-api-v1
  format: yaml
  label: USPTO Trademark Status and Document Retrieval (TSDR) API
  slug: tsdr-api
  spec_type: OpenAPI
  url: https://developer.uspto.gov/swagger/tsdr-api-v1
- filename: oa_actions.json
  format: json
  label: USPTO Office Action Text Retrieval API
  slug: office-actions-api
  spec_type: OpenAPI
  url: https://developer.uspto.gov/ds-api/swagger/docs/oa_actions.json
- filename: enriched_cited_reference_metadata.json
  format: json
  label: USPTO Enriched Citation API
  slug: enriched-citation-api
  spec_type: OpenAPI
  url: https://developer.uspto.gov/ds-api/swagger/docs/enriched_cited_reference_metadata.json
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories: []
  pricingCategory: Free Public Service
description: 'FinOps shape for USPTO: free public patent/trademark APIs. There is no commercial billing surface. FinOps centers on key stewardship and using the Bulk Data Storage System for high-volume needs.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: U.S. Patent and Trademark Office
  ProviderName: U.S. Patent and Trademark Office
  PublisherName: U.S. Patent and Trademark Office
  ServiceCategory: Government Open Data
  ServiceName: USPTO APIs
layout: finops
meters:
- aggregation: sum
  description: Requests against USPTO APIs (counts against per-API key-usage policy where applicable)
  dimensions:
  - api
  - api_key
  name: api_requests
  unit: request
- aggregation: count
  description: Bulk Data Storage System downloads (preferred for high-volume access)
  name: bulk_downloads
  unit: file
name: Uspto Finops
provider_name: USPTO
provider_slug: uspto
publisher_name: U.S. Patent and Trademark Office
service_category: Government Open Data
slug: uspto-finops
source_filename: uspto-finops.yml
source_heading: FinOps Profile
source_url: https://developer.uspto.gov/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: USPTO\nproviderId: uspto\npublisherName: U.S. Patent and Trademark Office\nserviceCategory: Government Open Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Federal Government\n  - Intellectual Property\n  - Open Data\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for USPTO: free public patent/trademark APIs. There is no commercial billing surface. FinOps centers on key stewardship and using the Bulk Data Storage System for high-volume needs.'\nsources:\n  - https://developer.uspto.gov/\n  - https://data.uspto.gov/\nbillingModel:\n  pricingCategory: Free Public Service\n  billingFrequency: None\n  billingCurrency:\
  \ USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: USPTO APIs\n  ServiceCategory: Government Open Data\n  ProviderName: U.S. Patent and Trademark Office\n  PublisherName: U.S. Patent and Trademark Office\n  InvoiceIssuerName: U.S. Patent and Trademark Office\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Requests against USPTO APIs (counts against per-API key-usage policy where applicable)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - api_key\n  - name: bulk_downloads\n    description: Bulk Data Storage System downloads (preferred for high-volume access)\n    unit: file\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Track usage via the per-API key-usage policy and FAQ; USPTO does not provide a centralized usage dashboard, so consumers should log their own request counts.\n  - name: Allocation\n    description: Allocate by application by issuing distinct USPTO API\
  \ keys per app/team for APIs that require them (e.g. TSDR).\n  - name: Optimization\n    description: Use the Bulk Data Storage System for catalog-scale ingestion instead of per-record API polling; cache responses; align with the data.uspto.gov migration before May 29, 2026.\n  - name: Accountability\n    description: Owner is the application team holding the key; review key-usage FAQs and 429 responses to confirm the integration is operating within documented bounds.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/uspto/refs/heads/main/finops/uspto-finops.yml
sources:
- https://developer.uspto.gov/
- https://data.uspto.gov/
specification: FinOps Framework
tags:
- Federal Government
- Intellectual Property
- Open Data
- FinOps
- FOCUS
---
