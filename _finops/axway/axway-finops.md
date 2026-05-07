---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: axway-amplify-platform-openapi-original.json
  format: json
  label: Axway Amplify Platform API
  slug: axway-amplify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/axway/refs/heads/main/openapi/axway-amplify-platform-openapi-original.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Axway: subscription / quote-based licensing for enterprise API management, integration, and MFT software. Costs are negotiated rather than usage-metered at the provider level.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Axway Software SA
  PricingCategory: Subscription
  ProviderName: Axway
  PublisherName: Axway Software SA
  ServiceCategory: Developer Tools / API
  ServiceName: Axway
layout: finops
meters:
- aggregation: max
  description: Per-seat or named-user licenses where applicable
  dimensions:
  - product
  - environment
  name: subscription_seats
  unit: seat
- aggregation: sum
  description: API gateway transactions billed under Amplify-hosted SKUs
  dimensions:
  - product
  - environment
  - region
  name: api_transactions
  unit: transaction
- aggregation: max
  description: Number of managed deployments (dev/test/staging/prod)
  dimensions:
  - product
  - region
  name: managed_environments
  unit: environment
- aggregation: sum
  description: File transfer volume for SecureTransport / Transfer CFT
  dimensions:
  - product
  name: mft_volume
  unit: GB
name: Axway Finops
provider_name: Axway
provider_slug: axway
publisher_name: Axway Software SA
service_category: Developer Tools / API
slug: axway-finops
source_filename: axway-finops.yml
source_heading: FinOps Profile
source_url: https://www.axway.com/en/axway-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Axway\nproviderId: axway\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - API Management\n  - Enterprise\n  - Integration\n  - Security\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Axway: subscription / quote-based licensing for enterprise API\n  management, integration, and MFT software. Costs are negotiated rather than usage-metered at the provider\n  level.'\nnotes: Axway pricing is contact-sales only; FinOps shape derived from product portfolio rather than published\n  rate cards.\nsources:\n  - https://www.axway.com/en/axway-pricing\n  - https://www.axway.com/en/products\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Axway Software\
  \ SA\nserviceCategory: Developer Tools / API\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Axway\n  ServiceCategory: Developer Tools / API\n  ProviderName: Axway\n  PublisherName: Axway Software SA\n  InvoiceIssuerName: Axway Software SA\n  PricingCategory: Subscription\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_seats\n    description: Per-seat or named-user licenses where applicable\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n      - environment\n  - name: api_transactions\n    description: API gateway transactions billed under Amplify-hosted SKUs\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - product\n      - environment\n      - region\n  - name: managed_environments\n    description: Number of managed deployments (dev/test/staging/prod)\n\
  \    unit: environment\n    aggregation: max\n    dimensions:\n      - product\n      - region\n  - name: mft_volume\n    description: File transfer volume for SecureTransport / Transfer CFT\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Track Axway entitlements and consumption through Amplify Platform Reporting and license\n      management dashboards; export to internal cost systems.\n  - name: Allocation\n    description: Tag environments and APIs with team / business-unit metadata in Amplify Central to allocate\n      subscription cost across consumers.\n  - name: Optimization\n    description: Right-size environments at renewal; consolidate gateways, retire unused APIs, and negotiate\n      multi-year terms for volume discount.\n  - name: Accountability\n    description: Assign API product owners in Amplify Engage; review utilization against contracted volumes\n      quarterly to avoid over-provisioning.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/axway/refs/heads/main/finops/axway-finops.yml
sources:
- https://www.axway.com/en/axway-pricing
- https://www.axway.com/en/products
specification: FinOps Framework
tags:
- API Management
- Enterprise
- Integration
- Security
- FinOps
- FOCUS
---
