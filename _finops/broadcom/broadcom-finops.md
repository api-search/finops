---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: broadcom-vsphere-automation-openapi.yml
  format: yaml
  label: Broadcom vSphere Automation API
  slug: vsphere-automation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/broadcom/refs/heads/main/openapi/broadcom-vsphere-automation-openapi.yml
- filename: broadcom-operations-for-applications-openapi.yml
  format: yaml
  label: Broadcom Operations for Applications REST API
  slug: operations-for-applications
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/broadcom/refs/heads/main/openapi/broadcom-operations-for-applications-openapi.yml
- filename: broadcom-vmware-cloud-foundation-openapi.yml
  format: yaml
  label: Broadcom VMware Cloud Foundation API
  slug: vmware-cloud-foundation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/broadcom/refs/heads/main/openapi/broadcom-vmware-cloud-foundation-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise License
description: 'FOCUS-aligned FinOps for Broadcom: enterprise license agreements covering VMware Cloud Foundation, vSphere, Aria Operations, Symantec, and Mainframe products. Pricing is core / CPU / socket / seat based and contracted per agreement; APIs ship with the underlying product license rather than being separately metered.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Broadcom Inc.
  PricingCategory: Standard
  PricingUnit: license-year
  ProviderName: Broadcom
  PublisherName: Broadcom Inc.
  ServiceCategory: Enterprise Software
  ServiceName: Broadcom
layout: finops
meters:
- aggregation: max
  description: Per-core licensing for VCF / vSphere subscription editions.
  dimensions:
  - product
  - edition
  - cluster
  name: license_cores
  unit: core
- aggregation: max
  description: Per-host licensing where applicable.
  dimensions:
  - product
  - cluster
  name: license_hosts
  unit: host
- aggregation: max
  description: Aria Operations for Applications metered by points-per-second / data-point ingestion.
  dimensions:
  - tenant
  - source
  name: aria_operations_pps
  unit: point-per-second
- aggregation: max
  description: Annual support subscription tied to the product license.
  dimensions:
  - product
  - support_tier
  name: support_subscription
  unit: year
name: Broadcom Finops
provider_name: Broadcom
provider_slug: broadcom
publisher_name: Broadcom Inc.
service_category: Enterprise Software & Infrastructure
slug: broadcom-finops
source_filename: broadcom-finops.yml
source_heading: FinOps Profile
source_url: https://developer.broadcom.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Broadcom\nproviderId: broadcom\npublisherName: Broadcom Inc.\nserviceCategory: Enterprise Software & Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud Infrastructure\n  - Virtualization\n  - Observability\n  - Mainframe\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Broadcom: enterprise license agreements covering VMware Cloud\n  Foundation, vSphere, Aria Operations, Symantec, and Mainframe products. Pricing is core / CPU / socket\n  / seat based and contracted per agreement; APIs ship with the underlying product license rather than\n  being separately metered.'\nsources:\n  - https://developer.broadcom.com/\n\
  \  - https://www.broadcom.com/products/software\nnotes: Broadcom is not metered per API call; cost is governed by the enterprise license agreement.\nbillingModel:\n  pricingCategory: Enterprise License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Broadcom\n  ServiceCategory: Enterprise Software\n  ProviderName: Broadcom\n  PublisherName: Broadcom Inc.\n  InvoiceIssuerName: Broadcom Inc.\n  BillingCurrency: USD\n  PricingCategory: Standard\n  PricingUnit: license-year\nmeters:\n  - name: license_cores\n    description: Per-core licensing for VCF / vSphere subscription editions.\n    unit: core\n    aggregation: max\n    dimensions:\n      - product\n      - edition\n      - cluster\n  - name: license_hosts\n    description: Per-host licensing where applicable.\n    unit: host\n    aggregation: max\n    dimensions:\n      - product\n      - cluster\n  - name: aria_operations_pps\n    description:\
  \ Aria Operations for Applications metered by points-per-second / data-point ingestion.\n    unit: point-per-second\n    aggregation: max\n    dimensions:\n      - tenant\n      - source\n  - name: support_subscription\n    description: Annual support subscription tied to the product license.\n    unit: year\n    aggregation: max\n    dimensions:\n      - product\n      - support_tier\nprinciples:\n  - name: Visibility\n    description: Pull license entitlements from the Broadcom Support Portal, ingestion / query usage\n      from Aria Operations dashboards, and reconcile against the contracted license counts and SaaS\n      ceilings.\n  - name: Allocation\n    description: Allocate VCF / vSphere license cost to hosting infrastructure cost centers; allocate\n      Aria Operations ingestion to the consuming application teams.\n  - name: Optimization\n    description: Right-size cluster core counts before renewal, retire idle observability sources to\n      lower points-per-second, consolidate\
  \ SDDC instances, and time license true-ups with capacity reviews.\n  - name: Accountability\n    description: Designate a Broadcom license owner per product line; review entitlement vs deployed\n      usage on a quarterly cadence and forecast renewals against infrastructure roadmaps.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/broadcom/refs/heads/main/finops/broadcom-finops.yml
sources:
- https://developer.broadcom.com/
- https://www.broadcom.com/products/software
specification: FinOps Framework
tags:
- Cloud Infrastructure
- Virtualization
- Observability
- Mainframe
- FinOps
- FOCUS
---
