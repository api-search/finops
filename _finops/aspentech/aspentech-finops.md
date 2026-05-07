---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aspentech-inmation-web-openapi.yml
  format: yaml
  label: AspenTech Inmation Web API
  slug: inmation-web-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aspentech/refs/heads/main/openapi/aspentech-inmation-web-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise License (Subscription)
description: FOCUS-aligned FinOps shape for AspenTech — enterprise-licensed industrial software with APIs bundled into the platform license. There is no per-API consumption meter; cost optimization centers on license tier, tag/process counts, and concurrent user counts.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Aspen Technology, Inc.
  PricingCategory: Enterprise License
  ProviderName: AspenTech
  PublisherName: Aspen Technology, Inc.
  ServiceCategory: Industrial Software
  ServiceName: AspenTech
  ServiceSubcategory: Process Optimization & Industrial IoT
layout: finops
meters:
- aggregation: max
  description: Annual aspenONE / AIoT Hub / Inmation enterprise license fee
  dimensions:
  - product
  - site
  name: platform_license
  unit: year
- aggregation: max
  description: Inmation tag / process variable count licensed
  dimensions:
  - site
  name: tag_count
  unit: tag
- aggregation: max
  description: Concurrent named-user or floating-user license entitlement
  dimensions:
  - product
  - site
  name: concurrent_users
  unit: seat
- aggregation: sum
  description: Activity-only meter; API access is included in the platform license
  dimensions:
  - product
  - site
  name: api_calls
  unit: request
name: Aspentech Finops
provider_name: AspenTech
provider_slug: aspentech
publisher_name: Aspen Technology, Inc.
service_category: Industrial Software / Process Optimization
slug: aspentech-finops
source_filename: aspentech-finops.yml
source_heading: FinOps Profile
source_url: https://www.aspentech.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AspenTech\nproviderId: aspentech\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Industrial IoT\n  - Process Optimization\n  - Manufacturing\n  - Energy\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for AspenTech — enterprise-licensed industrial software with\n  APIs bundled into the platform license. There is no per-API consumption meter; cost optimization\n  centers on license tier, tag/process counts, and concurrent user counts.\nsources:\n  - https://www.aspentech.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: APIs are bundled with platform licenses; no separate API billing line. Meters below proxy the\n  underlying platform sizing levers.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Aspen Technology, Inc.\nserviceCategory: Industrial Software / Process Optimization\nbillingModel:\n  pricingCategory: Enterprise License (Subscription)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: AspenTech\n  ServiceCategory: Industrial Software\n  ServiceSubcategory: Process Optimization & Industrial IoT\n  ProviderName: AspenTech\n  PublisherName: Aspen Technology, Inc.\n  InvoiceIssuerName: Aspen Technology, Inc.\n  BillingCurrency: USD\n  PricingCategory: Enterprise License\nmeters:\n  - name: platform_license\n    description: Annual aspenONE / AIoT Hub / Inmation enterprise license fee\n    unit: year\n    aggregation: max\n    dimensions:\n      - product\n      - site\n  - name: tag_count\n    description: Inmation tag / process variable count licensed\n    unit: tag\n    aggregation: max\n \
  \   dimensions:\n      - site\n  - name: concurrent_users\n    description: Concurrent named-user or floating-user license entitlement\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n      - site\n  - name: api_calls\n    description: Activity-only meter; API access is included in the platform license\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - site\nprinciples:\n  - name: Visibility\n    description: Use Inmation server admin dashboards and the AspenTech license-management portal to\n      surface tag-count consumption and concurrent-user peaks against entitlement.\n  - name: Allocation\n    description: Allocate license cost by site / refinery / plant using AspenTech's site-keyed entitlements\n      and Inmation namespaces; tag spend by business unit in the consumer's CMDB.\n  - name: Optimization\n    description: Right-size tag-count entitlements annually; consolidate Inmation servers where possible;\n      retire unused\
  \ aspenONE seats at renewal.\n  - name: Accountability\n    description: Plant IT / process-control engineers own AspenTech spend; renewal cycles are typically\n      annual with site-by-site review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aspentech/refs/heads/main/finops/aspentech-finops.yml
sources:
- https://www.aspentech.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Industrial IoT
- Process Optimization
- Manufacturing
- Energy
- FinOps
- FOCUS
---
