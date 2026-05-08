---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: qlik-sense-cloud-rest-api-openapi.yml
  format: yaml
  label: Qlik Cloud Platform REST API
  slug: qlik-cloud-platform-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense/refs/heads/main/openapi/qlik-sense-cloud-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for Qlik Cloud Analytics — a tiered SaaS analytics subscription billed by capacity / users rather than metered API calls. Specific tier prices are not public.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: QlikTech International AB
  ProviderName: Qlik
  PublisherName: QlikTech International AB
  ServiceCategory: Analytics
  ServiceName: Qlik Cloud Analytics
layout: finops
meters:
- aggregation: max
  name: subscription_users
  unit: seat
- aggregation: max
  name: data_capacity
  unit: GB
name: Qlik Sense Finops
provider_name: Qlik Sense
provider_slug: qlik-sense
publisher_name: QlikTech International AB
service_category: Analytics
slug: qlik-sense-finops
source_filename: qlik-sense-finops.yml
source_heading: FinOps Profile
source_url: https://www.qlik.com/us/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Qlik Sense\nproviderId: qlik-sense\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Analytics\n  - Business Intelligence\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Qlik Cloud Analytics — a tiered SaaS analytics subscription\n  billed by capacity / users rather than metered API calls. Specific tier prices are not public.\nnotes: Qlik's public pricing surface does not expose plan-tier prices to anonymous fetch; the FinOps\n  record keeps generic SaaS-subscription meters without inventing per-user rates.\nsources:\n  - https://www.qlik.com/us/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: QlikTech International AB\nserviceCategory:\
  \ Analytics\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Qlik Cloud Analytics\n  ServiceCategory: Analytics\n  ProviderName: Qlik\n  PublisherName: QlikTech International AB\n  InvoiceIssuerName: QlikTech International AB\n  BillingCurrency: USD\nmeters:\n  - name: subscription_users\n    unit: seat\n    aggregation: max\n  - name: data_capacity\n    unit: GB\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Capacity and seat usage are observable in the Qlik Cloud Management Console; cost itself\n      sits on the Qlik subscription invoice.\n  - name: Allocation\n    description: Allocate seats and capacity by space / business unit using Qlik's tenant and space\n      governance.\n  - name: Optimization\n    description: Right-size capacity tier, retire unused users, and consolidate spaces; renegotiate\n      capacity at renewal.\n  - name:\
  \ Accountability\n    description: Spend is owned by the analytics / data platform team that holds the Qlik subscription.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/qlik-sense/refs/heads/main/finops/qlik-sense-finops.yml
sources:
- https://www.qlik.com/us/pricing
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- FinOps
- FOCUS
---
