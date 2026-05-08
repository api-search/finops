---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-endpoint-configuration-management-configmgr-rest-api-openapi.yml
  format: yaml
  label: Configuration Manager REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/openapi/microsoft-endpoint-configuration-management-configmgr-rest-api-openapi.yml
- filename: microsoft-endpoint-configuration-management-intune-graph-api-openapi.yml
  format: yaml
  label: Microsoft Intune Graph API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/openapi/microsoft-endpoint-configuration-management-intune-graph-api-openapi.yml
- filename: microsoft-endpoint-configuration-management-intune-data-warehouse-api-openapi.yml
  format: yaml
  label: Intune Data Warehouse API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/openapi/microsoft-endpoint-configuration-management-intune-data-warehouse-api-openapi.yml
- filename: microsoft-endpoint-configuration-management-intune-reporting-export-api-openapi.yml
  format: yaml
  label: Intune Reporting Export API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/openapi/microsoft-endpoint-configuration-management-intune-reporting-export-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Microsoft Configuration Manager: per-user (Microsoft 365 / Intune) or per-device (System Center / Core CAL) subscription bundled with the Microsoft Intune family or an Enterprise Agreement; no per-call API charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Endpoint Management
  ServiceName: Microsoft Configuration Manager
layout: finops
meters:
- aggregation: max
  description: Count of devices currently managed by a Configuration Manager site
  dimensions:
  - site
  - device_type
  - os
  name: managed_devices
  unit: device
- aggregation: sum
  description: Microsoft Intune Plan 1 seats granting Configuration Manager co-management rights
  dimensions:
  - tenant
  - sku
  name: intune_seats
  unit: seat
- aggregation: sum
  description: Microsoft 365 E3 / E5 seats that include Configuration Manager + Intune entitlement
  dimensions:
  - tenant
  - sku
  name: m365_seats
  unit: seat
- aggregation: sum
  description: Cloud Management Gateway data egress (Azure)
  name: cmg_egress
  unit: GB
name: Microsoft Endpoint Configuration Management Finops
provider_name: Microsoft Endpoint Configuration Management
provider_slug: microsoft-endpoint-configuration-management
publisher_name: Microsoft Corporation
service_category: Endpoint Management
slug: microsoft-endpoint-configuration-management-finops
source_filename: microsoft-endpoint-configuration-management-finops.yml
source_heading: FinOps Profile
source_url: https://learn.microsoft.com/en-us/intune/configmgr/core/understand/configuration-manager-faq
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Endpoint Configuration Management\nproviderId: microsoft-endpoint-configuration-management\npublisherName: Microsoft Corporation\nserviceCategory: Endpoint Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Endpoint Management\n  - Configuration Manager\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Configuration Manager: per-user (Microsoft 365 / Intune)\n  or per-device (System Center / Core CAL) subscription bundled with the Microsoft Intune family or an\n  Enterprise Agreement; no per-call API charge.'\nsources:\n  - https://learn.microsoft.com/en-us/intune/configmgr/core/understand/configuration-manager-faq\n\
  \  - https://www.microsoft.com/en-us/security/business/microsoft-intune-pricing\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Configuration Manager\n  ServiceCategory: Endpoint Management\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: managed_devices\n    description: Count of devices currently managed by a Configuration Manager site\n    unit: device\n    aggregation: max\n    dimensions:\n      - site\n      - device_type\n      - os\n  - name: intune_seats\n    description: Microsoft Intune Plan 1 seats granting Configuration Manager co-management rights\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: m365_seats\n    description: Microsoft\
  \ 365 E3 / E5 seats that include Configuration Manager + Intune entitlement\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: cmg_egress\n    description: Cloud Management Gateway data egress (Azure)\n    unit: GB\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use the Configuration Manager console + AdminService REST API for on-prem inventory;\n      Microsoft 365 admin centre and Cost Management for the seat licences.\n  - name: Allocation\n    description: Tag managed devices with collection / OU / cost-centre; flow seat costs from Microsoft\n      365 admin centre to teams.\n  - name: Optimization\n    description: Consolidate Configuration Manager sites to reduce SQL and management-point footprint;\n      use co-management with Intune to retire legacy site servers; right-size the Cloud Management Gateway.\n  - name: Accountability\n    description: Endpoint engineering owns site-server health and CMG sizing; IT\
  \ finance owns the M365\n      / Intune SKU mix.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/finops/microsoft-endpoint-configuration-management-finops.yml
sources:
- https://learn.microsoft.com/en-us/intune/configmgr/core/understand/configuration-manager-faq
- https://www.microsoft.com/en-us/security/business/microsoft-intune-pricing
specification: FinOps Framework
tags:
- Endpoint Management
- Configuration Manager
- Microsoft
- FinOps
- FOCUS
---
