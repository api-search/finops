---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: $metadata
  format: yaml
  label: Dynamics 365 Sales API
  slug: ''
  spec_type: OpenAPI
  url: https://[org].api.crm.dynamics.com/api/data/v9.2/$metadata
- filename: $metadata
  format: yaml
  label: Dynamics 365 Customer Service API
  slug: ''
  spec_type: OpenAPI
  url: https://[org].api.crm.dynamics.com/api/data/v9.2/$metadata
- filename: openapi
  format: yaml
  label: Dynamics 365 Business Central API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.microsoft.com/dynamics365/business-central/dev-itpro/api-reference/v2.0/openapi
- filename: microsoft-dynamics-365-dataverse-web-api-openapi.yml
  format: yaml
  label: Microsoft Dataverse Web API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-dynamics-365/refs/heads/main/openapi/microsoft-dynamics-365-dataverse-web-api-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly (annual commitment for most apps)
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription (per Seat) + Tenant + Usage (storage/API)
description: FOCUS-aligned FinOps for Microsoft Dynamics 365 — primarily per-user-per-month seat pricing across Sales, Customer Service, Field Service, Project Operations, Finance, Supply Chain, Commerce, HR, plus tenant-priced Customer Insights and metered Dataverse capacity. Largest savings come from the qualifying-offer attach pricing (subsequent apps per user at $20–$30 vs full price), right-sizing Customer Insights profile capacity, and using Team Members for read-mostly users.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Subscription
  PricingUnit: user-month
  ProviderName: Microsoft Corporation
  PublisherName: Microsoft Corporation
  ServiceCategory: Business Applications
  ServiceName: Microsoft Dynamics 365
layout: finops
meters:
- aggregation: max
  description: Per-app user seats — Sales, Customer Service, Field Service, Finance, SCM, Commerce, HR, Project Operations.
  dimensions:
  - app
  - sku
  - is_attach
  - department
  name: app_seats
  unit: user-month
- aggregation: max
  description: Business Central Essentials / Premium / Team Members.
  dimensions:
  - sku
  name: business_central_seats
  unit: user-month
- aggregation: max
  description: Customer Insights Data + Journeys tenant subscriptions.
  dimensions:
  - product
  - profile_band
  name: customer_insights_tenants
  unit: tenant-month
- aggregation: max
  description: Dataverse database capacity (GB-month).
  dimensions:
  - environment
  - tenant
  name: dataverse_db_capacity
  unit: GB-month
- aggregation: max
  description: Dataverse file / blob capacity.
  dimensions:
  - environment
  name: dataverse_file_capacity
  unit: GB-month
- aggregation: max
  description: Dataverse audit log capacity.
  dimensions:
  - environment
  name: dataverse_log_capacity
  unit: GB-month
- aggregation: sum
  description: Daily Dataverse API requests beyond licensed allocation, billed via Power Platform request capacity packs.
  dimensions:
  - environment
  - service_principal
  name: api_request_entitlement_consumed
  unit: 1000-requests
- aggregation: sum
  description: Inbound voice-channel minutes for Dynamics 365 Contact Center.
  dimensions:
  - channel
  - country
  name: contact_center_ivr_minutes
  unit: minute
name: Microsoft Dynamics 365 Finops
provider_name: Microsoft Dynamics 365
provider_slug: microsoft-dynamics-365
publisher_name: Microsoft Corporation
service_category: Business Applications / CRM-ERP
slug: microsoft-dynamics-365-finops
source_filename: microsoft-dynamics-365-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/dynamics-365/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Dynamics 365\nproviderId: microsoft-dynamics-365\npublisherName: Microsoft Corporation\nserviceCategory: Business Applications / CRM-ERP\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Business Applications\n  - Cloud\n  - CRM\n  - Enterprise\n  - ERP\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Microsoft Dynamics 365 — primarily per-user-per-month\n  seat pricing across Sales, Customer Service, Field Service, Project Operations, Finance,\n  Supply Chain, Commerce, HR, plus tenant-priced Customer Insights and metered Dataverse\n  capacity. Largest savings come from the qualifying-offer\
  \ attach pricing (subsequent apps\n  per user at $20–$30 vs full price), right-sizing Customer Insights profile capacity, and\n  using Team Members for read-mostly users.\nsources:\n  - https://www.microsoft.com/dynamics-365/pricing\n  - https://learn.microsoft.com/en-us/dynamics365/get-started/licensing-overview\n  - https://learn.microsoft.com/en-us/power-platform/admin/capacity-storage\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription (per Seat) + Tenant + Usage (storage/API)\n  billingFrequency: Monthly (annual commitment for most apps)\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Dynamics 365\n  ServiceCategory: Business Applications\n  ProviderName: Microsoft Corporation\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory:\
  \ Subscription\n  PricingUnit: user-month\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: app_seats\n    description: Per-app user seats — Sales, Customer Service, Field Service, Finance, SCM,\n      Commerce, HR, Project Operations.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - app\n      - sku\n      - is_attach\n      - department\n  - name: business_central_seats\n    description: Business Central Essentials / Premium / Team Members.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - sku\n  - name: customer_insights_tenants\n    description: Customer Insights Data + Journeys tenant subscriptions.\n    unit: tenant-month\n    aggregation: max\n    dimensions:\n      - product\n      - profile_band\n  - name: dataverse_db_capacity\n    description: Dataverse database capacity (GB-month).\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - environment\n      - tenant\n  - name: dataverse_file_capacity\n  \
  \  description: Dataverse file / blob capacity.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - environment\n  - name: dataverse_log_capacity\n    description: Dataverse audit log capacity.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - environment\n  - name: api_request_entitlement_consumed\n    description: Daily Dataverse API requests beyond licensed allocation, billed via Power\n      Platform request capacity packs.\n    unit: 1000-requests\n    aggregation: sum\n    dimensions:\n      - environment\n      - service_principal\n  - name: contact_center_ivr_minutes\n    description: Inbound voice-channel minutes for Dynamics 365 Contact Center.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - channel\n      - country\nprinciples:\n  - name: Visibility\n    description: Microsoft 365 admin center > Billing surfaces seat allocations and the\n      qualifying-offer attach status. Power Platform admin center > Resources > Capacity\
  \ shows\n      Dataverse storage and API entitlement consumption per environment. Dynamics 365 admin\n      center surfaces production / sandbox split. FOCUS-aligned commerce exports itemize each\n      Dynamics SKU.\n  - name: Allocation\n    description: Use Entra ID dynamic groups by department / cost-center to assign the right\n      SKU per role. Multi-environment deployments split seats by business unit. Tag Dataverse\n      environments with cost-center and feed the tag into Power Platform admin center reports.\n  - name: Optimization\n    description: Use qualifying-offer attach for users needing multiple apps (e.g., Sales\n      Enterprise primary + Customer Service attach at $20). Replace full Sales/CS users with\n      Team Members ($8) where read-only access suffices. Buy Customer Insights at the actual\n      profile band; right-size profile capacity quarterly. Prefer Business Central over full\n      Finance/SCM for SMB. Disable trial environments developers spin up. Archive\
  \ old\n      Dataverse audit logs to reduce log capacity. For Contact Center, route low-value inbound\n      traffic to digital channels to reduce per-minute IVR cost.\n  - name: Accountability\n    description: License administrator approves new seat purchases; FinOps validates\n      attach-eligibility before each purchase. Quarterly audit of last-sign-in date triggers\n      seat reclamation. Set Cost Management budget on the M365/Dynamics commerce subscription\n      with alerts at 80/100%. Monthly Dataverse capacity review with a target of <80%\n      tenant-cap utilization.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.microsoft.com/dynamics-365\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-dynamics-365/refs/heads/main/finops/microsoft-dynamics-365-finops.yml
sources:
- https://www.microsoft.com/dynamics-365/pricing
- https://learn.microsoft.com/en-us/dynamics365/get-started/licensing-overview
- https://learn.microsoft.com/en-us/power-platform/admin/capacity-storage
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Business Applications
- Cloud
- CRM
- Enterprise
- ERP
- Microsoft
- FinOps
- FOCUS
---
