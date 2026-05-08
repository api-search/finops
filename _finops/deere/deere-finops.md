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
  - Adjustment
  pricingCategory: Bundled with Equipment / Subscription
description: 'FOCUS-aligned FinOps for John Deere developer APIs: there is no per-API-call invoice for the Operations Center / Precision Tech APIs. Cost flows through equipment, telematics (JDLink), and Operations Center subscriptions purchased via Deere dealers. Partner integrations may incur engineering and support costs but no metered API charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Deere & Company
  PricingCategory: Subscription
  ProviderName: John Deere
  PublisherName: Deere & Company
  ServiceCategory: Industry Platform
  ServiceName: John Deere Operations Center
  ServiceSubcategory: Precision Agriculture
layout: finops
meters:
- aggregation: count
  description: Count of Operations Center API calls. Not directly billed but useful for capacity planning and partner reporting.
  dimensions:
  - api
  - organization
  - client_id
  name: api_requests
  unit: request
- aggregation: count
  description: Webhook events delivered to partner endpoints.
  dimensions:
  - subscription
  - organization
  name: webhook_deliveries
  unit: event
- aggregation: max
  description: Count of connected machines under an organization (drives the underlying JDLink / Operations Center subscription bill).
  dimensions:
  - machine_type
  - organization
  name: connected_machines
  unit: machine
- aggregation: max
  description: Acres under management in Operations Center; common pricing dimension for precision-ag subscriptions.
  dimensions:
  - organization
  - region
  name: managed_acres
  unit: acre
name: Deere Finops
provider_name: John Deere
provider_slug: deere
publisher_name: Deere & Company
service_category: Industry Platform
slug: deere-finops
source_filename: deere-finops.yml
source_heading: FinOps Profile
source_url: https://developer.deere.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: John Deere\nproviderId: deere\npublisherName: Deere & Company\nserviceCategory: Industry Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Agriculture\n  - AgTech\n  - Operations Center\n  - Precision Agriculture\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for John Deere developer APIs: there is no per-API-call invoice\n  for the Operations Center / Precision Tech APIs. Cost flows through equipment, telematics\n  (JDLink), and Operations Center subscriptions purchased via Deere dealers. Partner integrations\n  may incur engineering and support costs but no metered API charge.'\nsources:\n  - https://developer.deere.com/\n\
  \  - https://www.deere.com/en/technology-products/precision-ag-technology/\nnotes: No metered API billing. FinOps shape attributes Deere spend to underlying equipment and\n  Operations Center subscriptions, with API integration as a no-fee add-on.\nbillingModel:\n  pricingCategory: Bundled with Equipment / Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: John Deere Operations Center\n  ServiceCategory: Industry Platform\n  ServiceSubcategory: Precision Agriculture\n  ProviderName: John Deere\n  PublisherName: Deere & Company\n  InvoiceIssuerName: Deere & Company\n  PricingCategory: Subscription\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_requests\n    description: Count of Operations Center API calls. Not directly billed but useful for capacity\n      planning and partner reporting.\n    unit: request\n    aggregation: count\n    dimensions:\n      - api\n\
  \      - organization\n      - client_id\n  - name: webhook_deliveries\n    description: Webhook events delivered to partner endpoints.\n    unit: event\n    aggregation: count\n    dimensions:\n      - subscription\n      - organization\n  - name: connected_machines\n    description: Count of connected machines under an organization (drives the underlying JDLink\n      / Operations Center subscription bill).\n    unit: machine\n    aggregation: max\n    dimensions:\n      - machine_type\n      - organization\n  - name: managed_acres\n    description: Acres under management in Operations Center; common pricing dimension for\n      precision-ag subscriptions.\n    unit: acre\n    aggregation: max\n    dimensions:\n      - organization\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the Operations Center admin console for connected-machine and acreage counts\n      and cross-reference dealer invoices for JDLink and Operations Center subscriptions. The\n      developer\
  \ portal exposes request volumes for partner capacity reporting.\n  - name: Allocation\n    description: Attribute Deere costs to the farming operation or business unit that owns the\n      Operations Center organization. Partner integrations should tag OAuth client_ids by\n      consuming product or customer.\n  - name: Optimization\n    description: Page large enumerations efficiently, subscribe to webhooks instead of polling,\n      cache slowly-changing field/boundary data locally, and align JDLink subscription tiers with\n      actual machine connectivity needs.\n  - name: Accountability\n    description: Designate a precision-ag lead at the customer who owns the Operations Center\n      seat allocation and the partner-integration roster. Review machine-and-acreage counts\n      annually before subscription renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/deere/refs/heads/main/finops/deere-finops.yml
sources:
- https://developer.deere.com/
- https://www.deere.com/en/technology-products/precision-ag-technology/
specification: FinOps Framework
tags:
- Agriculture
- AgTech
- Operations Center
- Precision Agriculture
- FinOps
- FOCUS
---
