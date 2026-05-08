---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-purview-catalog-openapi.yml
  format: yaml
  label: Microsoft Purview Catalog API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-catalog-openapi.yml
- filename: microsoft-purview-scanning-openapi.yml
  format: yaml
  label: Microsoft Purview Scanning API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-scanning-openapi.yml
- filename: microsoft-purview-account-openapi.yml
  format: yaml
  label: Microsoft Purview Account API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-account-openapi.yml
- filename: microsoft-purview-data-map-openapi.yml
  format: yaml
  label: Microsoft Purview Data Map API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-data-map-openapi.yml
- filename: microsoft-purview-metadata-policies-openapi.yml
  format: yaml
  label: Microsoft Purview Metadata Policies API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-metadata-policies-openapi.yml
- filename: microsoft-purview-workflow-openapi.yml
  format: yaml
  label: Microsoft Purview Workflow API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-workflow-openapi.yml
- filename: microsoft-purview-unified-catalog-openapi.yml
  format: yaml
  label: Microsoft Purview Unified Catalog API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-unified-catalog-openapi.yml
- filename: microsoft-purview-data-quality-openapi.yml
  format: yaml
  label: Microsoft Purview Data Quality API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-data-quality-openapi.yml
- filename: microsoft-purview-ediscovery-openapi.yml
  format: yaml
  label: Microsoft Purview eDiscovery API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-ediscovery-openapi.yml
- filename: microsoft-purview-information-protection-openapi.yml
  format: yaml
  label: Microsoft Purview Information Protection API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-information-protection-openapi.yml
- filename: microsoft-purview-data-security-governance-openapi.yml
  format: yaml
  label: Microsoft Purview Data Security and Governance API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-data-security-governance-openapi.yml
- filename: microsoft-purview-records-management-openapi.yml
  format: yaml
  label: Microsoft Purview Records Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-records-management-openapi.yml
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
description: FinOps framework definition for the Microsoft Purview API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Purview
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Purview
  PublisherName: Microsoft Purview
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Purview
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
name: Microsoft Purview Finops
provider_name: Microsoft Purview
provider_slug: microsoft-purview
publisher_name: Microsoft Purview
service_category: API
slug: microsoft-purview-finops
source_filename: microsoft-purview-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Purview\nproviderId: microsoft-purview\npublisherName: Microsoft Purview\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Compliance\n  - Data Catalog\n  - Data Classification\n  - Data Governance\n  - Data Loss Prevention\n  - Information Protection\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Purview API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n     \
  \ real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing\
  \ and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Purview\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Purview\n  PublisherName: Microsoft Purview\n  InvoiceIssuerName: Microsoft Purview\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Purview Catalog API\n    baseURL: https://{account-name}.purview.azure.com\n    tags:\n      - Classifications\n      - Data Catalog\n      - Data Discovery\n      - Glossary\n      - Metadata\n    serviceName: Microsoft Purview Catalog API\n    serviceCategory: API\n  - name: Microsoft Purview Scanning API\n    baseURL: https://{account-name}.purview.azure.com\n    tags:\n      - Automated Discovery\n      - Classification Rules\n      - Data Scanning\n      - Data Sources\n      - Scan Triggers\n    serviceName: Microsoft Purview Scanning API\n    serviceCategory: API\n  -\
  \ name: Microsoft Purview Account API\n    baseURL: https://management.azure.com\n    tags:\n      - Account Management\n      - Administration\n      - Configuration\n      - Resource Manager\n    serviceName: Microsoft Purview Account API\n    serviceCategory: API\n  - name: Microsoft Purview Data Map API\n    baseURL: https://{account-name}.purview.azure.com\n    tags:\n      - Data Discovery\n      - Data Map\n      - Entity Management\n      - Lineage\n      - Relationships\n    serviceName: Microsoft Purview Data Map API\n    serviceCategory: API\n  - name: Microsoft Purview Metadata Policies API\n    baseURL: https://{account-name}.purview.azure.com\n    tags:\n      - Access Policies\n      - Collections\n      - Data Governance\n      - Metadata\n      - Role Assignments\n    serviceName: Microsoft Purview Metadata Policies API\n    serviceCategory: API\n  - name: Microsoft Purview Workflow API\n    baseURL: https://{account-name}.purview.azure.com\n    tags:\n      - Approvals\n\
  \      - Automation\n      - Governance Tasks\n      - Workflows\n    serviceName: Microsoft Purview Workflow API\n    serviceCategory: API\n  - name: Microsoft Purview Unified Catalog API\n    baseURL: https://{account-name}.purview.azure.com\n    tags:\n      - Business Domains\n      - Data Governance\n      - Data Products\n      - Glossary Terms\n      - Unified Catalog\n    serviceName: Microsoft Purview Unified Catalog API\n    serviceCategory: API\n  - name: Microsoft Purview Data Quality API\n    baseURL: https://{account-name}.purview.azure.com\n    tags:\n      - Data Assessment\n      - Data Profiling\n      - Data Quality\n      - Quality Rules\n    serviceName: Microsoft Purview Data Quality API\n    serviceCategory: API\n  - name: Microsoft Purview eDiscovery API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Compliance\n      - eDiscovery\n      - Investigations\n      - Legal Hold\n      - Litigation\n    serviceName: Microsoft Purview eDiscovery API\n \
  \   serviceCategory: API\n  - name: Microsoft Purview Information Protection API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Data Classification\n      - Encryption\n      - Information Protection\n      - Rights Management\n      - Sensitivity Labels\n    serviceName: Microsoft Purview Information Protection API\n    serviceCategory: API\n  - name: Microsoft Purview Data Security and Governance API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - AI Security\n      - Compliance\n      - Data Loss Prevention\n      - Data Security\n      - Policy Enforcement\n    serviceName: Microsoft Purview Data Security and Governance API\n    serviceCategory: API\n  - name: Microsoft Purview Records Management API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Compliance\n      - Data Lifecycle\n      - Records Management\n      - Retention Labels\n    serviceName: Microsoft Purview Records Management API\n    serviceCategory: API\nunitEconomics:\n  -\
  \ name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/finops/microsoft-purview-finops.yml
sources: []
specification: FinOps Framework
tags:
- Compliance
- Data Catalog
- Data Classification
- Data Governance
- Data Loss Prevention
- Information Protection
- FinOps
- Cost Management
- FOCUS
---
