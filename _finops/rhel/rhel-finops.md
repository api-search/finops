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
  label: Red Hat Subscription Management API
  slug: subscription-management-api
  spec_type: OpenAPI
  url: https://api.access.redhat.com/management/v1/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights API
  slug: insights-api
  spec_type: OpenAPI
  url: https://cloud.redhat.com/api/insights/v1/openapi.json
- filename: rhel-security-data-openapi.yml
  format: yaml
  label: Red Hat Security Data API
  slug: security-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rhel/refs/heads/main/openapi/rhel-security-data-openapi.yml
- filename: openapi.json
  format: json
  label: Red Hat Insights Compliance API
  slug: compliance-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/compliance/v2/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights Vulnerability API
  slug: vulnerability-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/vulnerability/v1/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights Patch API
  slug: patch-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/patch/v3/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights Host Inventory API
  slug: inventory-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/inventory/v1/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights Remediations API
  slug: remediations-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/remediations/v1/openapi.json
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
description: FinOps framework definition for the Red Hat Enterprise Linux API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Red Hat Enterprise Linux
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Red Hat Enterprise Linux
  PublisherName: Red Hat Enterprise Linux
  ServiceCategory: Developer Tools / API
  ServiceName: Red Hat Enterprise Linux
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
name: Rhel Finops
provider_name: Red Hat Enterprise Linux
provider_slug: rhel
publisher_name: Red Hat Enterprise Linux
service_category: API
slug: rhel-finops
source_filename: rhel-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat Enterprise Linux\nproviderId: rhel\npublisherName: Red Hat Enterprise Linux\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Compliance\n  - Enterprise\n  - Linux\n  - Operating System\n  - Red Hat\n  - RHEL\n  - Security\n  - Subscription Management\n  - Vulnerability Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Red Hat Enterprise Linux API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Red Hat Enterprise Linux\n  ServiceCategory: Developer Tools / API\n  ProviderName: Red Hat Enterprise Linux\n  PublisherName: Red Hat Enterprise Linux\n  InvoiceIssuerName: Red Hat Enterprise Linux\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Red Hat Subscription Management API\n    baseURL: https://api.access.redhat.com/management/v1\n    tags:\n      - Entitlements\n      - Systems Management\n      - Subscriptions\n    serviceName: Red Hat Subscription Management API\n    serviceCategory: API\n  - name: Red Hat Insights API\n    baseURL: https://console.redhat.com/api/insights/v1\n    tags:\n      - Analytics\n      - Monitoring\n      - Remediation\n    serviceName: Red Hat Insights API\n    serviceCategory: API\n  - name: Red Hat Security Data API\n\
  \    baseURL: https://access.redhat.com/hydra/rest/securitydata\n    tags:\n      - Advisories\n      - CVE\n      - Errata\n      - Security\n      - Vulnerability Management\n    serviceName: Red Hat Security Data API\n    serviceCategory: API\n  - name: Red Hat Insights Compliance API\n    baseURL: https://console.redhat.com/api/compliance/v2\n    tags:\n      - Compliance\n      - SCAP\n      - Security\n    serviceName: Red Hat Insights Compliance API\n    serviceCategory: API\n  - name: Red Hat Insights Vulnerability API\n    baseURL: https://console.redhat.com/api/vulnerability/v1\n    tags:\n      - CVE\n      - Remediation\n      - Security\n      - Vulnerability Management\n    serviceName: Red Hat Insights Vulnerability API\n    serviceCategory: API\n  - name: Red Hat Insights Patch API\n    baseURL: https://console.redhat.com/api/patch/v3\n    tags:\n      - Advisories\n      - Patch Management\n      - Updates\n    serviceName: Red Hat Insights Patch API\n    serviceCategory:\
  \ API\n  - name: Red Hat Insights Host Inventory API\n    baseURL: https://console.redhat.com/api/inventory/v1\n    tags:\n      - Hosts\n      - Inventory\n      - Systems Management\n    serviceName: Red Hat Insights Host Inventory API\n    serviceCategory: API\n  - name: Red Hat Insights Remediations API\n    baseURL: https://console.redhat.com/api/remediations/v1\n    tags:\n      - Ansible\n      - Automation\n      - Remediation\n    serviceName: Red Hat Insights Remediations API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rhel/refs/heads/main/finops/rhel-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Compliance
- Enterprise
- Linux
- Operating System
- Red Hat
- RHEL
- Security
- Subscription Management
- Vulnerability Management
- FinOps
- Cost Management
- FOCUS
---
