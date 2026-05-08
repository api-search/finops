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
  - Adjustment
  pricingCategory: Service Contract
description: 'FOCUS-aligned FinOps for Brink''s: bundled commercial contract covering 24SEVEN ACCESS portal, Armored Account, RetailBox, and Brink''s Money paycard services with armored logistics and hardware. Software and API access are not separately metered; spend is dominated by per-pickup and per-location service fees set in the master services agreement.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Brink's Company
  PricingCategory: Other
  PricingUnit: service-contract
  ProviderName: Brink's
  PublisherName: The Brink's Company
  ServiceCategory: Cash Management & Logistics
  ServiceName: Brink's
layout: finops
meters:
- aggregation: sum
  description: Monthly contracted service fee covering portal access, software, and base logistics.
  dimensions:
  - location
  - product_line
  name: service_contract_month
  unit: month
- aggregation: sum
  description: Armored pickup events per location.
  dimensions:
  - location
  - frequency_band
  name: pickups
  unit: event
- aggregation: sum
  description: Cash deposits processed through 24SEVEN ACCESS / Armored Account.
  dimensions:
  - location
  name: deposits_processed
  unit: deposit
- aggregation: sum
  description: Brink's Money paycard loads.
  dimensions:
  - employer
  name: paycard_loads
  unit: load
name: Brinks Finops
provider_name: Brinks
provider_slug: brinks
publisher_name: The Brink's Company
service_category: Cash Management & Logistics
slug: brinks-finops
source_filename: brinks-finops.yml
source_heading: FinOps Profile
source_url: https://www.brinks.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Brinks\nproviderId: brinks\npublisherName: The Brink's Company\nserviceCategory: Cash Management & Logistics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cash Management\n  - Security\n  - ATM Services\n  - Financial Services\n  - Armored Transport\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Brink''s: bundled commercial contract covering 24SEVEN ACCESS\n  portal, Armored Account, RetailBox, and Brink''s Money paycard services with armored logistics and\n  hardware. Software and API access are not separately metered; spend is dominated by per-pickup and\n  per-location service fees set in the master\
  \ services agreement.'\nsources:\n  - https://www.brinks.com/\nnotes: API access is included with contracted cash management services; no public per-API price.\nbillingModel:\n  pricingCategory: Service Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Brink's\n  ServiceCategory: Cash Management & Logistics\n  ProviderName: Brink's\n  PublisherName: The Brink's Company\n  InvoiceIssuerName: The Brink's Company\n  BillingCurrency: USD\n  PricingCategory: Other\n  PricingUnit: service-contract\nmeters:\n  - name: service_contract_month\n    description: Monthly contracted service fee covering portal access, software, and base logistics.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - location\n      - product_line\n  - name: pickups\n    description: Armored pickup events per location.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - location\n\
  \      - frequency_band\n  - name: deposits_processed\n    description: Cash deposits processed through 24SEVEN ACCESS / Armored Account.\n    unit: deposit\n    aggregation: sum\n    dimensions:\n      - location\n  - name: paycard_loads\n    description: Brink's Money paycard loads.\n    unit: load\n    aggregation: sum\n    dimensions:\n      - employer\nprinciples:\n  - name: Visibility\n    description: Use 24SEVEN ACCESS to track deposits, pickups, and change orders by location; reconcile\n      against monthly invoices and the master services agreement.\n  - name: Allocation\n    description: Allocate cash management spend by store / location to product lines, regions, or business\n      units that own the cash flow.\n  - name: Optimization\n    description: Tune pickup frequency to actual deposit volume per location, consolidate stops where\n      geography allows, and renegotiate volume-based discounts at renewal.\n  - name: Accountability\n    description: Designate a treasury\
  \ / store-operations owner for the Brink's relationship; review pickup\n      frequency, dispute discrepancies, and forecast contract renewals against retail growth plans.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/brinks/refs/heads/main/finops/brinks-finops.yml
sources:
- https://www.brinks.com/
specification: FinOps Framework
tags:
- Cash Management
- Security
- ATM Services
- Financial Services
- Armored Transport
- FinOps
- FOCUS
---
