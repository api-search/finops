---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Hardware + Subscription
description: FinOps shape for Sensata Technologies — an industrial sensor manufacturer. Software / API spend is generally bundled into hardware-plus-connectivity contracts, not metered as a standalone API service. No public per-meter pricing or FOCUS column mapping was reconcilable.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sensata Technologies, Inc.
  ProviderName: Sensata Technologies
  PublisherName: Sensata Technologies, Inc.
  ServiceCategory: Industrial Sensors / IoT
  ServiceName: Sensata Technologies
layout: finops
meters:
- aggregation: sum
  description: Hardware units shipped under the contract (sensors, controllers, telematics devices)
  name: hardware_units
  unit: device
- aggregation: sum
  description: Connectivity / platform subscription for IoT-enabled devices
  name: connectivity_subscription
  unit: device-month
name: Sensata Technologies Finops
provider_name: Sensata Technologies
provider_slug: sensata-technologies
publisher_name: Sensata Technologies, Inc.
service_category: Industrial Sensors / IoT
slug: sensata-technologies-finops
source_filename: sensata-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.sensata.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sensata Technologies\nproviderId: sensata-technologies\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Sensors\n  - Industrial\n  - IoT\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Sensata Technologies — an industrial sensor manufacturer. Software / API\n  spend is generally bundled into hardware-plus-connectivity contracts, not metered as a standalone API\n  service. No public per-meter pricing or FOCUS column mapping was reconcilable.\nsources:\n  - https://www.sensata.com/\nnotes: Pricing, meters, and FOCUS column mappings are not publicly disclosed; reconciled to negotiated-contract\n  shape only.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Sensata Technologies, Inc.\nserviceCategory: Industrial Sensors / IoT\nbillingModel:\n  pricingCategory: Hardware + Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Sensata Technologies\n  ServiceCategory: Industrial Sensors / IoT\n  ProviderName: Sensata Technologies\n  PublisherName: Sensata Technologies, Inc.\n  InvoiceIssuerName: Sensata Technologies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: hardware_units\n    description: Hardware units shipped under the contract (sensors, controllers, telematics devices)\n    unit: device\n    aggregation: sum\n  - name: connectivity_subscription\n    description: Connectivity / platform subscription for IoT-enabled devices\n    unit: device-month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Sensata customer portal / Sensata IQ for connected fleets;\n      cost data lives on the negotiated invoice\
  \ rather than a usage API.\n  - name: Allocation\n    description: Allocate hardware and connectivity costs to the operational asset / fleet that the\n      device is deployed on.\n  - name: Optimization\n    description: Optimization is a procurement exercise — consolidate vendors, negotiate multi-year\n      hardware contracts, and right-size connected-device populations during contract renewals.\n  - name: Accountability\n    description: Operations / fleet management owns the device population; procurement owns commercial\n      terms with Sensata.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sensata-technologies/refs/heads/main/finops/sensata-technologies-finops.yml
sources:
- https://www.sensata.com/
specification: FinOps Framework
tags:
- Sensors
- Industrial
- IoT
- FinOps
- FOCUS
---
