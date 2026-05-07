---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dell-servers-idrac-redfish-openapi.yml
  format: yaml
  label: Dell iDRAC Redfish REST API
  slug: dell-servers-idrac-redfish
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dell-servers/refs/heads/main/openapi/dell-servers-idrac-redfish-openapi.yml
- filename: dell-servers-openmanage-enterprise-openapi.yml
  format: yaml
  label: Dell OpenManage Enterprise API
  slug: dell-servers-openmanage-enterprise
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dell-servers/refs/heads/main/openapi/dell-servers-openmanage-enterprise-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: License + Hardware
description: 'FOCUS-aligned FinOps for Dell server-management APIs: there is no per-call API invoice. Spend is the sum of (a) the underlying PowerEdge hardware, (b) iDRAC license tier upgrades (Enterprise / Datacenter) per server, (c) OpenManage Enterprise plug-in licenses per managed node (Power Manager, SupportAssist, Update Manager, OMIVV, OMEM), and (d) Dell ProSupport / hardware-warranty SKUs. The APIs themselves are bundled with the firmware.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Dell Inc.
  PricingCategory: License + Hardware
  ProviderName: Dell
  PublisherName: Dell Inc.
  ServiceCategory: Hardware Infrastructure
  ServiceName: Dell PowerEdge Management
  ServiceSubcategory: Server Management
layout: finops
meters:
- aggregation: max
  description: Count of PowerEdge servers under management. Drives iDRAC license counts and OpenManage Enterprise plug-in entitlements.
  dimensions:
  - model
  - generation
  - datacenter
  name: managed_servers
  unit: server
- aggregation: max
  description: iDRAC license tier per server (Express, Enterprise, Datacenter).
  dimensions:
  - tier
  - server
  name: idrac_license_tier
  unit: license
- aggregation: max
  description: Active OpenManage Enterprise plug-in licenses (Power Manager, SupportAssist, Update Manager, OMIVV, OMEM) per managed node.
  dimensions:
  - plugin
  - node
  name: ome_plugin_licenses
  unit: license
- aggregation: count
  description: Count of API calls against iDRAC / OME / OMIVV. Useful for capacity planning; not directly billable.
  dimensions:
  - api
  - device
  name: api_requests
  unit: request
- aggregation: sum
  description: Telemetry metrics streamed via the iDRAC Telemetry Streaming API. Useful for sizing downstream observability storage cost.
  dimensions:
  - device
  - metric_class
  name: telemetry_metrics
  unit: metric
name: Dell Servers Finops
provider_name: Dell Servers
provider_slug: dell-servers
publisher_name: Dell Inc.
service_category: Hardware Infrastructure
slug: dell-servers-finops
source_filename: dell-servers-finops.yml
source_heading: FinOps Profile
source_url: https://developer.dell.com/apis/2978
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dell Servers\nproviderId: dell-servers\npublisherName: Dell Inc.\nserviceCategory: Hardware Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Hardware\n  - Infrastructure\n  - Server Management\n  - Redfish\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Dell server-management APIs: there is no per-call API\n  invoice. Spend is the sum of (a) the underlying PowerEdge hardware, (b) iDRAC license tier\n  upgrades (Enterprise / Datacenter) per server, (c) OpenManage Enterprise plug-in licenses per\n  managed node (Power Manager, SupportAssist, Update Manager, OMIVV, OMEM), and (d) Dell\n  ProSupport\
  \ / hardware-warranty SKUs. The APIs themselves are bundled with the firmware.'\nsources:\n  - https://developer.dell.com/apis/2978\n  - https://www.dell.com/support/kbdoc/en-us/000178027/idrac-licenses\n  - https://www.dell.com/en-us/dt/solutions/openmanage/index.htm\nnotes: No metered API billing. FinOps shape attributes spend to per-server hardware + license\n  tiers + managed-node plug-in licenses. Per-license SKU pricing is channel-quoted and not public.\nbillingModel:\n  pricingCategory: License + Hardware\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Dell PowerEdge Management\n  ServiceCategory: Hardware Infrastructure\n  ServiceSubcategory: Server Management\n  ProviderName: Dell\n  PublisherName: Dell Inc.\n  InvoiceIssuerName: Dell Inc.\n  PricingCategory: License + Hardware\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: managed_servers\n    description: Count\
  \ of PowerEdge servers under management. Drives iDRAC license counts and\n      OpenManage Enterprise plug-in entitlements.\n    unit: server\n    aggregation: max\n    dimensions:\n      - model\n      - generation\n      - datacenter\n  - name: idrac_license_tier\n    description: iDRAC license tier per server (Express, Enterprise, Datacenter).\n    unit: license\n    aggregation: max\n    dimensions:\n      - tier\n      - server\n  - name: ome_plugin_licenses\n    description: Active OpenManage Enterprise plug-in licenses (Power Manager, SupportAssist,\n      Update Manager, OMIVV, OMEM) per managed node.\n    unit: license\n    aggregation: max\n    dimensions:\n      - plugin\n      - node\n  - name: api_requests\n    description: Count of API calls against iDRAC / OME / OMIVV. Useful for capacity planning;\n      not directly billable.\n    unit: request\n    aggregation: count\n    dimensions:\n      - api\n      - device\n  - name: telemetry_metrics\n    description: Telemetry\
  \ metrics streamed via the iDRAC Telemetry Streaming API. Useful for\n      sizing downstream observability storage cost.\n    unit: metric\n    aggregation: sum\n    dimensions:\n      - device\n      - metric_class\nprinciples:\n  - name: Visibility\n    description: Use OpenManage Enterprise inventory plus Dell Premier order history to enumerate\n      servers, license tiers, and plug-in entitlements. The OME API exposes managed-node and\n      license information for programmatic reconciliation against the Dell invoice.\n  - name: Allocation\n    description: Tag servers by datacenter, rack, business unit, and workload in OME so iDRAC and\n      plug-in license cost can be attributed to the consuming team or product.\n  - name: Optimization\n    description: Right-size iDRAC license tiers — only servers needing virtual console / telemetry\n      streaming / group manager benefit from Enterprise/Datacenter. Consolidate OME plug-in\n      licenses to the nodes that actually use the feature,\
  \ and use SupportAssist proactively to\n      reduce ProSupport ticket volume.\n  - name: Accountability\n    description: Designate an infrastructure / platform team owner for the Dell estate who reviews\n      iDRAC license sprawl, OME plug-in coverage, and ProSupport renewal annually. Track\n      cost-per-managed-server and cost-per-rack to spot optimization opportunities.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dell-servers/refs/heads/main/finops/dell-servers-finops.yml
sources:
- https://developer.dell.com/apis/2978
- https://www.dell.com/support/kbdoc/en-us/000178027/idrac-licenses
- https://www.dell.com/en-us/dt/solutions/openmanage/index.htm
specification: FinOps Framework
tags:
- Hardware
- Infrastructure
- Server Management
- Redfish
- FinOps
- FOCUS
---
