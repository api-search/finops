---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: broadridge-wealth-openapi.yml
  format: yaml
  label: Broadridge Wealth Management API
  slug: broadridge-wealth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/broadridge/refs/heads/main/openapi/broadridge-wealth-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Subscription + Volume
description: 'FOCUS-aligned FinOps for Broadridge: enterprise platform subscriptions across Wealth Operations, Asset Management / Galaxia Fund Data, and Investor Communications. Pricing is contracted per platform subscription and tied to accounts, AUM, and communications volume; APIs ship with the underlying platform rather than being separately metered.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Broadridge Financial Solutions, Inc.
  PricingCategory: Standard
  PricingUnit: subscription-month
  ProviderName: Broadridge
  PublisherName: Broadridge Financial Solutions, Inc.
  ServiceCategory: Financial Services Technology
  ServiceName: Broadridge
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription fee for the contracted Broadridge platform module.
  dimensions:
  - product_line
  - tier
  name: platform_subscription
  unit: month
- aggregation: max
  description: Number of accounts under management on the Wealth Operations / clearing platform.
  dimensions:
  - product_line
  - region
  name: accounts
  unit: account
- aggregation: max
  description: Assets Under Management used as a billing dimension for asset-management modules.
  dimensions:
  - product_line
  - currency
  name: aum
  unit: currency
- aggregation: sum
  description: Investor communications (proxy, regulatory, statements) processed.
  dimensions:
  - communication_type
  - channel
  name: investor_communications
  unit: communication
- aggregation: sum
  description: Galaxia fund-data records distributed for regulatory reporting.
  dimensions:
  - regulation
  - fund
  name: fund_data_records
  unit: record
name: Broadridge Finops
provider_name: broadridge
provider_slug: broadridge
publisher_name: Broadridge Financial Solutions, Inc.
service_category: Financial Services Technology
slug: broadridge-finops
source_filename: broadridge-finops.yml
source_heading: FinOps Profile
source_url: https://www.broadridge.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Broadridge\nproviderId: broadridge\npublisherName: Broadridge Financial Solutions, Inc.\nserviceCategory: Financial Services Technology\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial Services\n  - Wealth Management\n  - Asset Management\n  - Investor Communications\n  - Regulatory Reporting\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Broadridge: enterprise platform subscriptions across Wealth Operations,\n  Asset Management / Galaxia Fund Data, and Investor Communications. Pricing is contracted per platform\n  subscription and tied to accounts, AUM, and communications volume; APIs ship with\
  \ the underlying platform\n  rather than being separately metered.'\nsources:\n  - https://www.broadridge.com/\n  - https://github.com/wealthapiconnector/Broadridge-Wealth-API-Docs\nnotes: Broadridge is not metered per API call; cost is governed by the platform subscription and per-event\n  communications volume in the master services agreement.\nbillingModel:\n  pricingCategory: Enterprise Subscription + Volume\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Broadridge\n  ServiceCategory: Financial Services Technology\n  ProviderName: Broadridge\n  PublisherName: Broadridge Financial Solutions, Inc.\n  InvoiceIssuerName: Broadridge Financial Solutions, Inc.\n  BillingCurrency: USD\n  PricingCategory: Standard\n  PricingUnit: subscription-month\nmeters:\n  - name: platform_subscription\n    description: Monthly subscription fee for the contracted Broadridge platform module.\n\
  \    unit: month\n    aggregation: sum\n    dimensions:\n      - product_line\n      - tier\n  - name: accounts\n    description: Number of accounts under management on the Wealth Operations / clearing platform.\n    unit: account\n    aggregation: max\n    dimensions:\n      - product_line\n      - region\n  - name: aum\n    description: Assets Under Management used as a billing dimension for asset-management modules.\n    unit: currency\n    aggregation: max\n    dimensions:\n      - product_line\n      - currency\n  - name: investor_communications\n    description: Investor communications (proxy, regulatory, statements) processed.\n    unit: communication\n    aggregation: sum\n    dimensions:\n      - communication_type\n      - channel\n  - name: fund_data_records\n    description: Galaxia fund-data records distributed for regulatory reporting.\n    unit: record\n    aggregation: sum\n    dimensions:\n      - regulation\n      - fund\nprinciples:\n  - name: Visibility\n    description:\
  \ Pull invoice and platform usage reports from Broadridge account management; reconcile\n      account counts, AUM, and communications volume against the contracted ceilings on a monthly cadence.\n  - name: Allocation\n    description: Allocate platform fees by product line, channel, and regulatory regime so wealth, asset-management,\n      and communications spend route to the correct internal cost centers.\n  - name: Optimization\n    description: Consolidate communications channels (digital vs paper), align fund-data feed cadence\n      with downstream requirements, and renegotiate volume tiers at renewal as account / AUM growth materializes.\n  - name: Accountability\n    description: Designate a Broadridge relationship owner per platform module; review monthly invoices,\n      dispute discrepancies, and forecast renewals against business growth targets.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/broadridge/refs/heads/main/finops/broadridge-finops.yml
sources:
- https://www.broadridge.com/
- https://github.com/wealthapiconnector/Broadridge-Wealth-API-Docs
specification: FinOps Framework
tags:
- Financial Services
- Wealth Management
- Asset Management
- Investor Communications
- Regulatory Reporting
- FinOps
- FOCUS
---
