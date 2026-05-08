---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: infoblox-wapi-openapi.yml
  format: yaml
  label: Infoblox WAPI (Web API)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/infoblox/refs/heads/main/openapi/infoblox-wapi-openapi.yml
- filename: openapi.yaml
  format: yaml
  label: Infoblox BloxOne API
  slug: ''
  spec_type: OpenAPI
  url: https://csp.infoblox.com/apidoc/
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
description: FinOps framework definition for the Infoblox API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Infoblox
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Infoblox
  PublisherName: Infoblox
  ServiceCategory: Developer Tools / API
  ServiceName: Infoblox
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
name: Infoblox Finops
provider_name: Infoblox
provider_slug: infoblox
publisher_name: Infoblox
service_category: API
slug: infoblox-finops
source_filename: infoblox-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Infoblox\nproviderId: infoblox\npublisherName: Infoblox\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - DDI\n  - DHCP\n  - DNS\n  - IPAM\n  - Network Management\n  - Security\n  - Threat Intelligence\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Infoblox API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Infoblox\n  ServiceCategory: Developer Tools / API\n  ProviderName: Infoblox\n  PublisherName: Infoblox\n  InvoiceIssuerName: Infoblox\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Infoblox WAPI (Web API)\n    baseURL: https://{grid-master}/wapi/v2.12\n    tags:\n      - DDI\n      - DHCP\n      - DNS\n      - IPAM\n      - Network Management\n    serviceName: Infoblox WAPI (Web API)\n    serviceCategory: API\n  - name: Infoblox BloxOne API\n    baseURL: https://csp.infoblox.com/api\n    tags:\n      - Cloud\n      - DHCP\n      - DNS\n      - IPAM\n      - Security\n      - Threat Defense\n    serviceName: Infoblox BloxOne API\n    serviceCategory: API\n  - name: Infoblox BloxOne DNS Configuration API\n    baseURL: https://csp.infoblox.com/api/ddi/v1\n    tags:\n      - Cloud\n      - Configuration\n      - DNS\n    serviceName: Infoblox BloxOne DNS\
  \ Configuration API\n    serviceCategory: API\n  - name: Infoblox BloxOne DNS Data API\n    baseURL: https://csp.infoblox.com/api/ddi/v1\n    tags:\n      - Cloud\n      - DNS\n      - Records\n    serviceName: Infoblox BloxOne DNS Data API\n    serviceCategory: API\n  - name: Infoblox BloxOne IPAM/DHCP API\n    baseURL: https://csp.infoblox.com/api/ddi/v1\n    tags:\n      - Cloud\n      - DHCP\n      - IPAM\n      - Network Management\n    serviceName: Infoblox BloxOne IPAM/DHCP API\n    serviceCategory: API\n  - name: Infoblox BloxOne DDI Keys API\n    baseURL: https://csp.infoblox.com/api/ddi/v1\n    tags:\n      - Authentication\n      - DNS Security\n      - Keys\n    serviceName: Infoblox BloxOne DDI Keys API\n    serviceCategory: API\n  - name: Infoblox BloxOne Anycast Configuration API\n    baseURL: https://csp.infoblox.com/api/anycast/v1\n    tags:\n      - Anycast\n      - High Availability\n      - Network Management\n    serviceName: Infoblox BloxOne Anycast Configuration\
  \ API\n    serviceCategory: API\n  - name: Infoblox BloxOne Infrastructure Management API\n    baseURL: https://csp.infoblox.com/api/infra/v1\n    tags:\n      - Cloud\n      - Infrastructure\n      - Management\n    serviceName: Infoblox BloxOne Infrastructure Management API\n    serviceCategory: API\n  - name: Infoblox BloxOne Host Activation API\n    baseURL: https://csp.infoblox.com/api/host_app/v1\n    tags:\n      - Host Activation\n      - Infrastructure\n      - Provisioning\n    serviceName: Infoblox BloxOne Host Activation API\n    serviceCategory: API\n  - name: Infoblox BloxOne DNS Forwarding Proxy API\n    baseURL: https://csp.infoblox.com/api/atcdfp/v1\n    tags:\n      - DNS\n      - Forwarding Proxy\n      - Security\n    serviceName: Infoblox BloxOne DNS Forwarding Proxy API\n    serviceCategory: API\n  - name: Infoblox BloxOne Firewall API\n    baseURL: https://csp.infoblox.com/api/atcfw/v1\n    tags:\n      - Firewall\n      - Security\n      - Threat Defense\n    serviceName:\
  \ Infoblox BloxOne Firewall API\n    serviceCategory: API\n  - name: Infoblox BloxOne Redirect API\n    baseURL: https://csp.infoblox.com/api/atcfw/v1\n    tags:\n      - Redirect\n      - Security\n      - Threat Defense\n    serviceName: Infoblox BloxOne Redirect API\n    serviceCategory: API\n  - name: Infoblox BloxOne Upgrade Policy API\n    baseURL: https://csp.infoblox.com/api/upgrade_policy/v1\n    tags:\n      - Infrastructure\n      - Policy\n      - Upgrade\n    serviceName: Infoblox BloxOne Upgrade Policy API\n    serviceCategory: API\n  - name: Infoblox Threat Defense API\n    baseURL: https://csp.infoblox.com/tide/api\n    tags:\n      - DNS Security\n      - Firewall\n      - Security\n      - Threat Intelligence\n    serviceName: Infoblox Threat Defense API\n    serviceCategory: API\n  - name: Infoblox TIDE API\n    baseURL: https://csp.infoblox.com/tide/api\n    tags:\n      - Indicators\n      - Security\n      - Threat Intelligence\n      - TIDE\n    serviceName: Infoblox\
  \ TIDE API\n    serviceCategory: API\n  - name: Infoblox Dossier API\n    baseURL: https://csp.infoblox.com/tide/api\n    tags:\n      - Dossier\n      - Research\n      - Security\n      - Threat Intelligence\n    serviceName: Infoblox Dossier API\n    serviceCategory: API\n  - name: Infoblox NetMRI API\n    baseURL: https://{netmri-server}/api\n    tags:\n      - Compliance\n      - Configuration Management\n      - Network Automation\n    serviceName: Infoblox NetMRI API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/infoblox/refs/heads/main/finops/infoblox-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- DDI
- DHCP
- DNS
- IPAM
- Network Management
- Security
- Threat Intelligence
- FinOps
- Cost Management
- FOCUS
---
