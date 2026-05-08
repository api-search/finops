---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: acronis-account-management-openapi.yaml
  format: yaml
  label: Acronis Account Management API
  slug: account-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acronis/refs/heads/main/openapi/acronis-account-management-openapi.yaml
- filename: acronis-agent-management-openapi.yaml
  format: yaml
  label: Acronis Agent Management REST API
  slug: agent-management-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acronis/refs/heads/main/openapi/acronis-agent-management-openapi.yaml
- filename: acronis-task-manager-openapi.yaml
  format: yaml
  label: Acronis Task Manager API
  slug: task-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acronis/refs/heads/main/openapi/acronis-task-manager-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription + Pay-As-You-Go
description: FOCUS-aligned FinOps for Acronis. Two distinct shapes — consumer / SOHO True Image as a fixed-tier annual subscription per device, and Cyber Protect Cloud as MSP usage-based billing per workload + per GB of cloud storage with optional advanced packs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Acronis International GmbH
  ProviderName: Acronis
  PublisherName: Acronis International GmbH
  ServiceCategory: Cyber Protection / Backup
  ServiceName: Acronis
layout: finops
meters:
- aggregation: max
  description: A protected workload in Cyber Protect Cloud (server, workstation, VM, mailbox, mobile, Microsoft 365 seat, Google Workspace seat, hosted website).
  dimensions:
  - workload_type
  - tenant
  - region
  name: protected_workload
  unit: workload
- aggregation: max
  description: Acronis Cloud storage consumed for backup / DR / archive.
  dimensions:
  - tenant
  - storage_class
  - region
  name: cloud_storage
  unit: GB
- aggregation: sum
  description: Disaster Recovery compute points / runtime when Acronis DR is invoked.
  dimensions:
  - tenant
  - vm
  name: dr_compute
  unit: compute-point
- aggregation: max
  description: Add-on packs (Advanced Backup, Advanced DR, Advanced Email Security, EDR, XDR, MDR, Advanced Management, Advanced DLP) attached to workloads.
  dimensions:
  - pack
  - tenant
  name: advanced_pack
  unit: workload-pack
- aggregation: max
  description: True Image annual per-device subscription seat (consumer line).
  dimensions:
  - edition
  name: device_subscription
  unit: device-year
name: Acronis Finops
provider_name: Acronis
provider_slug: acronis
publisher_name: Acronis International GmbH
service_category: Cyber Protection / Backup / Endpoint Security
slug: acronis-finops
source_filename: acronis-finops.yml
source_heading: FinOps Profile
source_url: https://www.acronis.com/en/products/true-image/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Acronis\nproviderId: acronis\npublisherName: Acronis International GmbH\nserviceCategory: Cyber Protection / Backup / Endpoint Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cybersecurity\n  - Data Protection\n  - Backup\n  - Endpoint Management\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Acronis. Two distinct shapes — consumer / SOHO True Image as a\n  fixed-tier annual subscription per device, and Cyber Protect Cloud as MSP usage-based billing per\n  workload + per GB of cloud storage with optional advanced packs.\nsources:\n  - https://www.acronis.com/en/products/true-image/\n  - https://www.acronis.com/en-us/products/cloud/cyber-protect/\n\
  billingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Acronis\n  ServiceCategory: Cyber Protection / Backup\n  ProviderName: Acronis\n  PublisherName: Acronis International GmbH\n  InvoiceIssuerName: Acronis International GmbH\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: protected_workload\n    description: A protected workload in Cyber Protect Cloud (server, workstation, VM, mailbox, mobile,\n      Microsoft 365 seat, Google Workspace seat, hosted website).\n    unit: workload\n    aggregation: max\n    dimensions:\n      - workload_type\n      - tenant\n      - region\n  - name: cloud_storage\n    description: Acronis Cloud storage consumed for backup / DR / archive.\n    unit: GB\n    aggregation: max\n    dimensions:\n      - tenant\n      - storage_class\n      - region\n  - name: dr_compute\n    description: Disaster\
  \ Recovery compute points / runtime when Acronis DR is invoked.\n    unit: compute-point\n    aggregation: sum\n    dimensions:\n      - tenant\n      - vm\n  - name: advanced_pack\n    description: Add-on packs (Advanced Backup, Advanced DR, Advanced Email Security, EDR, XDR, MDR,\n      Advanced Management, Advanced DLP) attached to workloads.\n    unit: workload-pack\n    aggregation: max\n    dimensions:\n      - pack\n      - tenant\n  - name: device_subscription\n    description: True Image annual per-device subscription seat (consumer line).\n    unit: device-year\n    aggregation: max\n    dimensions:\n      - edition\nprinciples:\n  - name: Visibility\n    description: Use the Acronis Cyber Cloud Reports API and the partner portal usage reports to pull\n      per-tenant workload and storage counts; True Image consumer license counts come from the personal\n      account portal.\n  - name: Allocation\n    description: Allocate workload and storage cost to the end-customer tenant\
  \ in MSP scenarios; allocate\n      consumer True Image seats to the household / individual using them.\n  - name: Optimization\n    description: Tune backup schedules and retention policies to manage cloud-storage growth, leverage\n      Acronis local-only storage where possible, deactivate unused advanced packs, and consolidate workloads\n      onto a single agent rather than overlapping point tools.\n  - name: Accountability\n    description: MSP service-delivery owners reconcile per-tenant usage monthly; consumer True Image\n      cost is owned by the individual account holder.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/acronis/refs/heads/main/finops/acronis-finops.yml
sources:
- https://www.acronis.com/en/products/true-image/
- https://www.acronis.com/en-us/products/cloud/cyber-protect/
specification: FinOps Framework
tags:
- Cybersecurity
- Data Protection
- Backup
- Endpoint Management
- FinOps
- FOCUS
---
