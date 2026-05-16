---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: active-directory-users-openapi.yaml
  format: yaml
  label: Microsoft Graph Users API
  slug: microsoft-graph-users-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/active-directory/refs/heads/main/openapi/active-directory-users-openapi.yaml
- filename: active-directory-groups-openapi.yaml
  format: yaml
  label: Microsoft Graph Groups API
  slug: microsoft-graph-groups-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/active-directory/refs/heads/main/openapi/active-directory-groups-openapi.yaml
- filename: active-directory-applications-openapi.yaml
  format: yaml
  label: Microsoft Graph Applications and Service Principals API
  slug: microsoft-graph-applications-and-service-principals-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/active-directory/refs/heads/main/openapi/active-directory-applications-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription
description: FOCUS-aligned FinOps for Microsoft Entra ID (the modern Active Directory). Billed per user per month at a tier (Free / P1 / P2 / Suite) with optional standalone identity products (ID Governance, Internet Access, Private Access, Verified ID) and per-workload-identity charges for Workload ID. Programmatic access via Microsoft Graph is rate-limited rather than separately metered.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Identity / Directory Services
  ServiceName: Microsoft Entra ID
layout: finops
meters:
- aggregation: max
  description: Licensed Entra user seat (Free / P1 / P2 / Suite).
  dimensions:
  - tier
  - tenant
  name: entra_user_seat
  unit: seat
- aggregation: max
  description: Standalone Entra ID Governance seat.
  dimensions:
  - tenant
  name: entra_id_governance_seat
  unit: seat
- aggregation: max
  description: Entra Internet Access seat.
  dimensions:
  - tenant
  name: entra_internet_access_seat
  unit: seat
- aggregation: max
  description: Entra Private Access seat.
  dimensions:
  - tenant
  name: entra_private_access_seat
  unit: seat
- aggregation: max
  description: Entra Workload ID — service principal / managed identity protected by Workload ID.
  dimensions:
  - tenant
  name: workload_identity
  unit: workload-identity
- aggregation: sum
  description: ResourceUnit consumption against Microsoft Graph; not directly billed but a leading indicator of where automation pressure exists.
  dimensions:
  - application
  - tenant
  - operation
  name: graph_throttle_consumption
  unit: resource-unit
name: Active Directory Finops
provider_name: Microsoft Active Directory
provider_slug: active-directory
publisher_name: Microsoft Corporation
service_category: Identity / Directory Services
slug: active-directory-finops
source_filename: active-directory-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Active Directory\nproviderId: active-directory\npublisherName: Microsoft Corporation\nserviceCategory: Identity / Directory Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Active Directory\n  - Identity Management\n  - Microsoft Entra\n  - Zero Trust\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Microsoft Entra ID (the modern Active Directory). Billed per user\n  per month at a tier (Free / P1 / P2 / Suite) with optional standalone identity products (ID Governance,\n  Internet Access, Private Access, Verified ID) and per-workload-identity charges for Workload ID. Programmatic\n  access\
  \ via Microsoft Graph is rate-limited rather than separately metered.\nsources:\n  - https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing\n  - https://learn.microsoft.com/en-us/graph/throttling-limits\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Microsoft Entra ID\n  ServiceCategory: Identity / Directory Services\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: entra_user_seat\n    description: Licensed Entra user seat (Free / P1 / P2 / Suite).\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\n      - tenant\n  - name: entra_id_governance_seat\n    description: Standalone Entra ID Governance seat.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: entra_internet_access_seat\n\
  \    description: Entra Internet Access seat.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: entra_private_access_seat\n    description: Entra Private Access seat.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: workload_identity\n    description: Entra Workload ID — service principal / managed identity protected by Workload ID.\n    unit: workload-identity\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: graph_throttle_consumption\n    description: ResourceUnit consumption against Microsoft Graph; not directly billed but a leading\n      indicator of where automation pressure exists.\n    unit: resource-unit\n    aggregation: sum\n    dimensions:\n      - application\n      - tenant\n      - operation\nprinciples:\n  - name: Visibility\n    description: Use Microsoft Cost Management on the EA / MCA enrollment for Entra licensing line items;\n      use the Entra admin center \"Licenses\" pane for assignment\
  \ counts; use the Microsoft Graph activity\n      logs and the x-ms-throttle-limit-percentage header for automation pressure.\n  - name: Allocation\n    description: Allocate Entra seats by AD group → cost center mapping. For Workload ID, tag each managed\n      identity with its owning application and route cost to the consuming product team.\n  - name: Optimization\n    description: Right-tier users (don't put everyone on P2 if only privileged users need PIM); reclaim\n      seats from terminated employees through Lifecycle Workflows; consolidate point identity tools that\n      are duplicated by Entra ID Governance, Internet Access, or Private Access; prefer change-notifications\n      over polling to stay below throttle ceilings.\n  - name: Accountability\n    description: The IAM team owns tier mix and renewals; product owners own their Workload ID footprints\n      and the Graph applications calling on their behalf.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/active-directory/refs/heads/main/finops/active-directory-finops.yml
sources:
- https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing
- https://learn.microsoft.com/en-us/graph/throttling-limits
specification: FinOps Framework
tags:
- Active Directory
- Identity Management
- Microsoft Entra
- Zero Trust
- FinOps
- FOCUS
---
