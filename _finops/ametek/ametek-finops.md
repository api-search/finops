---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable
description: FOCUS-aligned FinOps placeholder for AMETEK. AMETEK is a hardware-led portfolio with no public API metered billing surface; spend is captured as capital equipment, calibration services, and software maintenance contracts rather than per-request charges.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AMETEK, Inc.
  ProviderName: AMETEK
  PublisherName: AMETEK, Inc.
  ServiceCategory: Electronic Instruments
  ServiceName: AMETEK
layout: finops
meters:
- aggregation: sum
  description: Placeholder; not billed as a developer line item
  dimensions:
  - consumer
  name: api_requests
  unit: request
name: Ametek Finops
provider_name: AMETEK
provider_slug: ametek
publisher_name: AMETEK, Inc.
service_category: Electronic Instruments
slug: ametek-finops
source_filename: ametek-finops.yml
source_heading: FinOps Profile
source_url: https://www.ametek.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AMETEK\nproviderId: ametek\npublisherName: AMETEK, Inc.\nserviceCategory: Electronic Instruments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Electronic Instruments\n  - Test and Measurement\ndescription: >-\n  FOCUS-aligned FinOps placeholder for AMETEK. AMETEK is a hardware-led\n  portfolio with no public API metered billing surface; spend is captured as\n  capital equipment, calibration services, and software maintenance contracts\n  rather than per-request charges.\nnotes: >-\n  No public API billing surface. Costs flow as hardware CapEx and software\n  maintenance.\nsources:\n  - https://www.ametek.com\n\
  billingModel:\n  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: AMETEK\n  ServiceCategory: Electronic Instruments\n  ProviderName: AMETEK\n  PublisherName: AMETEK, Inc.\n  InvoiceIssuerName: AMETEK, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: Placeholder; not billed as a developer line item\n    unit: request\n    aggregation: sum\n    dimensions:\n      - consumer\nprinciples:\n  - name: Visibility\n    description: >-\n      Visibility into AMETEK spend is via ERP / asset registers (instrument\n      serial numbers, calibration cycles), not API usage telemetry.\n  - name: Allocation\n    description: >-\n      Allocate AMETEK costs to the lab, manufacturing line, or business unit\n      that owns the underlying instrument.\n  - name: Optimization\n    description: >-\n      Optimize via instrument utilization, calibration scheduling, and\n\
  \      multi-year service contracts; not via request-level rate tuning.\n  - name: Accountability\n    description: >-\n      Budget ownership sits with engineering, R&D, and operations, not the\n      developer / FinOps API team.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ametek/refs/heads/main/finops/ametek-finops.yml
sources:
- https://www.ametek.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Electronic Instruments
- Test and Measurement
---
