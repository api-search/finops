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
description: 'FinOps placeholder for The Coca-Cola Company: no public API pricing surface, so meters and FOCUS columns reflect the typical shape of a bottler / retailer / distributor B2B contract.'
focus_columns:
  BillingCurrency: USD
  PricingCategory: Enterprise Contract
  ProviderName: The Coca-Cola Company
  PublisherName: The Coca-Cola Company
  ServiceCategory: Consumer Goods Manufacturing
  ServiceName: The Coca-Cola Company
layout: finops
meters:
- aggregation: sum
  description: Recurring partner integration / EDI subscription fee per the enterprise contract.
  dimensions:
  - contract
  name: contract_subscription
  unit: month
- aggregation: sum
  description: EDI documents exchanged with the bottler / retailer / distributor under the contract.
  dimensions:
  - document_type
  - partner
  name: edi_documents
  unit: document
name: Coca Cola Finops
provider_name: The Coca-Cola Company
provider_slug: coca-cola
publisher_name: The Coca-Cola Company
service_category: Consumer Goods Manufacturing
slug: coca-cola-finops
source_filename: coca-cola-finops.yml
source_heading: FinOps Profile
source_url: https://www.coca-colacompany.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: The Coca-Cola Company\nproviderId: coca-cola\npublisherName: The Coca-Cola Company\nserviceCategory: Consumer Goods Manufacturing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Beverages\n  - Consumer Goods\n  - Supply Chain\nnotes: The Coca-Cola Company is a beverage manufacturer, not a software vendor. There is no public API\n  price list; this artifact captures the structural FinOps shape of bilateral B2B / EDI integrations rather\n  than verified invoice line-items.\ndescription: 'FinOps placeholder for The Coca-Cola Company: no public API pricing surface, so meters and\n  FOCUS columns reflect\
  \ the typical shape of a bottler / retailer / distributor B2B contract.'\nsources:\n  - https://www.coca-colacompany.com\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: The Coca-Cola Company\n  ServiceCategory: Consumer Goods Manufacturing\n  ProviderName: The Coca-Cola Company\n  PublisherName: The Coca-Cola Company\n  PricingCategory: Enterprise Contract\n  BillingCurrency: USD\nmeters:\n  - name: contract_subscription\n    description: Recurring partner integration / EDI subscription fee per the enterprise contract.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\n  - name: edi_documents\n    description: EDI documents exchanged with the bottler / retailer / distributor under the contract.\n    unit: document\n    aggregation: sum\n    dimensions:\n      - document_type\n      - partner\nprinciples:\n  - name: Visibility\n\
  \    description: Reconcile EDI / B2B traffic against the partner contract via the partner's reporting deliverables.\n  - name: Allocation\n    description: Allocate partner-integration costs to the consuming bottler-operations, retail-supply,\n      or distributor-operations team.\n  - name: Optimization\n    description: Right-size partner contract scope at each renewal; consolidate EDI document types across\n      partners where possible.\n  - name: Accountability\n    description: Assign a partner-integration owner accountable for renewal and utilization review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coca-cola/refs/heads/main/finops/coca-cola-finops.yml
sources:
- https://www.coca-colacompany.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Beverages
- Consumer Goods
- Supply Chain
---
