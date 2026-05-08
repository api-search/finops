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
  - Tax
  pricingCategory: Enterprise Contract
description: 'FinOps placeholder for Clearwater Paper: no public API pricing surface, so meters and FOCUS columns reflect the typical shape of an enterprise EDI / partner contract.'
focus_columns:
  BillingCurrency: USD
  PricingCategory: Enterprise Contract
  ProviderName: Clearwater Paper
  PublisherName: Clearwater Paper Corporation
  ServiceCategory: Consumer Goods Manufacturing
  ServiceName: Clearwater Paper
layout: finops
meters:
- aggregation: sum
  description: Recurring partner integration / EDI subscription fee per the enterprise contract.
  dimensions:
  - contract
  name: contract_subscription
  unit: month
name: Clearwater Paper Finops
provider_name: Clearwater Paper
provider_slug: clearwater-paper
publisher_name: Clearwater Paper Corporation
service_category: Consumer Goods Manufacturing
slug: clearwater-paper-finops
source_filename: clearwater-paper-finops.yml
source_heading: FinOps Profile
source_url: https://www.clearwaterpaper.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Clearwater Paper\nproviderId: clearwater-paper\npublisherName: Clearwater Paper Corporation\nserviceCategory: Consumer Goods Manufacturing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Tissue\n  - Paperboard\n  - Consumer\nnotes: Clearwater Paper is a manufacturer, not a software vendor. There is no public API price list; this\n  artifact captures only the structural FinOps shape of a partner-contract or EDI integration.\ndescription: 'FinOps placeholder for Clearwater Paper: no public API pricing surface, so meters and FOCUS\n  columns reflect the typical shape of an enterprise EDI / partner\
  \ contract.'\nsources:\n  - https://www.clearwaterpaper.com\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: Clearwater Paper\n  ServiceCategory: Consumer Goods Manufacturing\n  ProviderName: Clearwater Paper\n  PublisherName: Clearwater Paper Corporation\n  PricingCategory: Enterprise Contract\n  BillingCurrency: USD\nmeters:\n  - name: contract_subscription\n    description: Recurring partner integration / EDI subscription fee per the enterprise contract.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Reconcile usage against the partner contract via the partner's reporting deliverables.\n  - name: Allocation\n    description: Allocate the contract to the consuming retail-supply or distributor-operations team.\n  - name: Optimization\n    description: Right-size the partner\
  \ contract scope at each renewal.\n  - name: Accountability\n    description: Assign a partner-integration owner accountable for renewal and utilization review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/clearwater-paper/refs/heads/main/finops/clearwater-paper-finops.yml
sources:
- https://www.clearwaterpaper.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Tissue
- Paperboard
- Consumer
---
