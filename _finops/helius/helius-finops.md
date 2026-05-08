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
  - Usage
  - Purchase
  pricingCategory: Subscription + Usage
description: Helius bills as monthly subscription with included credits. LaserStream data add-ons ($500-$4,500/month) and Dedicated Nodes ($2,900+/month) are line-itemed separately.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Helius
  ProviderName: Helius
  PublisherName: Helius
  ServiceCategory: Web3
  ServiceName: Helius
layout: finops
meters:
- aggregation: sum
  description: Helius credits consumed per request, weighted by method.
  dimensions:
  - api_key
  - method
  name: credits
  unit: credit
- aggregation: sum
  description: LaserStream gRPC bandwidth consumed.
  dimensions:
  - stream
  name: laserstream_bandwidth
  unit: byte
- aggregation: sum
  description: Dedicated node hours.
  dimensions:
  - node
  name: dedicated_nodes
  unit: hour
name: Helius Finops
provider_name: Helius
provider_slug: helius
publisher_name: Helius Labs, Inc.
service_category: Web3
slug: helius-finops
source_filename: helius-finops.yml
source_heading: FinOps Profile
source_url: https://www.helius.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Helius\nproviderId: helius\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Blockchain\n- Solana\n- RPC\n- DAS\n- Streams\n- FinOps\n- FOCUS\ndescription: Helius bills as monthly subscription with included credits. LaserStream\n  data add-ons ($500-$4,500/month) and Dedicated Nodes ($2,900+/month) are line-itemed\n  separately.\nnotes: Usage in dashboard.\nsources:\n- https://www.helius.dev/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Helius Labs, Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n\
  \  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: Helius\n  ServiceCategory: Web3\n  ProviderName: Helius\n  PublisherName: Helius\n  InvoiceIssuerName: Helius\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: credits\n  description: Helius credits consumed per request, weighted by method.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - api_key\n  - method\n- name: laserstream_bandwidth\n  description: LaserStream gRPC bandwidth consumed.\n  unit: byte\n  aggregation: sum\n  dimensions:\n  - stream\n- name: dedicated_nodes\n  description: Dedicated node hours.\n  unit: hour\n  aggregation: sum\n  dimensions:\n  - node\nprinciples:\n- name: Visibility\n  description: Monitor credit consumption in the Helius dashboard.\n- name: Allocation\n  description: API key per service; tag environments.\n- name: Optimization\n  description: Use DAS instead of getProgramAccounts; subscribe instead of poll; size\n    LaserStream filters.\n- name: Accountability\n\
  \  description: API-key owners review monthly credit usage.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/helius/refs/heads/main/finops/helius-finops.yml
sources:
- https://www.helius.dev/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Blockchain
- Solana
- RPC
- DAS
- Streams
- FinOps
- FOCUS
---
