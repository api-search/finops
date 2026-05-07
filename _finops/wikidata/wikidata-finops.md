---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: wikidata-mediawiki-openapi.yml
  format: yaml
  label: Wikibase REST API
  slug: wikibase-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/openapi/wikidata-mediawiki-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Free / CC0 (Wikimedia Enterprise priced separately)
description: 'FOCUS-aligned FinOps for Wikidata: the public APIs are zero-cost / CC0; consumer-side cost is the engineering effort and infrastructure spent fetching, caching, and re-hosting Wikidata content responsibly. Commercial-grade access is available separately through Wikimedia Enterprise and is the only path with a real invoice line.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Wikimedia Foundation, Inc.
  ProviderName: Wikimedia Foundation
  PublisherName: Wikimedia Foundation, Inc.
  ServiceCategory: Open Knowledge Graph
  ServiceName: Wikidata
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - client_ip
  name: sparql_queries
  unit: query
- aggregation: sum
  dimensions:
  - module
  - client_ip
  name: action_api_requests
  unit: request
- aggregation: sum
  dimensions:
  - resource
  - client_ip
  name: rest_api_requests
  unit: request
- aggregation: sum
  dimensions:
  - dump_type
  name: dump_downloads
  unit: GB
- aggregation: sum
  dimensions:
  - stream
  name: event_stream_subscriptions
  unit: connection-hour
name: Wikidata Finops
provider_name: Wikidata
provider_slug: wikidata
publisher_name: Wikimedia Foundation, Inc.
service_category: Open Knowledge Graph
slug: wikidata-finops
source_filename: wikidata-finops.yml
source_heading: FinOps Profile
source_url: https://www.wikidata.org/wiki/Wikidata:Data_access
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Wikidata\nproviderId: wikidata\npublisherName: Wikimedia Foundation, Inc.\nserviceCategory: Open Knowledge Graph\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Knowledge Graph\n  - Linked Data\n  - Open Data\n  - SPARQL\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Wikidata: the public APIs are zero-cost / CC0; consumer-side cost is the engineering effort and infrastructure spent fetching, caching, and re-hosting Wikidata content responsibly. Commercial-grade access is available separately through Wikimedia Enterprise and is the only path with a real invoice line.'\nsources:\n  - https://www.wikidata.org/wiki/Wikidata:Data_access\n\
  \  - https://dumps.wikimedia.org\n  - https://enterprise.wikimedia.com\nbillingModel:\n  pricingCategory: Free / CC0 (Wikimedia Enterprise priced separately)\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Wikidata\n  ServiceCategory: Open Knowledge Graph\n  ProviderName: Wikimedia Foundation\n  PublisherName: Wikimedia Foundation, Inc.\n  InvoiceIssuerName: Wikimedia Foundation, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: sparql_queries\n    unit: query\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - client_ip\n  - name: action_api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - module\n      - client_ip\n  - name: rest_api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - resource\n      - client_ip\n  - name: dump_downloads\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - dump_type\n  - name: event_stream_subscriptions\n  \
  \  unit: connection-hour\n    aggregation: sum\n    dimensions:\n      - stream\nprinciples:\n  - name: Visibility\n    description: There is no Wikimedia billing API for the free APIs; visibility is consumer-side - log SPARQL query runtimes, MediaWiki maxlag responses, and 429s to understand pressure on the shared infrastructure.\n  - name: Allocation\n    description: Allocate by surface (SPARQL vs Action vs REST vs dumps) since each surface has a different cost model for the consumer (live latency vs bulk-mirror vs streaming).\n  - name: Optimization\n    description: 'Optimization is etiquette: cache aggressively, prefer dumps for bulk reads, send maxlag and a descriptive User-Agent, and avoid running long SPARQL queries near the 60s timeout.'\n  - name: Accountability\n    description: Engineering owns User-Agent compliance and dump-mirroring strategy; if a use case requires SLAs, accountability for that spend shifts to procurement via Wikimedia Enterprise.\nmaintainers:\n  - FN:\
  \ Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/finops/wikidata-finops.yml
sources:
- https://www.wikidata.org/wiki/Wikidata:Data_access
- https://dumps.wikimedia.org
- https://enterprise.wikimedia.com
specification: FinOps Framework
tags:
- Knowledge Graph
- Linked Data
- Open Data
- SPARQL
- FinOps
- FOCUS
---
