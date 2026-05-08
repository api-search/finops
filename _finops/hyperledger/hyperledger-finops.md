---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hyperledger-openapi.yml
  format: yaml
  label: Hyperledger Besu API
  slug: hyperledger-besu-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hyperledger/refs/heads/main/openapi/hyperledger-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A (foundation) / Vendor-defined (managed offerings)
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Open Source (no foundation cost)
description: 'FOCUS-aligned FinOps for Hyperledger: open-source frameworks have no vendor invoice; cost surfaces are infrastructure (cloud / on-prem) for self-hosting plus optional vendor-managed offerings billed by ecosystem partners.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: varies (cloud provider for self-hosted; vendor for managed)
  ProviderName: Hyperledger / LF Decentralized Trust
  PublisherName: The Linux Foundation
  ServiceCategory: Blockchain & Distributed Ledger
  ServiceName: Hyperledger
layout: finops
meters:
- aggregation: sum
  description: Compute-hours for self-hosted Hyperledger nodes (peers, orderers, validators); billed by underlying cloud or on-prem infrastructure rather than the foundation.
  dimensions:
  - framework
  - cloud
  - region
  - node_role
  name: node_compute_hours
  unit: instance-hour
- aggregation: avg
  description: GB-month of ledger / world-state / chaindata storage attached to nodes.
  dimensions:
  - framework
  - tier
  name: ledger_storage
  unit: GB-month
- aggregation: sum
  description: Network egress for peer-to-peer gossip and external API consumers.
  dimensions:
  - framework
  - region
  name: network_egress
  unit: GB
- aggregation: sum
  description: Managed-blockchain billing line items charged by ecosystem vendors (IBM Blockchain, AWS Managed Blockchain, Kaleido, Oracle Blockchain).
  dimensions:
  - vendor
  - sku
  name: vendor_managed_service
  unit: varies
- aggregation: sum
  description: Operational throughput meter; useful for unit economics even though not directly billed.
  dimensions:
  - framework
  - channel
  - chaincode
  name: transactions_submitted
  unit: transaction
name: Hyperledger Finops
provider_name: Hyperledger
provider_slug: hyperledger
publisher_name: The Linux Foundation (LF Decentralized Trust)
service_category: Blockchain & Distributed Ledger
slug: hyperledger-finops
source_filename: hyperledger-finops.yml
source_heading: FinOps Profile
source_url: https://lfdecentralizedtrust.org/projects
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Hyperledger\nproviderId: hyperledger\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Blockchain\n  - Open Source\ndescription: 'FOCUS-aligned FinOps for Hyperledger: open-source frameworks have no vendor invoice;\n  cost surfaces are infrastructure (cloud / on-prem) for self-hosting plus optional vendor-managed\n  offerings billed by ecosystem partners.'\nsources:\n  - https://lfdecentralizedtrust.org/projects\n  - https://www.hyperledger.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Linux Foundation (LF Decentralized Trust)\nserviceCategory: Blockchain & Distributed Ledger\nbillingModel:\n  pricingCategory: Open Source\
  \ (no foundation cost)\n  billingFrequency: N/A (foundation) / Vendor-defined (managed offerings)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Hyperledger\n  ServiceCategory: Blockchain & Distributed Ledger\n  ProviderName: Hyperledger / LF Decentralized Trust\n  PublisherName: The Linux Foundation\n  InvoiceIssuerName: varies (cloud provider for self-hosted; vendor for managed)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: node_compute_hours\n    description: Compute-hours for self-hosted Hyperledger nodes (peers, orderers, validators); billed\n      by underlying cloud or on-prem infrastructure rather than the foundation.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - framework\n      - cloud\n      - region\n      - node_role\n  - name: ledger_storage\n    description: GB-month of ledger / world-state / chaindata storage attached to nodes.\n    unit: GB-month\n    aggregation:\
  \ avg\n    dimensions:\n      - framework\n      - tier\n  - name: network_egress\n    description: Network egress for peer-to-peer gossip and external API consumers.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - framework\n      - region\n  - name: vendor_managed_service\n    description: Managed-blockchain billing line items charged by ecosystem vendors (IBM Blockchain,\n      AWS Managed Blockchain, Kaleido, Oracle Blockchain).\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - vendor\n      - sku\n  - name: transactions_submitted\n    description: Operational throughput meter; useful for unit economics even though not directly\n      billed.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - framework\n      - channel\n      - chaincode\nprinciples:\n  - name: Visibility\n    description: Hyperledger itself produces no invoice. Track cost via the underlying cloud or on-prem\n      infrastructure billing (AWS Cost Explorer, Azure Cost\
  \ Management, GCP Billing, Kubernetes cost\n      tools like OpenCost). For managed offerings, use the vendor's billing portal.\n  - name: Allocation\n    description: Tag node infrastructure by network / consortium / channel so that cost can be allocated\n      back to the participating organization. Use Kubernetes namespaces and labels when running Fabric\n      / Besu under K8s.\n  - name: Optimization\n    description: Right-size peer and orderer nodes; use spot/preemptible nodes for non-critical peers;\n      consolidate networks where governance allows; consider managed offerings only when in-house\n      operational cost exceeds vendor markup.\n  - name: Accountability\n    description: Establish per-consortium and per-channel cost ownership. For managed offerings,\n      review monthly vendor invoices and validate node count, transaction volume, and storage size\n      against expectations.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hyperledger/refs/heads/main/finops/hyperledger-finops.yml
sources:
- https://lfdecentralizedtrust.org/projects
- https://www.hyperledger.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Blockchain
- Open Source
---
