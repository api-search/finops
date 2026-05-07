---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: appium-server-openapi.yaml
  format: yaml
  label: Appium Server API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appium/refs/heads/main/openapi/appium-server-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Open Source (No Charge)
description: 'FOCUS-aligned FinOps view for Appium: the framework itself is free and Apache-2.0 licensed with no direct charges. FinOps allocation should focus on the underlying compute (CI/CD runners, mac build hosts, device farms) and managed-cloud Appium services (BrowserStack, Sauce Labs, AWS Device Farm, LambdaTest) where actual spend occurs.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (no invoice)
  ProviderName: OpenJS Foundation / Appium
  PublisherName: OpenJS Foundation
  ServiceCategory: Test Automation / WebDriver
  ServiceName: Appium
layout: finops
meters:
- aggregation: sum
  description: Hours of self-hosted Appium server runtime, used to attribute infrastructure cost
  dimensions:
  - host_type
  - environment
  name: appium_server_hours
  unit: instance-hour
- aggregation: sum
  description: Connected-device wall-clock minutes consumed by test sessions
  dimensions:
  - platform
  - device_type
  name: device_minutes
  unit: minute
- aggregation: max
  description: Peak concurrent sessions, used for grid sizing
  dimensions:
  - environment
  name: parallel_sessions
  unit: session
- aggregation: sum
  description: Minutes consumed on managed Appium clouds (BrowserStack, Sauce Labs, AWS Device Farm, etc.) — actual billed spend
  dimensions:
  - cloud_provider
  - device_type
  name: cloud_grid_minutes
  unit: minute
name: Appium Finops
provider_name: Appium
provider_slug: appium
publisher_name: OpenJS Foundation
service_category: Test Automation / WebDriver
slug: appium-finops
source_filename: appium-finops.yml
source_heading: FinOps Profile
source_url: https://appium.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Appium\nproviderId: appium\npublisherName: OpenJS Foundation\nserviceCategory: Test Automation / WebDriver\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Open Source\n  - Test Automation\ndescription: 'FOCUS-aligned FinOps view for Appium: the framework itself is free and Apache-2.0 licensed\n  with no direct charges. FinOps allocation should focus on the underlying compute (CI/CD runners, mac\n  build hosts, device farms) and managed-cloud Appium services (BrowserStack, Sauce Labs, AWS Device Farm,\n  LambdaTest) where actual spend occurs.'\nsources:\n  - https://appium.io/\n  - https://github.com/appium/appium/blob/master/LICENSE\n\
  billingModel:\n  pricingCategory: Open Source (No Charge)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Appium\n  ServiceCategory: Test Automation / WebDriver\n  ProviderName: OpenJS Foundation / Appium\n  PublisherName: OpenJS Foundation\n  InvoiceIssuerName: N/A (no invoice)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: appium_server_hours\n    description: Hours of self-hosted Appium server runtime, used to attribute infrastructure cost\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - host_type\n      - environment\n  - name: device_minutes\n    description: Connected-device wall-clock minutes consumed by test sessions\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - platform\n      - device_type\n  - name: parallel_sessions\n    description: Peak concurrent sessions, used for grid sizing\n    unit: session\n    aggregation: max\n    dimensions:\n     \
  \ - environment\n  - name: cloud_grid_minutes\n    description: Minutes consumed on managed Appium clouds (BrowserStack, Sauce Labs, AWS Device Farm,\n      etc.) — actual billed spend\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - cloud_provider\n      - device_type\nprinciples:\n  - name: Visibility\n    description: Capture per-suite session duration and per-device minutes from CI/CD runs; correlate\n      to underlying compute or cloud-grid invoices.\n  - name: Allocation\n    description: Allocate test infrastructure cost to the consuming team or product based on session count\n      and device-minutes; tag CI jobs with team metadata.\n  - name: Optimization\n    description: Reuse driver sessions; parallelize across devices; prefer emulator/simulator where fidelity\n      allows; choose cloud-grid tier (parallel sessions) sized to peak rather than peak+headroom.\n  - name: Accountability\n    description: QE / Platform team owns the Appium grid contract or self-hosted\
  \ infra; product engineering\n      teams accountable for test-suite efficiency and minute consumption.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/appium/refs/heads/main/finops/appium-finops.yml
sources:
- https://appium.io/
- https://github.com/appium/appium/blob/master/LICENSE
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Open Source
- Test Automation
---
