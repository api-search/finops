---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: esri-arcgis-platform-openapi.yml
  format: yaml
  label: ESRI ArcGIS Platform API
  slug: esri-arcgis-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/esri-arcgis/refs/heads/main/openapi/esri-arcgis-platform-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (Location Platform); Annual (ArcGIS Online)
  chargeCategories:
  - Usage
  - Purchase
  - Credit
  - Adjustment
  pricingCategory: Pay-As-You-Go + Subscription + Credits
description: 'FOCUS-aligned FinOps for Esri ArcGIS: a hybrid surface combining (a) ArcGIS Location Platform pay-as-you-go transaction pricing per service (tiles, geocoding, routing, etc.) with monthly free tiers, and (b) ArcGIS Online named-user subscriptions plus credit-based consumption for storage and analysis.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Environmental Systems Research Institute, Inc.
  ProviderName: Esri
  PublisherName: Environmental Systems Research Institute, Inc.
  ServiceCategory: GIS / Location Services
  ServiceName: Esri ArcGIS
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api_key
  - style
  name: basemap_tile_requests
  unit: tile
- aggregation: sum
  dimensions:
  - api_key
  - operation
  name: geocode_requests
  unit: geocode
- aggregation: sum
  dimensions:
  - api_key
  - mode
  name: routing_requests
  unit: route
- aggregation: sum
  dimensions:
  - api_key
  - operation
  name: places_requests
  unit: request
- aggregation: sum
  dimensions:
  - api_key
  - dataset
  name: enrichment_attributes
  unit: attribute
- aggregation: sum
  dimensions:
  - api_key
  - operation
  name: spatial_analysis_features
  unit: feature
- aggregation: max
  dimensions:
  - org
  name: feature_storage
  unit: MB-month
- aggregation: max
  dimensions:
  - org
  name: tile_storage
  unit: MB-month
- aggregation: sum
  dimensions:
  - org
  name: tile_bandwidth
  unit: GB
- aggregation: sum
  dimensions:
  - org
  - user_type
  - service
  name: arcgis_online_credits
  unit: credit
- aggregation: max
  dimensions:
  - user_type
  name: arcgis_online_user_seats
  unit: seat
name: Esri Arcgis Finops
provider_name: ESRI ArcGIS
provider_slug: esri-arcgis
publisher_name: Environmental Systems Research Institute, Inc. (Esri)
service_category: GIS / Location Services
slug: esri-arcgis-finops
source_filename: esri-arcgis-finops.yml
source_heading: FinOps Profile
source_url: https://location.arcgis.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Esri ArcGIS\nproviderId: esri-arcgis\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - GIS\n  - Location Services\n  - Mapping\ndescription: 'FOCUS-aligned FinOps for Esri ArcGIS: a hybrid surface combining (a) ArcGIS Location Platform\n  pay-as-you-go transaction pricing per service (tiles, geocoding, routing, etc.) with monthly free tiers,\n  and (b) ArcGIS Online named-user subscriptions plus credit-based consumption for storage and analysis.'\nsources:\n  - https://location.arcgis.com/pricing/\n  - https://www.esri.com/en-us/arcgis/products/arcgis-online/pricing/credits\n  - https://www.esri.com/en-us/arcgis/products/arcgis-online/buy\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Environmental Systems Research Institute, Inc. (Esri)\nserviceCategory: GIS / Location Services\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription + Credits\n  billingFrequency: Monthly (Location Platform); Annual (ArcGIS Online)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Esri ArcGIS\n  ServiceCategory: GIS / Location Services\n  ProviderName: Esri\n  PublisherName: Environmental Systems Research Institute, Inc.\n  InvoiceIssuerName: Environmental Systems Research Institute, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: basemap_tile_requests\n    unit: tile\n    aggregation: sum\n    dimensions:\n      - api_key\n      - style\n  - name: geocode_requests\n    unit: geocode\n    aggregation: sum\n    dimensions:\n      - api_key\n      - operation\n  - name: routing_requests\n    unit: route\n    aggregation: sum\n    dimensions:\n      - api_key\n      - mode\n \
  \ - name: places_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - operation\n  - name: enrichment_attributes\n    unit: attribute\n    aggregation: sum\n    dimensions:\n      - api_key\n      - dataset\n  - name: spatial_analysis_features\n    unit: feature\n    aggregation: sum\n    dimensions:\n      - api_key\n      - operation\n  - name: feature_storage\n    unit: MB-month\n    aggregation: max\n    dimensions:\n      - org\n  - name: tile_storage\n    unit: MB-month\n    aggregation: max\n    dimensions:\n      - org\n  - name: tile_bandwidth\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - org\n  - name: arcgis_online_credits\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - org\n      - user_type\n      - service\n  - name: arcgis_online_user_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - user_type\nprinciples:\n  - name: Visibility\n    description: Use the ArcGIS Location Platform\
  \ usage dashboard, ArcGIS Online credits dashboard, and\n      org-level reports to monitor monthly consumption against free-tier ceilings.\n  - name: Allocation\n    description: Issue one API key per application or environment; assign ArcGIS Online users to groups\n      mapped to cost centers to allocate seat and credit spend.\n  - name: Optimization\n    description: Cache geocoding results where licensing allows; pre-bake tile sets that exceed 2M/month\n      free; tune routing precision; right-size user-type assignments (Viewer vs Creator) to avoid over-licensing;\n      buy credit blocks before recurring overage.\n  - name: Accountability\n    description: GIS lead owns ArcGIS Online org subscription; engineering owns Location Platform API\n      keys; finance reviews monthly variance against credit and PAYG forecasts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/esri-arcgis/refs/heads/main/finops/esri-arcgis-finops.yml
sources:
- https://location.arcgis.com/pricing/
- https://www.esri.com/en-us/arcgis/products/arcgis-online/pricing/credits
- https://www.esri.com/en-us/arcgis/products/arcgis-online/buy
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- GIS
- Location Services
- Mapping
---
