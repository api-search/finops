---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cloudzero-api-openapi.yml
  format: yaml
  label: CloudZero API
  slug: api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudzero/refs/heads/main/openapi/cloudzero-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for the CloudZero platform itself: a contact-sales subscription that scales with ingested cloud spend, with unlimited user seats. CloudZero is a FOCUS member organization and exports cost data in FOCUS format to its customers.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: CloudZero, Inc.
  PricingCategory: Subscription
  PricingUnit: subscription-month
  ProviderName: CloudZero
  PublisherName: CloudZero, Inc.
  ServiceCategory: FinOps Platform
  ServiceName: CloudZero
layout: finops
meters:
- aggregation: sum
  description: Recurring CloudZero platform subscription fee.
  dimensions:
  - plan
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Cloud spend (USD) ingested into the CloudZero platform across connected accounts.
  dimensions:
  - cloud_provider
  - account
  name: cloud_spend_ingested
  unit: usd
- aggregation: max
  description: Active user seats (CloudZero markets unlimited seats; may still appear on invoice).
  dimensions:
  - role
  name: user_seats
  unit: seat-month
- aggregation: max
  description: Connected data sources (AWS, Azure, GCP, Snowflake, Kubernetes, SaaS).
  dimensions:
  - source_type
  name: data_sources
  unit: source
name: Cloudzero Finops
provider_name: CloudZero
provider_slug: cloudzero
publisher_name: CloudZero, Inc.
service_category: FinOps Platform
slug: cloudzero-finops
source_filename: cloudzero-finops.yml
source_heading: FinOps Profile
source_url: https://www.cloudzero.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CloudZero\nproviderId: cloudzero\npublisherName: CloudZero, Inc.\nserviceCategory: FinOps Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud Cost Management\n  - Cost Allocation\n  - Unit Economics\nnotes: CloudZero is itself a FinOps platform, so this artifact describes the cost surface of consuming\n  the CloudZero product. Public pricing numbers are not disclosed (contact-sales), so the focus columns\n  and meters reflect the structural shape of a CloudZero subscription invoice rather than verified line-items.\ndescription: 'FOCUS-aligned FinOps for the CloudZero platform itself:\
  \ a contact-sales subscription that\n  scales with ingested cloud spend, with unlimited user seats. CloudZero is a FOCUS member organization\n  and exports cost data in FOCUS format to its customers.'\nsources:\n  - https://www.cloudzero.com/pricing/\n  - https://www.cloudzero.com/focus/\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: CloudZero\n  ServiceCategory: FinOps Platform\n  ProviderName: CloudZero\n  PublisherName: CloudZero, Inc.\n  InvoiceIssuerName: CloudZero, Inc.\n  PricingCategory: Subscription\n  PricingUnit: subscription-month\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_fee\n    description: Recurring CloudZero platform subscription fee.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: cloud_spend_ingested\n    description: Cloud spend (USD) ingested\
  \ into the CloudZero platform across connected accounts.\n    unit: usd\n    aggregation: sum\n    dimensions:\n      - cloud_provider\n      - account\n  - name: user_seats\n    description: Active user seats (CloudZero markets unlimited seats; may still appear on invoice).\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - role\n  - name: data_sources\n    description: Connected data sources (AWS, Azure, GCP, Snowflake, Kubernetes, SaaS).\n    unit: source\n    aggregation: max\n    dimensions:\n      - source_type\nprinciples:\n  - name: Visibility\n    description: Use CloudZero's own dashboards and the FOCUS export to see what you spend on CloudZero\n      itself, not just the cloud spend it ingests.\n  - name: Allocation\n    description: Tag the CloudZero subscription line in your AP system to the FinOps practice or the team\n      that owns FinOps tooling; flow the FOCUS-format export back into your data warehouse alongside CUR.\n  - name: Optimization\n    description:\
  \ Right-size the contract against the cloud spend you actually ingest into CloudZero; consolidate\n      data sources rather than activating them speculatively, since pricing scales with ingested spend.\n  - name: Accountability\n    description: Assign FinOps platform ownership to a single accountable owner who reviews monthly utilization\n      against the contract during the CloudZero-led FinOps Account Manager check-in.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudzero/refs/heads/main/finops/cloudzero-finops.yml
sources:
- https://www.cloudzero.com/pricing/
- https://www.cloudzero.com/focus/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud Cost Management
- Cost Allocation
- Unit Economics
---
