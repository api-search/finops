---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-dynamics-business-central-openapi.yml
  format: yaml
  label: Microsoft Dynamics 365 Business Central API
  slug: business-central-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-dynamics/refs/heads/main/openapi/microsoft-dynamics-business-central-openapi.yml
- filename: microsoft-dynamics-dataverse-openapi.yml
  format: yaml
  label: Microsoft Dynamics 365 Dataverse Web API
  slug: dataverse-web-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-dynamics/refs/heads/main/openapi/microsoft-dynamics-dataverse-openapi.yml
- filename: microsoft-dynamics-finance-operations-openapi.yml
  format: yaml
  label: Microsoft Dynamics 365 Finance & Operations Data API
  slug: finance-operations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-dynamics/refs/heads/main/openapi/microsoft-dynamics-finance-operations-openapi.yml
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
  pricingCategory: Subscription (per Seat) + Tenant
description: FOCUS-aligned FinOps for Microsoft Dynamics — primarily per-user-per-month seat pricing across Sales, Customer Service, Finance, Supply Chain, Field Service, Business Central, and tenant-priced platforms (Customer Insights). Significant savings from the qualifying-offer attach pricing — first app full price, subsequent apps for the same user at the attach rate ($20 / $30 / etc.). Largest waste signals are paying full price on attach-eligible users and over-provisioning Customer Insights profile capacity.
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
  description: Sales Pro / Enterprise / Premium user seats.
  dimensions:
  - sku
  - department
  - cost_center
  - is_attach
  name: sales_seats
  unit: user-month
- aggregation: max
  description: Customer Service Pro / Enterprise user seats.
  dimensions:
  - sku
  - is_attach
  name: customer_service_seats
  unit: user-month
- aggregation: max
  description: Field Service user seats.
  dimensions:
  - is_attach
  name: field_service_seats
  unit: user-month
- aggregation: max
  description: Finance user seats.
  dimensions:
  - is_attach
  name: finance_seats
  unit: user-month
- aggregation: max
  description: Supply Chain Management user seats.
  dimensions:
  - is_attach
  name: supply_chain_seats
  unit: user-month
- aggregation: max
  description: Business Central Essentials / Premium / Team Members.
  dimensions:
  - sku
  name: business_central_seats
  unit: user-month
- aggregation: max
  description: Customer Insights tenants and add-on profile bands.
  dimensions:
  - profile_band
  name: customer_insights_tenants
  unit: tenant-month
- aggregation: max
  description: Dataverse storage capacity (database GB, file GB, log GB) consumed by Dynamics 365 applications.
  dimensions:
  - environment
  - storage_type
  name: dataverse_capacity
  unit: GB-month
- aggregation: sum
  description: Power Platform request entitlement consumed beyond licensed allocation.
  dimensions:
  - environment
  - service_principal
  name: api_request_entitlement
  unit: request
name: Microsoft Dynamics Finops
provider_name: Microsoft Dynamics
provider_slug: microsoft-dynamics
publisher_name: Microsoft Corporation
service_category: Business Applications / CRM-ERP
slug: microsoft-dynamics-finops
source_filename: microsoft-dynamics-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/dynamics-365/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Dynamics\nproviderId: microsoft-dynamics\npublisherName: Microsoft Corporation\nserviceCategory: Business Applications / CRM-ERP\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - CRM\n  - ERP\n  - Microsoft Dynamics\n  - Business Applications\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Microsoft Dynamics — primarily per-user-per-month seat\n  pricing across Sales, Customer Service, Finance, Supply Chain, Field Service, Business\n  Central, and tenant-priced platforms (Customer Insights). Significant savings from the\n  qualifying-offer attach pricing — first app full price, subsequent apps for\
  \ the same user\n  at the attach rate ($20 / $30 / etc.). Largest waste signals are paying full price on\n  attach-eligible users and over-provisioning Customer Insights profile capacity.\nsources:\n  - https://www.microsoft.com/dynamics-365/pricing\n  - https://learn.microsoft.com/en-us/dynamics365/get-started/licensing-overview\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription (per Seat) + Tenant\n  billingFrequency: Monthly (annual commitment for most apps)\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Dynamics 365\n  ServiceCategory: Business Applications\n  ProviderName: Microsoft Corporation\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Subscription\n  PricingUnit: user-month\n  BillingCurrency: USD\n  ChargeCategory:\
  \ Usage\nmeters:\n  - name: sales_seats\n    description: Sales Pro / Enterprise / Premium user seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - sku\n      - department\n      - cost_center\n      - is_attach\n  - name: customer_service_seats\n    description: Customer Service Pro / Enterprise user seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - sku\n      - is_attach\n  - name: field_service_seats\n    description: Field Service user seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - is_attach\n  - name: finance_seats\n    description: Finance user seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - is_attach\n  - name: supply_chain_seats\n    description: Supply Chain Management user seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - is_attach\n  - name: business_central_seats\n    description: Business Central Essentials / Premium / Team Members.\n  \
  \  unit: user-month\n    aggregation: max\n    dimensions:\n      - sku\n  - name: customer_insights_tenants\n    description: Customer Insights tenants and add-on profile bands.\n    unit: tenant-month\n    aggregation: max\n    dimensions:\n      - profile_band\n  - name: dataverse_capacity\n    description: Dataverse storage capacity (database GB, file GB, log GB) consumed by\n      Dynamics 365 applications.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - environment\n      - storage_type\n  - name: api_request_entitlement\n    description: Power Platform request entitlement consumed beyond licensed allocation.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - environment\n      - service_principal\nprinciples:\n  - name: Visibility\n    description: Microsoft 365 admin center > Billing surfaces seat allocations and the\n      qualifying-offer attach status. Power Platform admin center > Resources > Capacity shows\n      Dataverse storage and API\
  \ entitlement consumption. FOCUS-aligned commerce exports\n      itemize each Dynamics SKU.\n  - name: Allocation\n    description: Tag users by department / cost-center via Entra ID groups; group-rule\n      assignment enforces the right SKU per role. Multi-org deployments split seats by\n      environment to drive chargeback.\n  - name: Optimization\n    description: Use qualifying-offer attach for users needing multiple apps (e.g., Sales\n      Enterprise primary + Customer Service attach at $20). Replace full Sales/CS users with\n      Team Members ($8) where read-only access is enough. Buy Customer Insights at the\n      profile band actually used; right-size profile capacity quarterly. Prefer Business\n      Central over full Finance/SCM for SMB deployments. Disable trial environments that\n      auto-create when developers explore; they consume capacity.\n  - name: Accountability\n    description: License administrator approves new seat purchases; FinOps validates\n      attach-eligibility\
  \ before each purchase. Quarterly audit of last-sign-in date triggers\n      seat reclamation. Set Cost Management budget on the M365/Dynamics commerce subscription\n      with alerts at 80/100%.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.microsoft.com/dynamics-365\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-dynamics/refs/heads/main/finops/microsoft-dynamics-finops.yml
sources:
- https://www.microsoft.com/dynamics-365/pricing
- https://learn.microsoft.com/en-us/dynamics365/get-started/licensing-overview
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- CRM
- ERP
- Microsoft Dynamics
- Business Applications
- FinOps
- FOCUS
---
