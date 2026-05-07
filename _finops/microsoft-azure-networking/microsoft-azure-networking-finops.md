---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement currency varies by region)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Azure Networking — pay-as-you-go per resource family (Virtual Network, Load Balancer, VPN Gateway, ExpressRoute, Front Door, Firewall, DNS) plus metered outbound data transfer. Reserved Instances, Savings Plans, and Azure consumption commitments (MACC) are the primary cost-optimization levers; Cost Management + Billing, Azure Advisor, and the FOCUS-conformant Cost Management exports provide visibility.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Usage-Based
  PricingUnit: varies (hour, GB, request, zone-month)
  ProviderName: Microsoft Azure
  PublisherName: Microsoft Corporation
  RegionId: varies (eastus, westeurope, etc.)
  ServiceCategory: Networking
  ServiceName: Azure Networking
layout: finops
meters:
- aggregation: sum
  description: Hourly running cost of a deployed gateway resource (VPN Gateway, Application Gateway, ExpressRoute Gateway, NAT Gateway, Bastion).
  dimensions:
  - resource_type
  - sku
  - region
  name: gateway_hours
  unit: hour
- aggregation: sum
  description: Inbound + outbound data passing through a managed networking resource (Load Balancer, App Gateway, Firewall, NAT Gateway).
  dimensions:
  - resource_type
  - region
  name: data_processed
  unit: GB
- aggregation: sum
  description: Outbound data transfer from Azure to the public internet, charged in tiered bands by source region zone.
  dimensions:
  - source_region
  - destination_zone
  - tier_band
  name: data_egress_internet
  unit: GB
- aggregation: sum
  description: VNet peering ingress + egress, in-region or cross-region.
  dimensions:
  - peering_type
  - region_pair
  name: vnet_peering
  unit: GB
- aggregation: sum
  description: Resolution requests against Azure DNS hosted zones.
  dimensions:
  - zone
  - record_type
  name: dns_queries
  unit: query
- aggregation: max
  description: Active DNS hosted zones billed per month.
  dimensions:
  - zone_type
  name: dns_zones
  unit: zone-month
- aggregation: sum
  description: Active load-balancing / WAF / firewall rules contributing to capacity charges.
  dimensions:
  - resource_type
  - rule_type
  name: rule_count
  unit: rule-hour
name: Microsoft Azure Networking Finops
provider_name: Azure Networking
provider_slug: microsoft-azure-networking
publisher_name: Microsoft Corporation
service_category: Cloud Networking
slug: microsoft-azure-networking-finops
source_filename: microsoft-azure-networking-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/virtual-network/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Networking\nproviderId: microsoft-azure-networking\npublisherName: Microsoft Corporation\nserviceCategory: Cloud Networking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Azure\n  - Cloud\n  - Infrastructure\n  - Microsoft\n  - Networking\n  - FinOps\n  - FOCUS\n  - Cost Management\ndescription: FOCUS-aligned FinOps for Azure Networking — pay-as-you-go per resource family\n  (Virtual Network, Load Balancer, VPN Gateway, ExpressRoute, Front Door, Firewall, DNS) plus\n  metered outbound data transfer. Reserved Instances, Savings Plans, and Azure consumption\n  commitments (MACC) are the primary cost-optimization\
  \ levers; Cost Management + Billing,\n  Azure Advisor, and the FOCUS-conformant Cost Management exports provide visibility.\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/virtual-network/\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/costs/quick-create-budget\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement currency varies by region)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Networking\n  ServiceCategory: Networking\n  ProviderName: Microsoft Azure\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Usage-Based\n  PricingUnit: varies (hour, GB, request, zone-month)\n\
  \  BillingCurrency: USD\n  ChargeCategory: Usage\n  RegionId: varies (eastus, westeurope, etc.)\nmeters:\n  - name: gateway_hours\n    description: Hourly running cost of a deployed gateway resource (VPN Gateway, Application\n      Gateway, ExpressRoute Gateway, NAT Gateway, Bastion).\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - sku\n      - region\n  - name: data_processed\n    description: Inbound + outbound data passing through a managed networking resource (Load\n      Balancer, App Gateway, Firewall, NAT Gateway).\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - region\n  - name: data_egress_internet\n    description: Outbound data transfer from Azure to the public internet, charged in tiered\n      bands by source region zone.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source_region\n      - destination_zone\n      - tier_band\n  - name: vnet_peering\n    description: VNet peering ingress\
  \ + egress, in-region or cross-region.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - peering_type\n      - region_pair\n  - name: dns_queries\n    description: Resolution requests against Azure DNS hosted zones.\n    unit: query\n    aggregation: sum\n    dimensions:\n      - zone\n      - record_type\n  - name: dns_zones\n    description: Active DNS hosted zones billed per month.\n    unit: zone-month\n    aggregation: max\n    dimensions:\n      - zone_type\n  - name: rule_count\n    description: Active load-balancing / WAF / firewall rules contributing to capacity charges.\n    unit: rule-hour\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - rule_type\nprinciples:\n  - name: Visibility\n    description: Use Microsoft Cost Management + Billing, Azure Monitor, and the FOCUS-aligned\n      Cost Management Exports v2 to ingest line-level cost data into your cost analytics platform.\n      Network Watcher, NSG Flow Logs, and VNet flow logs reveal traffic\
  \ patterns driving egress\n      and peering charges.\n  - name: Allocation\n    description: Tag every networking resource with cost-center, environment, application,\n      and owner. Use Azure Policy to enforce required tags. Management Groups + Subscriptions\n      provide hierarchical chargeback boundaries; FOCUS columns SubAccountId / ResourceTags\n      carry the tags through to billing exports.\n  - name: Optimization\n    description: Right-size gateway SKUs (VpnGw1 vs VpnGw5), purchase 1- or 3-year Reserved\n      Capacity for ExpressRoute and Application Gateway, use Azure Front Door / Private Link\n      to avoid public-internet egress, deploy NAT Gateway instead of Public IPs to minimize\n      SNAT cost, and consolidate Standard Load Balancer rules. Azure Advisor surfaces idle\n      gateways and underutilized firewalls.\n  - name: Accountability\n    description: Set Cost Management budgets with action-group alerts at 50/80/100% thresholds\n      per subscription/resource\
  \ group. Network architects own egress topology decisions; tag\n      the workload owner so egress overage routes to the right team. Review monthly cost\n      against unit economics (egress per active user, gateway-hour per region served).\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://azure.microsoft.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-networking/refs/heads/main/finops/microsoft-azure-networking-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/virtual-network/
- https://learn.microsoft.com/en-us/azure/cost-management-billing/
- https://learn.microsoft.com/en-us/azure/cost-management-billing/costs/quick-create-budget
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Azure
- Cloud
- Infrastructure
- Microsoft
- Networking
- FinOps
- FOCUS
- Cost Management
---
