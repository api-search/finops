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
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps scaffold for Lennar: partner-only API access with no public per-call pricing. Consumer-side telemetry mirrors the Azure APIM subscription used to access Lennar APIs.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Lennar Corporation
  ProviderName: Lennar
  PublisherName: Lennar Corporation
  ServiceCategory: Real Estate / API
  ServiceName: Lennar API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - subscription_key
  - environment
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - contract
  name: partner_fees
  unit: month
name: Lennar Finops
provider_name: Lennar
provider_slug: lennar
publisher_name: Lennar Corporation
service_category: Real Estate / API
slug: lennar-finops
source_filename: lennar-finops.yml
source_heading: FinOps Profile
source_url: https://azu-lndscapmu01e.portal.azure-api.net/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lennar\nproviderId: lennar\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Homebuilder\n  - Real Estate\n  - Fortune 500\n  - Mortgage\ndescription: 'FOCUS-aligned FinOps scaffold for Lennar: partner-only API access with no public per-call\n  pricing. Consumer-side telemetry mirrors the Azure APIM subscription used to access Lennar APIs.'\nnotes: Pricing is partner-contract driven; meters below describe the consumer-side observation surface\n  rather than billable Lennar line items.\nsources:\n  - https://azu-lndscapmu01e.portal.azure-api.net/\n  - https://www.lennar.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lennar\
  \ Corporation\nserviceCategory: Real Estate / API\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Lennar API\n  ServiceCategory: Real Estate / API\n  ProviderName: Lennar\n  PublisherName: Lennar Corporation\n  InvoiceIssuerName: Lennar Corporation\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - subscription_key\n      - environment\n  - name: partner_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Use Azure API Management analytics on the Lennar subscription to observe call volume\n      and error rates; Lennar does not expose a separate billing API.\n  - name: Allocation\n    description: Issue distinct APIM subscription keys per consuming team (sales, mortgage,\
  \ title) to\n      attribute call volume and any partner-contract draw.\n  - name: Optimization\n    description: Cache reference data (community / floor-plan lookups) and batch mortgage events to stay\n      under partner-subscription quotas.\n  - name: Accountability\n    description: Assign a Lennar partner contract owner who reviews APIM call volume and partner-contract\n      consumption monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lennar/refs/heads/main/finops/lennar-finops.yml
sources:
- https://azu-lndscapmu01e.portal.azure-api.net/
- https://www.lennar.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Homebuilder
- Real Estate
- Fortune 500
- Mortgage
---
