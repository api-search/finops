---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: docusign-openapi-original.yml
  format: yaml
  label: Docusign eSignature REST API
  slug: docusign-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-openapi-original.yml
- filename: docusign-admin-openapi-original.yml
  format: yaml
  label: Docusign Admin API
  slug: docusign-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-admin-openapi-original.yml
- filename: docusign-click-openapi-original.yml
  format: yaml
  label: Docusign Click API
  slug: docusign-click-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-click-openapi-original.yml
- filename: docusign-maestro-openapi-original.yml
  format: yaml
  label: Docusign Maestro API
  slug: docusign-maestro-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-maestro-openapi-original.yml
- filename: docusign-monitor-openapi-original.yml
  format: yaml
  label: Docusign Monitor API
  slug: docusign-monitor-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-monitor-openapi-original.yml
- filename: docusign-rooms-openapi-original.yml
  format: yaml
  label: Docusign Rooms API
  slug: docusign-rooms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-rooms-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat + Envelope Allowance
description: FOCUS-aligned FinOps for DocuSign.
focus_columns:
  BillingCurrency: USD
  ProviderName: DocuSign
  PublisherName: DocuSign
  ServiceCategory: E-Signature
  ServiceName: DocuSign
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: envelopes_sent
  unit: envelope
- aggregation: sum
  name: sms_sends
  unit: message
- aggregation: sum
  name: id_verifications
  unit: verification
- aggregation: sum
  name: api_calls
  unit: call
name: Docusign Finops
provider_name: Docusign
provider_slug: docusign
publisher_name: DocuSign
service_category: E-Signature
slug: docusign-finops
source_filename: docusign-finops.yml
source_heading: FinOps Profile
source_url: https://www.docusign.com/products/electronic-signature
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: DocuSign\nproviderId: docusign\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - E-Signature\ndescription: FOCUS-aligned FinOps for DocuSign.\nsources:\n  - https://www.docusign.com/products/electronic-signature\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: DocuSign\nserviceCategory: E-Signature\nbillingModel:\n  pricingCategory: Per-Seat + Envelope Allowance\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: DocuSign\n  ServiceCategory: E-Signature\n  ProviderName: DocuSign\n  PublisherName: DocuSign\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation:\
  \ max\n    dimensions:\n      - plan\n  - name: envelopes_sent\n    unit: envelope\n    aggregation: sum\n  - name: sms_sends\n    unit: message\n    aggregation: sum\n  - name: id_verifications\n    unit: verification\n    aggregation: sum\n  - name: api_calls\n    unit: call\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track DocuSign consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/finops/docusign-finops.yml
sources:
- https://www.docusign.com/products/electronic-signature
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- E-Signature
---
