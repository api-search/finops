---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Regulated Tariff / Enterprise Contract
description: 'FinOps placeholder for CMS Energy: Green Button Connect is free; partner / EDI / demand-response integrations are governed by MPSC tariffs or bilateral agreements rather than a public API price list.'
focus_columns:
  BillingCurrency: USD
  PricingCategory: Regulated Tariff
  ProviderName: CMS Energy
  PublisherName: CMS Energy Corporation
  ServiceCategory: Energy / Utility
  ServiceName: CMS Energy
layout: finops
meters:
- aggregation: sum
  description: Customer-authorized energy data shared via Green Button Connect (no charge).
  dimensions:
  - third_party_application
  name: green_button_data_access
  unit: request
- aggregation: sum
  description: Recurring partner integration / EDI subscription fee per the contract.
  dimensions:
  - contract
  name: partner_contract_subscription
  unit: month
name: Cms Energy Finops
provider_name: CMS Energy
provider_slug: cms-energy
publisher_name: CMS Energy Corporation
service_category: Energy / Utility
slug: cms-energy-finops
source_filename: cms-energy-finops.yml
source_heading: FinOps Profile
source_url: https://www.consumersenergy.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CMS Energy\nproviderId: cms-energy\npublisherName: CMS Energy Corporation\nserviceCategory: Energy / Utility\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Energy\n  - Utility\n  - Green Button\nnotes: CMS Energy is a regulated utility, not a software vendor. Green Button Connect is provided at no\n  cost to customers and authorized third parties. The shape below captures the structural FinOps surface\n  of partner / EDI integrations rather than a verified invoice.\ndescription: 'FinOps placeholder for CMS Energy: Green Button Connect is free; partner / EDI / demand-response\n  integrations are\
  \ governed by MPSC tariffs or bilateral agreements rather than a public API price list.'\nsources:\n  - https://www.consumersenergy.com\n  - https://www.greenbuttondata.org/\nbillingModel:\n  pricingCategory: Regulated Tariff / Enterprise Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: CMS Energy\n  ServiceCategory: Energy / Utility\n  ProviderName: CMS Energy\n  PublisherName: CMS Energy Corporation\n  PricingCategory: Regulated Tariff\n  BillingCurrency: USD\nmeters:\n  - name: green_button_data_access\n    description: Customer-authorized energy data shared via Green Button Connect (no charge).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - third_party_application\n  - name: partner_contract_subscription\n    description: Recurring partner integration / EDI subscription fee per the contract.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\n\
  principles:\n  - name: Visibility\n    description: Reconcile usage against partner contracts via the partner's reporting deliverables; Green\n      Button Connect access is observable through the customer's authorization log.\n  - name: Allocation\n    description: Allocate partner-integration costs to the consuming demand-response or settlement program;\n      Green Button Connect carries no allocable cost.\n  - name: Optimization\n    description: Right-size partner contract scope at each renewal; ensure Green Button Connect implementation\n      is up to date with NAESB ESPI revisions to avoid out-of-band custom integrations.\n  - name: Accountability\n    description: Assign a partner-integration owner accountable for renewal and utilization review; assign\n      a Green Button Connect program owner accountable for NAESB ESPI compliance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cms-energy/refs/heads/main/finops/cms-energy-finops.yml
sources:
- https://www.consumersenergy.com
- https://www.greenbuttondata.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Energy
- Utility
- Green Button
---
