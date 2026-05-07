---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cisco-voice-portal-call-control-openapi.yml
  format: yaml
  label: Cisco Voice Portal Call Control API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-voice-portal/refs/heads/main/openapi/cisco-voice-portal-call-control-openapi.yml
- filename: cisco-voice-portal-reporting-openapi.yml
  format: yaml
  label: Cisco Voice Portal Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-voice-portal/refs/heads/main/openapi/cisco-voice-portal-reporting-openapi.yml
- filename: cisco-voice-portal-administration-openapi.yml
  format: yaml
  label: Cisco Voice Portal Administration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-voice-portal/refs/heads/main/openapi/cisco-voice-portal-administration-openapi.yml
- filename: cisco-voice-portal-vxml-services-openapi.yml
  format: yaml
  label: Cisco Voice Portal VXML Services API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-voice-portal/refs/heads/main/openapi/cisco-voice-portal-vxml-services-openapi.yml
- filename: cisco-voice-portal-call-events-asyncapi.yml
  format: yaml
  label: Cisco Voice Portal Call Events API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-voice-portal/refs/heads/main/asyncapi/cisco-voice-portal-call-events-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Perpetual License
description: FOCUS-aligned FinOps shape for Cisco Unified Customer Voice Portal. Cost is driven by Smart Licensing entitlements for IVR / call-control ports under the Cisco Contact Center Enterprise bill of materials, not by per-API metering.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cisco Systems, Inc.
  ProviderName: Cisco
  PublisherName: Cisco Systems, Inc.
  ServiceCategory: Contact Center
  ServiceName: Cisco Voice Portal
layout: finops
meters:
- aggregation: max
  description: Licensed IVR ports for VXML self-service.
  dimensions:
  - region
  - environment
  name: ivr_ports
  unit: port
- aggregation: max
  description: Licensed call-control / queueing ports.
  dimensions:
  - region
  - environment
  name: call_control_ports
  unit: port
- aggregation: sum
  description: VM compute for CVP Call Server, VXML Server, OAMP, and Reporting Server.
  dimensions:
  - role
  - region
  name: cvp_server_compute
  unit: instance-hour
name: Cisco Voice Portal Finops
provider_name: Cisco Voice Portal
provider_slug: cisco-voice-portal
publisher_name: Cisco Systems, Inc.
service_category: Contact Center
slug: cisco-voice-portal-finops
source_filename: cisco-voice-portal-finops.yml
source_heading: FinOps Profile
source_url: https://www.cisco.com/c/en/us/products/customer-collaboration/unified-customer-voice-portal/index.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Voice Portal\nproviderId: cisco-voice-portal\npublisherName: Cisco Systems, Inc.\nserviceCategory: Contact Center\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Contact Center\n  - IVR\n  - Voice\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Cisco Unified Customer Voice Portal. Cost is driven by\n  Smart Licensing entitlements for IVR / call-control ports under the Cisco Contact Center Enterprise\n  bill of materials, not by per-API metering.\nnotes: Per-API meters below are placeholders modeled on operational dimensions; real billing flows\n  through Cisco Contact Center licensing line items\
  \ and underlying server / TDM gateway costs.\nsources:\n  - https://www.cisco.com/c/en/us/products/customer-collaboration/unified-customer-voice-portal/index.html\nbillingModel:\n  pricingCategory: Subscription + Perpetual License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Cisco Voice Portal\n  ServiceCategory: Contact Center\n  ProviderName: Cisco\n  PublisherName: Cisco Systems, Inc.\n  InvoiceIssuerName: Cisco Systems, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: ivr_ports\n    description: Licensed IVR ports for VXML self-service.\n    unit: port\n    aggregation: max\n    dimensions:\n      - region\n      - environment\n  - name: call_control_ports\n    description: Licensed call-control / queueing ports.\n    unit: port\n    aggregation: max\n    dimensions:\n      - region\n      - environment\n  - name: cvp_server_compute\n    description:\
  \ VM compute for CVP Call Server, VXML Server, OAMP, and Reporting Server.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - role\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the CVP Reporting Server, Cisco Smart Software Manager, and Contact Center\n      management portal to observe port utilization and license consumption.\n  - name: Allocation\n    description: Allocate IVR / port costs to the contact center business unit; chargeback by line\n      of business using call-type / dialed-number reporting.\n  - name: Optimization\n    description: Right-size IVR port counts to peak concurrent call volume, retire low-traffic IVR\n      applications, and consolidate VXML applications onto shared CVP servers.\n  - name: Accountability\n    description: Contact Center operations owner is accountable for CVP port forecasting, license\n      renewals, and IVR application lifecycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-voice-portal/refs/heads/main/finops/cisco-voice-portal-finops.yml
sources:
- https://www.cisco.com/c/en/us/products/customer-collaboration/unified-customer-voice-portal/index.html
specification: FinOps Framework
tags:
- Contact Center
- IVR
- Voice
- FinOps
- FOCUS
---
