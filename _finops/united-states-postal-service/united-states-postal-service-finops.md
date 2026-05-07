---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: united-states-postal-service-addresses-openapi.yml
  format: yaml
  label: USPS Addresses API
  slug: usps-addresses-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/openapi/united-states-postal-service-addresses-openapi.yml
- filename: united-states-postal-service-tracking-openapi.yml
  format: yaml
  label: USPS Tracking API
  slug: usps-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/openapi/united-states-postal-service-tracking-openapi.yml
- filename: united-states-postal-service-domestic-prices-openapi.yml
  format: yaml
  label: USPS Domestic Prices API
  slug: usps-domestic-prices-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/openapi/united-states-postal-service-domestic-prices-openapi.yml
- filename: united-states-postal-service-carrier-pickup-openapi.yml
  format: yaml
  label: USPS Carrier Pickup API
  slug: usps-carrier-pickup-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/openapi/united-states-postal-service-carrier-pickup-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Purchase
  pricingCategory: Pay-Per-Label (postage)
description: FOCUS-aligned FinOps for USPS Developer APIs. The APIs themselves are not metered as a per-call charge. Real spend lives downstream - postage paid per shipping label via an Enterprise Payment Account. The API surface is the cost-control point for label generation, address validation efficiency, and tracking polling rather than itself a billable line.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: United States Postal Service
  ProviderName: United States Postal Service
  PublisherName: United States Postal Service
  ServiceCategory: Postal / Shipping
  ServiceName: USPS Developer APIs
layout: finops
meters:
- aggregation: sum
  description: Labels generated through the Labels APIs; postage cost is debited from the Enterprise Payment Account per label based on USPS rate cards.
  dimensions:
  - service_class
  - origin_zip
  - destination_zip
  - weight
  name: shipping_labels
  unit: label
- aggregation: sum
  description: Calls to the Addresses API for validation; not separately billed but tracked against portal quota.
  name: address_validation_calls
  unit: request
- aggregation: sum
  description: Calls to the Tracking API; not separately billed but tracked against portal quota.
  name: tracking_calls
  unit: request
- aggregation: sum
  description: Calls to Domestic / International Pricing APIs for rate quoting; not separately billed.
  name: pricing_calls
  unit: request
name: United States Postal Service Finops
provider_name: United States Postal Service
provider_slug: united-states-postal-service
publisher_name: United States Postal Service
service_category: Postal / Shipping
slug: united-states-postal-service-finops
source_filename: united-states-postal-service-finops.yml
source_heading: FinOps Profile
source_url: https://developers.usps.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: United States Postal Service\nproviderId: united-states-postal-service\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Government\n  - Postal Service\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for USPS Developer APIs. The APIs themselves are not metered as\n  a per-call charge. Real spend lives downstream - postage paid per shipping label via an Enterprise\n  Payment Account. The API surface is the cost-control point for label generation, address validation\n  efficiency, and tracking polling rather than itself a billable line.\nsources:\n  - https://developers.usps.com\n  - https://developers.usps.com/getting-started\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: United States Postal Service\nserviceCategory: Postal / Shipping\nbillingModel:\n  pricingCategory: Pay-Per-Label (postage)\n  billingFrequency: Continuous Settlement\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: USPS Developer APIs\n  ServiceCategory: Postal / Shipping\n  ProviderName: United States Postal Service\n  PublisherName: United States Postal Service\n  InvoiceIssuerName: United States Postal Service\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: shipping_labels\n    description: Labels generated through the Labels APIs; postage cost is debited from the Enterprise\n      Payment Account per label based on USPS rate cards.\n    unit: label\n    aggregation: sum\n    dimensions:\n      - service_class\n      - origin_zip\n      - destination_zip\n      - weight\n  - name: address_validation_calls\n    description: Calls to the Addresses API for validation; not separately billed but tracked against\n\
  \      portal quota.\n    unit: request\n    aggregation: sum\n  - name: tracking_calls\n    description: Calls to the Tracking API; not separately billed but tracked against portal quota.\n    unit: request\n    aggregation: sum\n  - name: pricing_calls\n    description: Calls to Domestic / International Pricing APIs for rate quoting; not separately\n      billed.\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: USPS does not expose a usage API for cost; track Enterprise Payment Account postage\n      debits and correlate to label-creation events from your own integration logs.\n  - name: Allocation\n    description: Tag every Labels API call with cost-center, customer-order, and origin-warehouse\n      so postage debits can be allocated post-fact via internal reconciliation.\n  - name: Optimization\n    description: Reduce postage spend by selecting the right service class per shipment, cleansing\n      addresses up-front via the Addresses\
  \ API, and avoiding redundant label re-generation. Reduce\n      portal quota pressure by caching address-validation and pricing responses.\n  - name: Accountability\n    description: Assign Enterprise Payment Account ownership to a finance/operations stakeholder;\n      submit USPS API service requests to right-size quota for the production workload.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/finops/united-states-postal-service-finops.yml
sources:
- https://developers.usps.com
- https://developers.usps.com/getting-started
specification: FinOps Framework
tags:
- Government
- Postal Service
- FinOps
- FOCUS
---
