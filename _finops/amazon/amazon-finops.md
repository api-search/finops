---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-selling-partner-api-openapi.yml
  format: yaml
  label: Amazon Selling Partner API
  slug: selling-partner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon/refs/heads/main/openapi/amazon-selling-partner-api-openapi.yml
- filename: amazon-advertising-api-openapi.yml
  format: yaml
  label: Amazon Advertising API
  slug: advertising-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon/refs/heads/main/openapi/amazon-advertising-api-openapi.yml
- filename: amazon-pay-api-openapi.yml
  format: yaml
  label: Amazon Pay API
  slug: pay-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon/refs/heads/main/openapi/amazon-pay-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Amazon (Web Services + Marketplace + Ads).
focus_columns:
  BillingCurrency: USD
  ProviderName: Amazon (Web Services + Marketplace + Ads)
  PublisherName: Amazon (Web Services + Marketplace + Ads)
  ServiceCategory: Cloud + Commerce
  ServiceName: Amazon (Web Services + Marketplace + Ads)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - region
  - instance_type
  - tenant
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - service
  - tier
  name: storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - egress_type
  - region_pair
  name: data_transfer
  unit: GB
- aggregation: sum
  dimensions:
  - service
  - operation
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - service
  name: managed_services
  unit: varies
name: Amazon Finops
provider_name: Amazon
provider_slug: amazon
publisher_name: Amazon (Web Services + Marketplace + Ads)
service_category: Cloud + Commerce
slug: amazon-finops
source_filename: amazon-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon (Web Services + Marketplace + Ads)\nproviderId: amazon\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud + Commerce\ndescription: FOCUS-aligned FinOps for Amazon (Web Services + Marketplace + Ads).\nsources:\n  - https://aws.amazon.com/pricing/\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon (Web Services + Marketplace + Ads)\nserviceCategory: Cloud + Commerce\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Amazon (Web Services + Marketplace + Ads)\n  ServiceCategory: Cloud + Commerce\n\
  \  ProviderName: Amazon (Web Services + Marketplace + Ads)\n  PublisherName: Amazon (Web Services + Marketplace + Ads)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Amazon (Web Services + Marketplace + Ads) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n  \
  \  description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon/refs/heads/main/finops/amazon-finops.yml
sources:
- https://aws.amazon.com/pricing/
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud + Commerce
---
