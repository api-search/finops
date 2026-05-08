---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: metro-transit-nextrip-openapi.json
  format: json
  label: Metro Transit NexTrip API
  slug: nextrip-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/metro-transit/refs/heads/main/openapi/metro-transit-nextrip-openapi.json
- filename: metro-transit-alerts-openapi.json
  format: json
  label: Metro Transit Service Alerts API
  slug: alerts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/metro-transit/refs/heads/main/openapi/metro-transit-alerts-openapi.json
- filename: metro-transit-tripplanner-openapi.json
  format: json
  label: Metro Transit Trip Planner API
  slug: trip-planner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/metro-transit/refs/heads/main/openapi/metro-transit-tripplanner-openapi.json
- filename: metro-transit-schedule-openapi.json
  format: json
  label: Metro Transit Schedule API
  slug: schedule-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/metro-transit/refs/heads/main/openapi/metro-transit-schedule-openapi.json
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A
  chargeCategories: []
  pricingCategory: Free / Open Data
description: 'FOCUS-aligned FinOps shape for Metro Transit: a free, open-data API surface (GTFS, GTFS-realtime, NexTrip / REST). There is no provider-side cost to the API consumer; FinOps focus shifts to the consumer-side compute / egress / storage cost of polling and serving the public data, plus the Metropolitan Council''s own publishing cost (which is not invoiced to consumers).'
focus_columns:
  BillingCurrency: N/A
  ChargeCategory: N/A
  InvoiceIssuerName: N/A (free / open data)
  ProviderName: Metro Transit
  PublisherName: Metropolitan Council
  ServiceCategory: Public Transit Open Data
  ServiceName: Metro Transit Open Data API
layout: finops
meters:
- aggregation: sum
  description: Number of polls against GTFS-realtime feeds (consumer-side).
  dimensions:
  - feed
  - consumer_app
  name: realtime_polls
  unit: request
- aggregation: sum
  description: GTFS static zip downloads (current + next-week + flex).
  dimensions:
  - feed
  - consumer_app
  name: gtfs_downloads
  unit: download
- aggregation: sum
  description: REST API requests (NexTrip, alerts, trip planner, schedule).
  dimensions:
  - endpoint
  - consumer_app
  name: rest_requests
  unit: request
- aggregation: sum
  description: Bytes downloaded from svc.metrotransit.org (consumer-side accounting).
  dimensions:
  - feed
  - consumer_app
  name: data_egress
  unit: GB
name: Metro Transit Finops
provider_name: Metro Transit
provider_slug: metro-transit
publisher_name: Metropolitan Council (Metro Transit)
service_category: Public Transit Open Data
slug: metro-transit-finops
source_filename: metro-transit-finops.yml
source_heading: FinOps Profile
source_url: https://svc.metrotransit.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Metro Transit\nproviderId: metro-transit\npublisherName: Metropolitan Council (Metro Transit)\nserviceCategory: Public Transit Open Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Minneapolis\n  - Minnesota\n  - Public Transportation\n  - Real-Time\n  - Transit\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Metro Transit: a free, open-data API surface (GTFS, GTFS-realtime,\n  NexTrip / REST). There is no provider-side cost to the API consumer; FinOps focus shifts to the\n  consumer-side compute / egress / storage cost of polling and serving the public data, plus the\n  Metropolitan Council''s\
  \ own publishing cost (which is not invoiced to consumers).'\nsources:\n  - https://svc.metrotransit.org/\n  - https://www.metrotransit.org/developers\nprinciples:\n  - name: Visibility\n    description: There is no Metro Transit invoice to track. Instead, monitor consumer-side metrics —\n      poll rate per feed, bytes downloaded, cache hit rate — to understand the cost the public data\n      surface generates inside your own infrastructure.\n  - name: Allocation\n    description: Allocate consumer-side cost (egress, compute, storage of GTFS archive) by the application\n      or product feature consuming the data (commuter app, signage, internal analytics, ML training).\n  - name: Optimization\n    description: Cache GTFS-realtime feeds at a single edge / proxy and fan out to clients (instead of\n      having each client poll svc.metrotransit.org directly). Use Last-Modified for the static GTFS zip\n      to skip re-downloads. Match poll cadence to the 5-second refresh interval — polling\
  \ faster is\n      pure waste.\n  - name: Accountability\n    description: Designate a data-feed owner inside the consuming organization who tracks polling\n      behavior, ensures attribution, and responds promptly if Metro Transit reports excessive load.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Architecting for Cloud\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Free / Open Data\n  billingFrequency: N/A\n  billingCurrency: N/A\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Metro Transit Open Data API\n  ServiceCategory: Public Transit Open Data\n  ProviderName: Metro Transit\n  PublisherName: Metropolitan Council\n  InvoiceIssuerName:\
  \ N/A (free / open data)\n  BillingCurrency: N/A\n  ChargeCategory: N/A\nmeters:\n  - name: realtime_polls\n    description: Number of polls against GTFS-realtime feeds (consumer-side).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - feed\n      - consumer_app\n  - name: gtfs_downloads\n    description: GTFS static zip downloads (current + next-week + flex).\n    unit: download\n    aggregation: sum\n    dimensions:\n      - feed\n      - consumer_app\n  - name: rest_requests\n    description: REST API requests (NexTrip, alerts, trip planner, schedule).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - consumer_app\n  - name: data_egress\n    description: Bytes downloaded from svc.metrotransit.org (consumer-side accounting).\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - feed\n      - consumer_app\napis:\n  - name: Metro Transit NexTrip API\n    baseURL: https://svc.metrotransit.org/nextripv2\n    tags:\n      - Departures\n\
  \      - Real-Time\n      - Transit\n    serviceName: Metro Transit NexTrip API\n    serviceCategory: API\n  - name: Metro Transit Service Alerts API\n    baseURL: https://svc.metrotransit.org/alerts\n    tags:\n      - Alerts\n      - Real-Time\n      - Transit\n    serviceName: Metro Transit Service Alerts API\n    serviceCategory: API\n  - name: Metro Transit Trip Planner API\n    baseURL: https://svc.metrotransit.org/tripplanner\n    tags:\n      - Trip Planner\n      - Routing\n      - Transit\n    serviceName: Metro Transit Trip Planner API\n    serviceCategory: API\n  - name: Metro Transit Schedule API\n    baseURL: https://svc.metrotransit.org/schedule\n    tags:\n      - Schedule\n      - Timetable\n      - Transit\n    serviceName: Metro Transit Schedule API\n    serviceCategory: API\nunitEconomics:\n  - name: Internal Cost per Public-Data Poll\n    metric: consumer_infra_cost / realtime_polls\n    target: minimize via shared edge cache\n  - name: Cache Hit Rate\n    metric:\
  \ cache_hits / (cache_hits + origin_polls)\n    target: '> 0.95'\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/metro-transit/refs/heads/main/finops/metro-transit-finops.yml
sources:
- https://svc.metrotransit.org/
- https://www.metrotransit.org/developers
specification: FinOps Framework
tags:
- Minneapolis
- Minnesota
- Public Transportation
- Real-Time
- Transit
- FinOps
- FOCUS
---
