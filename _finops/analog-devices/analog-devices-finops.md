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
  pricingCategory: Hardware Purchase
description: FOCUS-aligned FinOps for Analog Devices. ADI's developer software (libiio, pyadi-iio, no-OS, CodeFusion Studio) is free open-source; spend on ADI flows as bill-of-material direct cost for silicon and evaluation hardware, invoiced via distributors or direct sales, not as API consumption.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Analog Devices, Inc. (or distributor of record)
  ProviderName: Analog Devices
  PublisherName: Analog Devices, Inc.
  ServiceCategory: Semiconductors
  ServiceName: Analog Devices
layout: finops
meters:
- aggregation: sum
  description: Count of ADI integrated circuits ordered
  dimensions:
  - part_number
  - distributor
  - program
  name: silicon_units_purchased
  unit: unit
- aggregation: sum
  description: Evaluation / development hardware purchases
  dimensions:
  - board_family
  - distributor
  name: evaluation_boards_purchased
  unit: unit
- aggregation: count
  description: Open-source SDK downloads (free; tracked for adoption only)
  dimensions:
  - package
  name: sdk_downloads
  unit: download
name: Analog Devices Finops
provider_name: Analog Devices
provider_slug: analog-devices
publisher_name: Analog Devices, Inc.
service_category: Semiconductors
slug: analog-devices-finops
source_filename: analog-devices-finops.yml
source_heading: FinOps Profile
source_url: https://www.analog.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Analog Devices\nproviderId: analog-devices\npublisherName: Analog Devices, Inc.\nserviceCategory: Semiconductors\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Semiconductors\n  - Embedded Systems\n  - Open Source\ndescription: >-\n  FOCUS-aligned FinOps for Analog Devices. ADI's developer software (libiio,\n  pyadi-iio, no-OS, CodeFusion Studio) is free open-source; spend on ADI flows\n  as bill-of-material direct cost for silicon and evaluation hardware,\n  invoiced via distributors or direct sales, not as API consumption.\nnotes: >-\n  No SaaS metered API. The \"billing model\" reflects hardware\
  \ procurement, not\n  API metering.\nsources:\n  - https://www.analog.com\n  - https://github.com/analogdevicesinc\nbillingModel:\n  pricingCategory: Hardware Purchase\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Analog Devices\n  ServiceCategory: Semiconductors\n  ProviderName: Analog Devices\n  PublisherName: Analog Devices, Inc.\n  InvoiceIssuerName: Analog Devices, Inc. (or distributor of record)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: silicon_units_purchased\n    description: Count of ADI integrated circuits ordered\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - part_number\n      - distributor\n      - program\n  - name: evaluation_boards_purchased\n    description: Evaluation / development hardware purchases\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - board_family\n      - distributor\n  - name: sdk_downloads\n    description: Open-source\
  \ SDK downloads (free; tracked for adoption only)\n    unit: download\n    aggregation: count\n    dimensions:\n      - package\nprinciples:\n  - name: Visibility\n    description: >-\n      Track ADI spend through ERP / procurement systems and distributor\n      portals; SDK adoption can be tracked through GitHub release downloads\n      and EngineerZone forum activity.\n  - name: Allocation\n    description: >-\n      Allocate ADI silicon costs to BOMs and product lines; SDK use carries no\n      direct cost so no allocation tag is needed.\n  - name: Optimization\n    description: >-\n      Optimization levers are part consolidation across BOMs, multi-source\n      qualification, and volume agreements with ADI / distributors. SDK use is\n      free.\n  - name: Accountability\n    description: >-\n      Procurement and hardware engineering own the cost; software / firmware\n      teams own the open-source SDK consumption (no chargeback).\nmaintainers:\n  - FN: API Evangelist\n    email:\
  \ info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/analog-devices/refs/heads/main/finops/analog-devices-finops.yml
sources:
- https://www.analog.com
- https://github.com/analogdevicesinc
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Semiconductors
- Embedded Systems
- Open Source
---
