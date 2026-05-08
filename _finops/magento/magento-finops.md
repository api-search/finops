---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: magento-rest-api-openapi.yml
  format: yaml
  label: Magento REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/magento/refs/heads/main/openapi/magento-rest-api-openapi.yml
- filename: magento-webhooks-asyncapi.yml
  format: yaml
  label: Adobe Commerce Webhooks
  slug: webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/magento/refs/heads/main/asyncapi/magento-webhooks-asyncapi.yml
- filename: magento-events-asyncapi.yml
  format: yaml
  label: Adobe Commerce Eventing
  slug: events
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/magento/refs/heads/main/asyncapi/magento-events-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom Tier-Based by AOV/GMV
description: FOCUS-aligned FinOps for Adobe Commerce (Magento).
focus_columns:
  BillingCurrency: USD
  ProviderName: Adobe Commerce (Magento)
  PublisherName: Adobe Commerce (Magento)
  ServiceCategory: E-Commerce Platform
  ServiceName: Adobe Commerce (Magento)
layout: finops
meters:
- aggregation: max
  name: annual_contract
  unit: year
- aggregation: sum
  name: gmv
  unit: USD
- aggregation: avg
  name: average_order_value
  unit: USD
- aggregation: max
  name: cloud_infrastructure
  unit: GB-month
name: Magento Finops
provider_name: magento
provider_slug: magento
publisher_name: Adobe Commerce (Magento)
service_category: E-Commerce Platform
slug: magento-finops
source_filename: magento-finops.yml
source_heading: FinOps Profile
source_url: https://business.adobe.com/products/magento/magento-commerce.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Commerce (Magento)\nproviderId: magento\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - E-Commerce Platform\ndescription: FOCUS-aligned FinOps for Adobe Commerce (Magento).\nsources:\n  - https://business.adobe.com/products/magento/magento-commerce.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Commerce (Magento)\nserviceCategory: E-Commerce Platform\nbillingModel:\n  pricingCategory: Custom Tier-Based by AOV/GMV\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Adobe Commerce (Magento)\n  ServiceCategory: E-Commerce Platform\n  ProviderName: Adobe Commerce (Magento)\n  PublisherName:\
  \ Adobe Commerce (Magento)\n  BillingCurrency: USD\nmeters:\n  - name: annual_contract\n    unit: year\n    aggregation: max\n  - name: gmv\n    unit: USD\n    aggregation: sum\n  - name: average_order_value\n    unit: USD\n    aggregation: avg\n  - name: cloud_infrastructure\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Adobe Commerce (Magento) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/magento/refs/heads/main/finops/magento-finops.yml
sources:
- https://business.adobe.com/products/magento/magento-commerce.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- E-Commerce Platform
---
