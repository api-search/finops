---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: crm-oas
  format: yaml
  label: Zoho CRM
  slug: zoho-crm
  spec_type: OpenAPI
  url: https://github.com/zoho/crm-oas
- filename: zohodesk-oas
  format: yaml
  label: Zoho Desk
  slug: zoho-desk
  spec_type: OpenAPI
  url: https://github.com/zoho/zohodesk-oas
- filename: analytics-oas
  format: yaml
  label: Zoho Analytics
  slug: zoho-analytics
  spec_type: OpenAPI
  url: https://github.com/zoho/analytics-oas
- filename: bigin-oas
  format: yaml
  label: Zoho Bigin
  slug: zoho-bigin
  spec_type: OpenAPI
  url: https://github.com/zoho/bigin-oas
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription (Per-Product or Suite)
description: FOCUS-aligned FinOps for Zoho.
focus_columns:
  BillingCurrency: USD
  ProviderName: Zoho
  PublisherName: Zoho
  ServiceCategory: CRM and Suite
  ServiceName: Zoho
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - edition
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: api_credits
  unit: credit
- aggregation: max
  name: storage
  unit: GB-month
name: Zoho Finops
provider_name: Zoho
provider_slug: zoho
publisher_name: Zoho
service_category: CRM and Suite
slug: zoho-finops
source_filename: zoho-finops.yml
source_heading: FinOps Profile
source_url: https://www.zoho.com/crm/zohocrm-pricing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Zoho\nproviderId: zoho\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - CRM and Suite\ndescription: FOCUS-aligned FinOps for Zoho.\nsources:\n  - https://www.zoho.com/crm/zohocrm-pricing.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Zoho\nserviceCategory: CRM and Suite\nbillingModel:\n  pricingCategory: Per-User Subscription (Per-Product or Suite)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Zoho\n  ServiceCategory: CRM and Suite\n  ProviderName: Zoho\n  PublisherName: Zoho\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n\
  \      - product\n      - edition\n  - name: api_credits\n    unit: credit\n    aggregation: sum\n  - name: storage\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Zoho consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zoho/refs/heads/main/finops/zoho-finops.yml
sources:
- https://www.zoho.com/crm/zohocrm-pricing.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- CRM and Suite
---
