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
  slug: microsoft-purview-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-catalog-openapi.yml
- filename: microsoft-purview-scanning-openapi.yml
  format: yaml
  label: Microsoft Purview Scanning API
  slug: microsoft-purview-scanning-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-scanning-openapi.yml
- filename: microsoft-purview-account-openapi.yml
  format: yaml
  label: Microsoft Purview Account API
  slug: microsoft-purview-account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-account-openapi.yml
- filename: microsoft-purview-data-map-openapi.yml
  format: yaml
  label: Microsoft Purview Data Map API
  slug: microsoft-purview-data-map-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-data-map-openapi.yml
- filename: microsoft-purview-metadata-policies-openapi.yml
  format: yaml
  label: Microsoft Purview Metadata Policies API
  slug: microsoft-purview-metadata-policies-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-metadata-policies-openapi.yml
- filename: microsoft-purview-workflow-openapi.yml
  format: yaml
  label: Microsoft Purview Workflow API
  slug: microsoft-purview-workflow-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-workflow-openapi.yml
- filename: microsoft-purview-unified-catalog-openapi.yml
  format: yaml
  label: Microsoft Purview Unified Catalog API
  slug: microsoft-purview-unified-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-unified-catalog-openapi.yml
- filename: microsoft-purview-data-quality-openapi.yml
  format: yaml
  label: Microsoft Purview Data Quality API
  slug: microsoft-purview-data-quality-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-data-quality-openapi.yml
- filename: microsoft-purview-ediscovery-openapi.yml
  format: yaml
  label: Microsoft Purview eDiscovery API
  slug: microsoft-purview-ediscovery-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-ediscovery-openapi.yml
- filename: microsoft-purview-information-protection-openapi.yml
  format: yaml
  label: Microsoft Purview Information Protection API
  slug: microsoft-purview-information-protection-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-information-protection-openapi.yml
- filename: microsoft-purview-data-security-governance-openapi.yml
  format: yaml
  label: Microsoft Purview Data Security and Governance API
  slug: microsoft-purview-data-security-and-governance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-data-security-governance-openapi.yml
- filename: microsoft-purview-records-management-openapi.yml
  format: yaml
  label: Microsoft Purview Records Management API
  slug: microsoft-purview-records-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/openapi/microsoft-purview-records-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Microsoft Purview: dual model — user-based Microsoft 365 commerce for the Purview Suite ($12/user/month) and Azure-billed pay-as-you-go meters for data-plane features (Data Map, scanning, classification, Data Estate Insights, Data Security Investigations).'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Security
  ServiceName: Microsoft Purview
  ServiceSubcategory: Data Governance
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  name: purview_suite_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - region
  - account
  name: data_map_capacity_units
  unit: capacity-unit-hour
- aggregation: sum
  dimensions:
  - region
  - source_type
  name: scan_vcore_hours
  unit: vCore-hour
- aggregation: count
  dimensions:
  - region
  - source_type
  name: classified_assets
  unit: asset
- aggregation: max
  dimensions:
  - region
  name: data_estate_insights_assets
  unit: asset-month
- aggregation: count
  dimensions:
  - region
  - investigator
  name: data_security_investigations
  unit: investigation
name: Microsoft Purview Finops
provider_name: Microsoft Purview
provider_slug: microsoft-purview
publisher_name: Microsoft Corporation
service_category: Compliance / Data Governance
slug: microsoft-purview-finops
source_filename: microsoft-purview-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/security/business/microsoft-purview
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Purview\nproviderId: microsoft-purview\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Compliance\n  - Microsoft\n  - Data Governance\ndescription: 'FOCUS-aligned FinOps for Microsoft Purview: dual model — user-based Microsoft 365 commerce\n  for the Purview Suite ($12/user/month) and Azure-billed pay-as-you-go meters for data-plane features\n  (Data Map, scanning, classification, Data Estate Insights, Data Security Investigations).'\nsources:\n  - https://www.microsoft.com/en-us/security/business/microsoft-purview\n  - https://www.microsoft.com/en-us/security/business/purview-suite-pricing\n  - https://azure.microsoft.com/en-us/pricing/details/purview/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Compliance / Data Governance\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Purview\n  ServiceCategory: Security\n  ServiceSubcategory: Data Governance\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: purview_suite_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - assigned_user\n  - name: data_map_capacity_units\n    unit: capacity-unit-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - account\n  - name: scan_vcore_hours\n    unit: vCore-hour\n    aggregation:\
  \ sum\n    dimensions:\n      - region\n      - source_type\n  - name: classified_assets\n    unit: asset\n    aggregation: count\n    dimensions:\n      - region\n      - source_type\n  - name: data_estate_insights_assets\n    unit: asset-month\n    aggregation: max\n    dimensions:\n      - region\n  - name: data_security_investigations\n    unit: investigation\n    aggregation: count\n    dimensions:\n      - region\n      - investigator\nprinciples:\n  - name: Visibility\n    description: Use Azure Cost Management exports plus the Purview governance portal to surface Data\n      Map, scan, and classification consumption; cross-reference Microsoft 365 admin center seat usage\n      for the Suite SKU.\n  - name: Allocation\n    description: Tag Purview accounts and scans with cost-center / data-domain tags; allocate Suite\n      seats via Microsoft 365 license groups; map Data Estate Insights cost back to data-domain owners.\n  - name: Optimization\n    description: Tune scan frequency\
  \ to actual data-change rates; deallocate idle Data Map capacity\n      units between scans; consolidate Purview accounts within a tenant; combine M365 Suite + Azure\n      pay-as-you-go to avoid double-charging users for governance modules already covered.\n  - name: Accountability\n    description: Assign a data-governance budget owner per Purview account; review Cost Management\n      dashboards monthly; alert when scan-vCore-hours exceed forecast by 20%.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-purview/refs/heads/main/finops/microsoft-purview-finops.yml
sources:
- https://www.microsoft.com/en-us/security/business/microsoft-purview
- https://www.microsoft.com/en-us/security/business/purview-suite-pricing
- https://azure.microsoft.com/en-us/pricing/details/purview/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Compliance
- Microsoft
- Data Governance
---
