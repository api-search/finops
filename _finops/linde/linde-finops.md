---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD/EUR/GBP
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Bundled with Supply Agreement
description: 'FOCUS-aligned FinOps scaffold for Linde: customer / partner-only digital integrations with no public per-call API pricing. Consumer-side telemetry tracks against the underlying supply / engineering agreement rather than metered API invoices.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Linde plc
  ProviderName: Linde
  PublisherName: Linde plc
  ServiceCategory: Industrial Gases / API
  ServiceName: Linde API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - integration
  - environment
  - customer
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - asset
  - site
  name: telemetry_events
  unit: event
- aggregation: sum
  dimensions:
  - partner
  - document_type
  name: edi_messages
  unit: message
name: Linde Finops
provider_name: Linde
provider_slug: linde
publisher_name: Linde plc
service_category: Industrial Gases / API
slug: linde-finops
source_filename: linde-finops.yml
source_heading: FinOps Profile
source_url: https://www.linde.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Linde\nproviderId: linde\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Industrial Gases\n  - Engineering\n  - Chemistry\ndescription: 'FOCUS-aligned FinOps scaffold for Linde: customer / partner-only digital integrations with\n  no public per-call API pricing. Consumer-side telemetry tracks against the underlying supply / engineering\n  agreement rather than metered API invoices.'\nnotes: Pricing is bundled into customer agreements. Meters describe the consumer-side observation surface.\nsources:\n  - https://www.linde.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Linde plc\nserviceCategory: Industrial Gases / API\nbillingModel:\n\
  \  pricingCategory: Bundled with Supply Agreement\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/GBP\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Linde API\n  ServiceCategory: Industrial Gases / API\n  ProviderName: Linde\n  PublisherName: Linde plc\n  InvoiceIssuerName: Linde plc\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n      - environment\n      - customer\n  - name: telemetry_events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - asset\n      - site\n  - name: edi_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - partner\n      - document_type\nprinciples:\n  - name: Visibility\n    description: Track API and EDI message volumes through your own integration platform / observability\n      stack; Linde does not expose a public usage API.\n  - name: Allocation\n    description: Tag\
  \ integrations by site, customer cost center, and gas / engineering product line so\n      digital touchpoints can be associated with the right supply contract.\n  - name: Optimization\n    description: Batch order and replenishment messages to agreed EDI cadences; sample telemetry rather\n      than streaming where supply contracts allow.\n  - name: Accountability\n    description: Assign a Linde customer / digital integration owner per contract who reconciles digital\n      integration cost-of-ownership against supply spend.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/linde/refs/heads/main/finops/linde-finops.yml
sources:
- https://www.linde.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Industrial Gases
- Engineering
- Chemistry
---
