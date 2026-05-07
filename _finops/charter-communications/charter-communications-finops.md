---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: charter-communications-spectrum-enterprise-api-openapi.yml
  format: yaml
  label: Charter Communications Spectrum Enterprise API
  slug: spectrum-enterprise-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/charter-communications/refs/heads/main/openapi/charter-communications-spectrum-enterprise-api-openapi.yml
- filename: charter-communications-bryte-iq-api-openapi.yml
  format: yaml
  label: Charter Communications Bryte IQ API
  slug: bryte-iq-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/charter-communications/refs/heads/main/openapi/charter-communications-bryte-iq-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Usage (Contract)
description: 'FOCUS-aligned FinOps framing for Charter Communications: enterprise telecom and NaaS services billed by contract; API access bundled with Spectrum Enterprise / Bryte IQ service charges rather than separately metered.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Charter Communications, Inc.
  ProviderName: Charter Communications
  PublisherName: Charter Communications, Inc.
  ServiceCategory: Telecommunications
  ServiceName: Spectrum Enterprise / Bryte IQ
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - location
  name: connectivity_circuits
  unit: circuit-month
- aggregation: max
  dimensions:
  - service
  - location
  name: bandwidth_committed
  unit: Mbps-month
- aggregation: sum
  name: naas_qod_sessions
  unit: session
- aggregation: sum
  name: managed_services
  unit: service-month
name: Charter Communications Finops
provider_name: Charter Communications
provider_slug: charter-communications
publisher_name: Charter Communications, Inc.
service_category: Telecommunications / Broadband
slug: charter-communications-finops
source_filename: charter-communications-finops.yml
source_heading: FinOps Profile
source_url: https://enterprise.spectrum.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Charter Communications\nproviderId: charter-communications\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Telecommunications\n  - Broadband\ndescription: 'FOCUS-aligned FinOps framing for Charter Communications: enterprise telecom and NaaS services\n  billed by contract; API access bundled with Spectrum Enterprise / Bryte IQ service charges rather\n  than separately metered.'\nnotes: API consumption is not separately priced. Meters reflect bundled telecom / NaaS billing surface.\nsources:\n  - https://enterprise.spectrum.com/\n  - https://www.brytenetwork.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Charter Communications,\
  \ Inc.\nserviceCategory: Telecommunications / Broadband\nbillingModel:\n  pricingCategory: Subscription + Usage (Contract)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Spectrum Enterprise / Bryte IQ\n  ServiceCategory: Telecommunications\n  ProviderName: Charter Communications\n  PublisherName: Charter Communications, Inc.\n  InvoiceIssuerName: Charter Communications, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: connectivity_circuits\n    unit: circuit-month\n    aggregation: sum\n    dimensions:\n      - service\n      - location\n  - name: bandwidth_committed\n    unit: Mbps-month\n    aggregation: max\n    dimensions:\n      - service\n      - location\n  - name: naas_qod_sessions\n    unit: session\n    aggregation: sum\n  - name: managed_services\n    unit: service-month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use\
  \ the Spectrum Enterprise customer portal and Bryte IQ usage reports for invoice and\n      service inventory data.\n  - name: Allocation\n    description: Allocate by site / circuit ID / NaaS subscription; tag in CMDB for chargeback.\n  - name: Optimization\n    description: Right-size committed bandwidth, exercise NaaS dynamic capacity for bursty workloads,\n      and consolidate sites at strategic POPs.\n  - name: Accountability\n    description: Telecom / network team owns Charter invoices; review monthly against forecast and SLA\n      credits.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/charter-communications/refs/heads/main/finops/charter-communications-finops.yml
sources:
- https://enterprise.spectrum.com/
- https://www.brytenetwork.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Telecommunications
- Broadband
---
