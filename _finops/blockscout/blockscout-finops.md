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
  - Subscription
  - Usage
  pricingCategory: Subscription with Metered Credit Allowance
description: 'FinOps view of Blockscout. Three cost models: free / self-host (OSS), hosted PRO API on dev.blockscout.com (subscription with credit allowance), and Explorer-as-a-Service (managed hosting). Per-chain public instances are typically free.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Blockscout
  ProviderName: Blockscout
  PublisherName: Blockscout
  ServiceCategory: Crypto Explorer
  ServiceName: Blockscout PRO API
layout: finops
meters:
- aggregation: sum
  description: Monthly PRO subscription per API key.
  dimensions:
  - api_key
  name: pro_subscription
  unit: month
- aggregation: sum
  description: Per-call credit consumption against monthly allowance.
  dimensions:
  - api_key
  - chain
  - endpoint
  name: pro_credits
  unit: credit
- aggregation: sum
  description: Explorer-as-a-Service managed-instance subscription.
  dimensions:
  - chain
  name: eaas_subscription
  unit: month
name: Blockscout Finops
provider_name: Blockscout
provider_slug: blockscout
publisher_name: Blockscout
service_category: Crypto Explorer
slug: blockscout-finops
source_filename: blockscout-finops.yml
source_heading: FinOps Profile
source_url: https://dev.blockscout.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Blockscout\nproviderId: blockscout\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Web3\n  - Explorer\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Blockscout. Three cost models: free / self-host (OSS), hosted PRO API on\n  dev.blockscout.com (subscription with credit allowance), and Explorer-as-a-Service (managed\n  hosting). Per-chain public instances are typically free.\nsources:\n  - https://dev.blockscout.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Blockscout\nserviceCategory: Crypto Explorer\nbillingModel:\n  pricingCategory: Subscription with Metered Credit Allowance\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\nfocusColumns:\n  ServiceName: Blockscout PRO API\n  ServiceCategory: Crypto Explorer\n  ProviderName: Blockscout\n  PublisherName: Blockscout\n  InvoiceIssuerName: Blockscout\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: pro_subscription\n    description: Monthly PRO subscription per API key.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\n  - name: pro_credits\n    description: Per-call credit consumption against monthly allowance.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api_key\n      - chain\n      - endpoint\n  - name: eaas_subscription\n    description: Explorer-as-a-Service managed-instance subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - chain\nprinciples:\n  - name: Visibility\n    description: Track per-endpoint credit consumption and per-chain EaaS costs.\n  -\
  \ name: Allocation\n    description: Allocate PRO subscription per API key; allocate EaaS per chain.\n  - name: Optimization\n    description: Self-host where chain volume justifies; use PRO for breadth across chains.\n  - name: Accountability\n    description: Assign a billing owner per PRO key and per managed instance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/blockscout/refs/heads/main/finops/blockscout-finops.yml
sources:
- https://dev.blockscout.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Explorer
- FinOps
- FOCUS
---
