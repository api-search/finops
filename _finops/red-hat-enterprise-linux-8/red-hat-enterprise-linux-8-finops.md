---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: RHEL 8 Subscription Management API
  slug: subscription-management-api
  spec_type: OpenAPI
  url: https://api.access.redhat.com/management/v1/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Insights API
  slug: insights-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/insights/v1/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Image Builder API
  slug: image-builder-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/image-builder/v1/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Patch Management API
  slug: patch-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/patch/v3/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Vulnerability Management API
  slug: vulnerability-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/vulnerability/v1/openapi.json
- filename: openapi.json
  format: json
  label: RHEL 8 Compliance API
  slug: compliance-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/compliance/v2/openapi.json
- filename: red-hat-enterprise-linux-8-security-data-openapi.yml
  format: yaml
  label: RHEL 8 Security Data API
  slug: security-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-enterprise-linux-8/refs/heads/main/openapi/red-hat-enterprise-linux-8-security-data-openapi.yml
- filename: openapi.json
  format: json
  label: RHEL 8 Host Inventory API
  slug: host-inventory-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/inventory/v1/openapi.json
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
description: FinOps framework definition for the Red Hat Enterprise Linux 8 API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Red Hat Enterprise Linux 8
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Red Hat Enterprise Linux 8
  PublisherName: Red Hat Enterprise Linux 8
  ServiceCategory: Developer Tools / API
  ServiceName: Red Hat Enterprise Linux 8
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
name: Red Hat Enterprise Linux 8 Finops
provider_name: Red Hat Enterprise Linux 8
provider_slug: red-hat-enterprise-linux-8
publisher_name: Red Hat Enterprise Linux 8
service_category: API
slug: red-hat-enterprise-linux-8-finops
source_filename: red-hat-enterprise-linux-8-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat Enterprise Linux 8\nproviderId: red-hat-enterprise-linux-8\npublisherName: Red Hat Enterprise Linux 8\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Enterprise\n  - Linux\n  - Operating System\n  - Red Hat\n  - RHEL\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Red Hat Enterprise Linux 8 API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Red Hat Enterprise Linux 8\n  ServiceCategory: Developer Tools / API\n  ProviderName: Red Hat Enterprise Linux 8\n  PublisherName: Red Hat Enterprise Linux 8\n  InvoiceIssuerName: Red Hat Enterprise Linux 8\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: RHEL 8 Subscription Management API\n    baseURL: https://api.access.redhat.com/management/v1\n    tags:\n      - Entitlements\n      - Registration\n      - Subscriptions\n      - System Management\n    serviceName: RHEL 8 Subscription Management API\n    serviceCategory: API\n  - name: RHEL 8 Insights API\n    baseURL: https://console.redhat.com/api/insights/v1\n    tags:\n      - Analytics\n      - Compliance\n      - Monitoring\n      - Predictive Analytics\n      - Security\n      - Vulnerabilities\n    serviceName: RHEL 8 Insights API\n    serviceCategory: API\n  - name:\
  \ RHEL 8 Image Builder API\n    baseURL: https://console.redhat.com/api/image-builder/v1\n    tags:\n      - Cloud\n      - Deployment\n      - Image Builder\n      - Infrastructure\n      - Provisioning\n    serviceName: RHEL 8 Image Builder API\n    serviceCategory: API\n  - name: RHEL 8 Patch Management API\n    baseURL: https://console.redhat.com/api/patch/v3\n    tags:\n      - Errata\n      - Packages\n      - Patch Management\n      - Security\n      - Updates\n    serviceName: RHEL 8 Patch Management API\n    serviceCategory: API\n  - name: RHEL 8 Vulnerability Management API\n    baseURL: https://console.redhat.com/api/vulnerability/v1\n    tags:\n      - CVE\n      - Risk Management\n      - Security\n      - Vulnerabilities\n    serviceName: RHEL 8 Vulnerability Management API\n    serviceCategory: API\n  - name: RHEL 8 Compliance API\n    baseURL: https://console.redhat.com/api/compliance/v2\n    tags:\n      - Compliance\n      - SCAP\n      - Security\n      - STIG\n    serviceName:\
  \ RHEL 8 Compliance API\n    serviceCategory: API\n  - name: RHEL 8 Security Data API\n    baseURL: https://access.redhat.com/labs/securitydataapi\n    tags:\n      - Advisories\n      - CVE\n      - OVAL\n      - Public Data\n      - Security\n    serviceName: RHEL 8 Security Data API\n    serviceCategory: API\n  - name: RHEL 8 Host Inventory API\n    baseURL: https://console.redhat.com/api/inventory/v1\n    tags:\n      - Asset Management\n      - Inventory\n      - System Management\n    serviceName: RHEL 8 Host Inventory API\n    serviceCategory: API\n  - name: RHEL 8 Cockpit Web Console API\n    baseURL: https://localhost:9090/cockpit\n    tags:\n      - Management\n      - System Administration\n      - UI\n      - Web Console\n    serviceName: RHEL 8 Cockpit Web Console API\n    serviceCategory: API\n  - name: RHEL 8 System Roles API\n    baseURL: https://console.redhat.com/ansible/automation-hub/\n    tags:\n      - Ansible\n      - Automation\n      - Configuration Management\n\
  \      - System Roles\n    serviceName: RHEL 8 System Roles API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat-enterprise-linux-8/refs/heads/main/finops/red-hat-enterprise-linux-8-finops.yml
sources: []
specification: FinOps Framework
tags:
- Enterprise
- Linux
- Operating System
- Red Hat
- RHEL
- FinOps
- Cost Management
- FOCUS
---
