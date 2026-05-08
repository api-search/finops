---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-azure-networking-openapi.yml
  format: yaml
  label: Azure Virtual Networks API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-networking/refs/heads/main/openapi/microsoft-azure-networking-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Azure Networking API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Networking
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Networking
  PublisherName: Azure Networking
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Networking
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Microsoft Azure Networking Finops
provider_name: Azure Networking
provider_slug: microsoft-azure-networking
publisher_name: Azure Networking
service_category: API
slug: microsoft-azure-networking-finops
source_filename: microsoft-azure-networking-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Networking\nproviderId: microsoft-azure-networking\npublisherName: Azure Networking\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Azure\n  - Cloud\n  - Infrastructure\n  - Microsoft\n  - Networking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Networking API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Networking\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Networking\n  PublisherName: Azure Networking\n  InvoiceIssuerName: Azure Networking\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Virtual Networks API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks\n    tags:\n      - Peering\n      - Subnets\n      - Virtual Networks\n      - Vnet\n    serviceName: Azure Virtual Networks API\n    serviceCategory: API\n  - name: Azure Load Balancer API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers\n    tags:\n      - High Availability\n      - Load Balancer\n      - Traffic Distribution\n    serviceName: Azure Load\
  \ Balancer API\n    serviceCategory: API\n  - name: Azure Application Gateway API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/applicationGateways\n    tags:\n      - Application Gateway\n      - Layer 7 Load Balancing\n      - Ssl Termination\n      - Web Application Firewall\n    serviceName: Azure Application Gateway API\n    serviceCategory: API\n  - name: Azure Network Security Groups API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkSecurityGroups\n    tags:\n      - Firewall\n      - Network Security Groups\n      - Nsg\n      - Security\n    serviceName: Azure Network Security Groups API\n    serviceCategory: API\n  - name: Azure VPN Gateway API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways\n\
  \    tags:\n      - Gateway\n      - Hybrid Connectivity\n      - Site-To-Site\n      - Vpn\n    serviceName: Azure VPN Gateway API\n    serviceCategory: API\n  - name: Azure Traffic Manager API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles\n    tags:\n      - Dns\n      - Failover\n      - Global Load Balancing\n      - Traffic Manager\n    serviceName: Azure Traffic Manager API\n    serviceCategory: API\n  - name: Azure ExpressRoute API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/expressRouteCircuits\n    tags:\n      - Dedicated Connection\n      - Expressroute\n      - Hybrid\n      - Private Connectivity\n    serviceName: Azure ExpressRoute API\n    serviceCategory: API\n  - name: Azure Firewall API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/azureFirewalls\n\
  \    tags:\n      - Firewall\n      - Network Security\n      - Security\n      - Threat Protection\n    serviceName: Azure Firewall API\n    serviceCategory: API\n  - name: Azure DNS API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/dnsZones\n    tags:\n      - DNS\n      - Domain Name System\n      - Records\n      - Zones\n    serviceName: Azure DNS API\n    serviceCategory: API\n  - name: Azure Private DNS API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/privateDnsZones\n    tags:\n      - DNS\n      - Name Resolution\n      - Private DNS\n      - Virtual Networks\n    serviceName: Azure Private DNS API\n    serviceCategory: API\n  - name: Azure Front Door API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/frontDoors\n\
  \    tags:\n      - CDN\n      - Front Door\n      - Global Load Balancing\n      - Web Application Firewall\n    serviceName: Azure Front Door API\n    serviceCategory: API\n  - name: Azure DDoS Protection API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/ddosProtectionPlans\n    tags:\n      - DDoS Protection\n      - Network Security\n      - Security\n      - Threat Mitigation\n    serviceName: Azure DDoS Protection API\n    serviceCategory: API\n  - name: Azure Network Watcher API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers\n    tags:\n      - Diagnostics\n      - Flow Logs\n      - Network Monitoring\n      - Packet Capture\n    serviceName: Azure Network Watcher API\n    serviceCategory: API\n  - name: Azure Bastion API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/bastionHosts\n\
  \    tags:\n      - Bastion\n      - RDP\n      - Remote Access\n      - Secure Connectivity\n      - SSH\n    serviceName: Azure Bastion API\n    serviceCategory: API\n  - name: Azure NAT Gateway API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/natGateways\n    tags:\n      - IP Address Management\n      - NAT Gateway\n      - Outbound Connectivity\n      - SNAT\n    serviceName: Azure NAT Gateway API\n    serviceCategory: API\n  - name: Azure Private Link API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/privateLinkServices\n    tags:\n      - Network Isolation\n      - Private Endpoint\n      - Private Link\n      - Security\n    serviceName: Azure Private Link API\n    serviceCategory: API\n  - name: Azure Virtual WAN API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualWans\n\
  \    tags:\n      - Branch Connectivity\n      - Hybrid Networking\n      - SD-WAN\n      - Virtual WAN\n    serviceName: Azure Virtual WAN API\n    serviceCategory: API\n  - name: Azure Web Application Firewall API\n    baseURL: https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies\n    tags:\n      - Application Protection\n      - Security\n      - WAF\n      - Web Application Firewall\n    serviceName: Azure Web Application Firewall API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://azure.microsoft.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-networking/refs/heads/main/finops/microsoft-azure-networking-finops.yml
sources: []
specification: FinOps Framework
tags:
- Azure
- Cloud
- Infrastructure
- Microsoft
- Networking
- FinOps
- Cost Management
- FOCUS
---
