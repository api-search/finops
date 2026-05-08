---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mintlify-openapi.yml
  format: yaml
  label: Mintlify Update API
  slug: update-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mintlify/refs/heads/main/openapi/mintlify-openapi.yml
- filename: mintlify-openapi.yml
  format: yaml
  label: Mintlify Agent API
  slug: agent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mintlify/refs/heads/main/openapi/mintlify-openapi.yml
- filename: mintlify-openapi.yml
  format: yaml
  label: Mintlify Assistant API
  slug: assistant-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mintlify/refs/heads/main/openapi/mintlify-openapi.yml
- filename: mintlify-openapi.yml
  format: yaml
  label: Mintlify Analytics API
  slug: analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mintlify/refs/heads/main/openapi/mintlify-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Mintlify: flat per-month subscription tier (Pro $250/month base, +$20 per additional editor seat) with a metered AI Assistant credit overage at $0.01/credit. Free Hobby tier and contact-sales Enterprise tier round out the model.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Mintlify, Inc.
  ProviderName: Mintlify
  PublisherName: Mintlify, Inc.
  ServiceCategory: Developer Tools
  ServiceName: Mintlify
  ServiceSubcategory: Documentation
layout: finops
meters:
- aggregation: sum
  dimensions:
  - account
  name: pro_subscription
  unit: month
- aggregation: sum
  dimensions:
  - account
  - assigned_user
  name: editor_seats_addon
  unit: seat-month
- aggregation: sum
  dimensions:
  - account
  - assistant_type
  name: ai_assistant_credits_consumed
  unit: credit
- aggregation: sum
  dimensions:
  - account
  name: ai_assistant_credit_overage
  unit: credit
- aggregation: count
  dimensions:
  - account
  name: enterprise_contract
  unit: contract-year
name: Mintlify Finops
provider_name: Mintlify
provider_slug: mintlify
publisher_name: Mintlify, Inc.
service_category: Documentation / Developer Tools
slug: mintlify-finops
source_filename: mintlify-finops.yml
source_heading: FinOps Profile
source_url: https://mintlify.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mintlify\nproviderId: mintlify\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Documentation\n  - Developer Tools\ndescription: 'FOCUS-aligned FinOps for Mintlify: flat per-month subscription tier (Pro $250/month base,\n  +$20 per additional editor seat) with a metered AI Assistant credit overage at $0.01/credit. Free\n  Hobby tier and contact-sales Enterprise tier round out the model.'\nsources:\n  - https://mintlify.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mintlify, Inc.\nserviceCategory: Documentation / Developer Tools\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Mintlify\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: Documentation\n  ProviderName: Mintlify\n  PublisherName: Mintlify, Inc.\n  InvoiceIssuerName: Mintlify, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: pro_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\n  - name: editor_seats_addon\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - account\n      - assigned_user\n  - name: ai_assistant_credits_consumed\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - account\n      - assistant_type\n  - name: ai_assistant_credit_overage\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - account\n  - name: enterprise_contract\n    unit: contract-year\n    aggregation: count\n    dimensions:\n    \
  \  - account\nprinciples:\n  - name: Visibility\n    description: Pull AI credit consumption from the Mintlify dashboard usage report; reconcile against\n      monthly invoice to spot overage.\n  - name: Allocation\n    description: Tag editor seats to the engineering / docs team that consumes them; allocate AI credit\n      cost to the product line whose docs are queried (use Assistant analytics on Enterprise).\n  - name: Optimization\n    description: Trim unused editor seats — each costs $20/month above the 5 included; cap AI Assistant\n      to internal IP ranges or authenticated users to avoid runaway public-traffic credit overage; move\n      to annual billing for ~15% savings.\n  - name: Accountability\n    description: Designate a docs platform owner; review AI credit overage monthly; cap Assistant\n      credits via product configuration to prevent surprise charges.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mintlify/refs/heads/main/finops/mintlify-finops.yml
sources:
- https://mintlify.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Documentation
- Developer Tools
---
