---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hp-workforce-solutions-analytics-api-openapi.yml
  format: yaml
  label: HP Workforce Solutions Analytics API
  slug: hp-workforce-solutions-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hp/refs/heads/main/openapi/hp-workforce-solutions-analytics-api-openapi.yml
- filename: hp-printos-device-api-openapi.yml
  format: yaml
  label: HP PrintOS Device API
  slug: hp-printos-device-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hp/refs/heads/main/openapi/hp-printos-device-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual / Monthly per HP service contract
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Bundled (Service Contract)
description: 'FOCUS-aligned FinOps for HP developer APIs: API access is bundled with HP Active Care / Proactive Insights and HP Indigo PrintOS service contracts rather than billed per-call. Cost tracking lives at the device-fleet and PrintOS subscription level rather than per-API-request.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: HP Inc.
  ProviderName: HP
  PublisherName: HP Inc.
  ServiceCategory: Device Management & Industrial Printing
  ServiceName: HP Developer APIs
layout: finops
meters:
- aggregation: max
  description: Devices enrolled in HP Active Care / Proactive Insights; the primary cost dimension for the Workforce Solutions Analytics API contract.
  dimensions:
  - tenant
  - device_type
  - region
  name: enrolled_devices
  unit: device
- aggregation: max
  description: HP Indigo presses or industrial printers attached to PrintOS.
  dimensions:
  - print_shop
  - press_model
  name: printos_devices
  unit: device
- aggregation: max
  description: Named-user seats on the HP services contract where applicable.
  dimensions:
  - tenant
  - role
  name: contract_seats
  unit: seat
- aggregation: sum
  description: API call volume (Workforce Solutions Analytics + PrintOS Device API). Not directly billed but useful for capacity / fair-use monitoring.
  dimensions:
  - api
  - tenant
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes / events emitted per device into PrintOS or Proactive Insights cloud.
  dimensions:
  - device
  name: device_telemetry
  unit: event
name: Hp Finops
provider_name: HP
provider_slug: hp
publisher_name: HP Inc.
service_category: Device Management & Industrial Printing
slug: hp-finops
source_filename: hp-finops.yml
source_heading: FinOps Profile
source_url: https://developers.hp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: HP\nproviderId: hp\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Device Management\n  - Printing\n  - PrintOS\ndescription: 'FOCUS-aligned FinOps for HP developer APIs: API access is bundled with HP Active Care\n  / Proactive Insights and HP Indigo PrintOS service contracts rather than billed per-call. Cost\n  tracking lives at the device-fleet and PrintOS subscription level rather than per-API-request.'\nnotes: HP does not invoice for API consumption directly; all cost flows through the underlying device-management\n  or print-operations service contract.\nsources:\n  - https://developers.hp.com/\n  - https://www.hp.com/us-en/services/active-care.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: HP Inc.\nserviceCategory: Device Management & Industrial Printing\nbillingModel:\n  pricingCategory: Bundled (Service Contract)\n  billingFrequency: Annual / Monthly per HP service contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: HP Developer APIs\n  ServiceCategory: Device Management & Industrial Printing\n  ProviderName: HP\n  PublisherName: HP Inc.\n  InvoiceIssuerName: HP Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: enrolled_devices\n    description: Devices enrolled in HP Active Care / Proactive Insights; the primary cost dimension\n      for the Workforce Solutions Analytics API contract.\n    unit: device\n    aggregation: max\n    dimensions:\n      - tenant\n      - device_type\n      - region\n  - name: printos_devices\n    description: HP Indigo presses or industrial printers attached to PrintOS.\n    unit: device\n\
  \    aggregation: max\n    dimensions:\n      - print_shop\n      - press_model\n  - name: contract_seats\n    description: Named-user seats on the HP services contract where applicable.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n      - role\n  - name: api_requests\n    description: API call volume (Workforce Solutions Analytics + PrintOS Device API). Not directly\n      billed but useful for capacity / fair-use monitoring.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\n  - name: device_telemetry\n    description: Bytes / events emitted per device into PrintOS or Proactive Insights cloud.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - device\nprinciples:\n  - name: Visibility\n    description: Track device-fleet count and PrintOS press count via the HP services portal; reconcile\n      monthly against the HP service contract. API-level visibility comes from your own request logs\n      since HP does\
  \ not surface per-call billing.\n  - name: Allocation\n    description: Tag devices by business unit, site, and cost center. Allocate the bundled service-contract\n      cost across consuming teams pro-rata to enrolled-device count.\n  - name: Optimization\n    description: Decommission unused devices from Active Care / Proactive Insights enrollment to\n      reduce per-device contract cost. Consolidate PrintOS presses under fewer print shops where\n      operationally viable. Avoid excessive polling that triggers fair-use throttling.\n  - name: Accountability\n    description: Assign a contract owner for each HP service line. Review the renewal each year against\n      actual device-fleet utilization and API consumption volume.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hp/refs/heads/main/finops/hp-finops.yml
sources:
- https://developers.hp.com/
- https://www.hp.com/us-en/services/active-care.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Device Management
- Printing
- PrintOS
---
