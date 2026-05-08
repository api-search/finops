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
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Oracle APEX API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle APEX
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle APEX
  PublisherName: Oracle APEX
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle APEX
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
name: Oracle Apex Finops
provider_name: Oracle APEX
provider_slug: oracle-apex
publisher_name: Oracle APEX
service_category: API
slug: oracle-apex-finops
source_filename: oracle-apex-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle APEX\nproviderId: oracle-apex\npublisherName: Oracle APEX\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - APEX\n  - Cloud\n  - Database\n  - Development Platform\n  - Enterprise\n  - Generative AI\n  - Low-Code\n  - Oracle\n  - ORDS\n  - PL/SQL\n  - REST API\n  - Web Applications\n  - Workflow\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle APEX API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle APEX\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle APEX\n  PublisherName: Oracle APEX\n  InvoiceIssuerName: Oracle APEX\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      -\
  \ consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle APEX REST Data Services API\n    baseURL: https://apex.oracle.com/pls/apex/\n    tags:\n      - Data Services\n      - Database\n      - Low-Code\n      - REST\n    serviceName: Oracle APEX REST Data Services API\n    serviceCategory: API\n  - name: Oracle APEX SQL Workshop API\n    baseURL: https://apex.oracle.com/pls/apex/\n    tags:\n      - Database\n      - Development\n      - SQL\n    serviceName: Oracle APEX SQL Workshop API\n    serviceCategory: API\n  - name: Oracle APEX Application API\n    baseURL: https://apex.oracle.com/pls/apex/\n    tags:\n  \
  \    - Applications\n      - Development\n      - Management\n    serviceName: Oracle APEX Application API\n    serviceCategory: API\n  - name: Oracle REST Data Services (ORDS) API\n    baseURL: https://example.com/ords/_/db-api/stable/\n    tags:\n      - Integration\n      - ORDS\n      - REST\n      - Web Services\n    serviceName: Oracle REST Data Services (ORDS) API\n    serviceCategory: API\n  - name: Oracle APEX Cloud REST API\n    baseURL: https://apex.oracle.com/pls/apex/\n    tags:\n      - Administration\n      - Cloud\n      - Oracle Cloud\n      - Provisioning\n      - REST\n    serviceName: Oracle APEX Cloud REST API\n    serviceCategory: API\n  - name: Oracle APEX Export and Import API\n    baseURL: https://apex.oracle.com/pls/apex/\n    tags:\n      - Applications\n      - Deployment\n      - Export\n      - Import\n      - PL/SQL\n    serviceName: Oracle APEX Export and Import API\n    serviceCategory: API\n  - name: Oracle APEX Approval and Workflow API\n    baseURL:\
  \ https://apex.oracle.com/pls/apex/\n    tags:\n      - Approval\n      - Automation\n      - Human Tasks\n      - PL/SQL\n      - Workflow\n    serviceName: Oracle APEX Approval and Workflow API\n    serviceCategory: API\n  - name: Oracle APEX Utility API\n    baseURL: https://apex.oracle.com/pls/apex/\n    tags:\n      - Authentication\n      - PL/SQL\n      - Session\n      - User Management\n      - Utility\n    serviceName: Oracle APEX Utility API\n    serviceCategory: API\n  - name: Oracle APEX Generative AI API\n    baseURL: https://apex.oracle.com/pls/apex/\n    tags:\n      - AI\n      - Generative AI\n      - Machine Learning\n      - PL/SQL\n      - Vector Search\n    serviceName: Oracle APEX Generative AI API\n    serviceCategory: API\n  - name: Oracle ORDS Database API\n    baseURL: https://example.com/ords/\n    tags:\n      - Database\n      - Management\n      - Monitoring\n      - ORDS\n      - REST\n    serviceName: Oracle ORDS Database API\n    serviceCategory: API\n\
  \  - name: Oracle APEX REST Administration API\n    baseURL: https://apex.oracle.com/pls/apex/\n    tags:\n      - Administration\n      - Automation\n      - Instance Management\n      - REST\n    serviceName: Oracle APEX REST Administration API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-apex/refs/heads/main/finops/oracle-apex-finops.yml
sources: []
specification: FinOps Framework
tags:
- APEX
- Cloud
- Database
- Development Platform
- Enterprise
- Generative AI
- Low-Code
- Oracle
- ORDS
- PL/SQL
- REST API
- Web Applications
- Workflow
- FinOps
- Cost Management
- FOCUS
---
