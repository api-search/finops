---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Tuya operates the Tuya IoT Development Platform with project-scoped cloud usage; no public self-serve price list or FOCUS-aligned billing export is published, and Cloud Development Packages are quoted per project. FinOps shape is therefore documented at the Contact Sales level pending vendor disclosure.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tuya Inc.
  ProviderName: Tuya
  PublisherName: Tuya Inc.
  ServiceCategory: IoT Cloud Platform
  ServiceName: Tuya IoT Development Platform
layout: finops
meters:
- aggregation: sum
  description: Contracted Cloud Development Package line scoped to the project.
  dimensions:
  - project
  name: cloud_development_package
  unit: month
- aggregation: max
  description: Devices connected through the Tuya cloud under the project (basis for sizing the package).
  dimensions:
  - project
  - region
  name: connected_devices
  unit: device
name: Tuya Finops
provider_name: Tuya
provider_slug: tuya
publisher_name: Tuya Inc.
service_category: IoT Cloud Platform
slug: tuya-finops
source_filename: tuya-finops.yml
source_heading: FinOps Profile
source_url: https://developer.tuya.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tuya\nproviderId: tuya\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - IoT\n  - Smart Home\n  - Cloud Platform\n  - FinOps\n  - FOCUS\ndescription: Tuya operates the Tuya IoT Development Platform with project-scoped cloud usage; no public\n  self-serve price list or FOCUS-aligned billing export is published, and Cloud Development Packages are\n  quoted per project. FinOps shape is therefore documented at the Contact Sales level pending vendor disclosure.\nsources:\n  - https://developer.tuya.com/\n  - https://www.tuya.com/\nnotes: No public pricing endpoint reachable; Cloud Development Package prices are quoted per engagement.\n  Meters listed reflect typical IoT-platform billable lines but per-unit prices are not public.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tuya Inc.\nserviceCategory: IoT Cloud Platform\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Tuya IoT Development Platform\n  ServiceCategory: IoT Cloud Platform\n  ProviderName: Tuya\n  PublisherName: Tuya Inc.\n  InvoiceIssuerName: Tuya Inc.\n  BillingCurrency: USD\nmeters:\n  - name: cloud_development_package\n    description: Contracted Cloud Development Package line scoped to the project.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - project\n  - name: connected_devices\n    description: Devices connected through the Tuya cloud under the project (basis for sizing the package).\n    unit: device\n    aggregation: max\n    dimensions:\n      - project\n      - region\nprinciples:\n  - name: Visibility\n    description: Visibility is\
  \ via the Tuya developer console (project-scoped device counts and API call\n      logs); a public FOCUS export is not published.\n  - name: Allocation\n    description: Allocate Tuya spend per project / product line; Tuya's project model already maps cleanly\n      to a product or SKU in your portfolio.\n  - name: Optimization\n    description: Optimization happens by package right-sizing at contract renewal and by avoiding over-provisioning\n      of value-added services (AI, voice, OTA) that are not actively used by the device fleet.\n  - name: Accountability\n    description: An IoT product or hardware-platform owner manages the Tuya relationship per project;\n      finance approves the per-project Cloud Development Package contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tuya/refs/heads/main/finops/tuya-finops.yml
sources:
- https://developer.tuya.com/
- https://www.tuya.com/
specification: FinOps Framework
tags:
- IoT
- Smart Home
- Cloud Platform
- FinOps
- FOCUS
---
