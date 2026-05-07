---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the The National Aeronautics and Space Administration API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: The National Aeronautics and Space Administration
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: The National Aeronautics and Space Administration
  PublisherName: The National Aeronautics and Space Administration
  ServiceCategory: Developer Tools / API
  ServiceName: The National Aeronautics and Space Administration
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: National Aeronautics And Space Administration Finops
provider_name: The National Aeronautics and Space Administration
provider_slug: national-aeronautics-and-space-administration
publisher_name: The National Aeronautics and Space Administration
service_category: API
slug: national-aeronautics-and-space-administration-finops
source_filename: national-aeronautics-and-space-administration-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: The National Aeronautics and Space Administration\nproviderId: national-aeronautics-and-space-administration\npublisherName: The National Aeronautics and Space Administration\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Government\n  - Science\n  - Space\n  - Imagery\n  - Earth Observation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the The National Aeronautics and Space Administration API\n  surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics\n  reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs\
  \ visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n   \
  \   - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: The National Aeronautics and Space Administration\n  ServiceCategory: Developer Tools / API\n  ProviderName: The National Aeronautics and Space Administration\n  PublisherName: The National Aeronautics and Space Administration\n  InvoiceIssuerName: The National Aeronautics and Space Administration\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n\
  \    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: APOD - Astronomy Picture of the Day\n    baseURL: https://api.nasa.gov/planetary/apod\n    tags:\n      - Astronomy\n      - Imagery\n    serviceName: APOD - Astronomy Picture of the Day\n    serviceCategory: API\n  - name: NeoWs - Near Earth Object Web Service\n    baseURL: https://api.nasa.gov/neo/rest/v1\n    tags:\n      - Asteroids\n      - Space\n    serviceName: NeoWs - Near Earth Object\
  \ Web Service\n    serviceCategory: API\n  - name: DONKI - Space Weather Database Of Notifications, Knowledge, Information\n    baseURL: https://api.nasa.gov/DONKI\n    tags:\n      - Space Weather\n      - Science\n    serviceName: DONKI - Space Weather Database Of Notifications, Knowledge, Information\n    serviceCategory: API\n  - name: Earth Imagery and Assets\n    baseURL: https://api.nasa.gov/planetary/earth\n    tags:\n      - Earth Observation\n      - Imagery\n    serviceName: Earth Imagery and Assets\n    serviceCategory: API\n  - name: EONET - Earth Observatory Natural Event Tracker\n    baseURL: https://eonet.gsfc.nasa.gov/api/v3\n    tags:\n      - Earth Observation\n      - Natural Events\n    serviceName: EONET - Earth Observatory Natural Event Tracker\n    serviceCategory: API\n  - name: EPIC - Earth Polychromatic Imaging Camera\n    baseURL: https://api.nasa.gov/EPIC/api\n    tags:\n      - Earth Observation\n      - Imagery\n    serviceName: EPIC - Earth Polychromatic\
  \ Imaging Camera\n    serviceCategory: API\n  - name: Mars Rover Photos\n    baseURL: https://api.nasa.gov/mars-photos/api/v1\n    tags:\n      - Mars\n      - Imagery\n      - Rover\n    serviceName: Mars Rover Photos\n    serviceCategory: API\n  - name: NASA Image and Video Library\n    baseURL: https://images-api.nasa.gov\n    tags:\n      - Imagery\n      - Video\n      - Media\n    serviceName: NASA Image and Video Library\n    serviceCategory: API\n  - name: TLE - Two Line Element Set\n    baseURL: https://tle.ivanstanojevic.me/api\n    tags:\n      - Satellites\n      - Orbital Data\n    serviceName: TLE - Two Line Element Set\n    serviceCategory: API\n  - name: Exoplanet Archive API\n    baseURL: https://exoplanetarchive.ipac.caltech.edu/TAP\n    tags:\n      - Exoplanets\n      - Astronomy\n    serviceName: Exoplanet Archive API\n    serviceCategory: API\n  - name: InSight - Mars Weather Service\n    baseURL: https://api.nasa.gov/insight_weather\n    tags:\n      - Mars\n   \
  \   - Weather\n    serviceName: InSight - Mars Weather Service\n    serviceCategory: API\n  - name: TechPort\n    baseURL: https://api.nasa.gov/techport/api\n    tags:\n      - Technology\n      - Research\n    serviceName: TechPort\n    serviceCategory: API\n  - name: SSD/CNEOS - Solar System Dynamics and Center for Near-Earth Object Studies\n    baseURL: https://ssd-api.jpl.nasa.gov\n    tags:\n      - Solar System\n      - Asteroids\n      - Comets\n    serviceName: SSD/CNEOS - Solar System Dynamics and Center for Near-Earth Object Studies\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/national-aeronautics-and-space-administration/refs/heads/main/finops/national-aeronautics-and-space-administration-finops.yml
sources: []
specification: FinOps Framework
tags:
- Government
- Science
- Space
- Imagery
- Earth Observation
- FinOps
- Cost Management
- FOCUS
---
