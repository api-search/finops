---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Managed Services Contract
description: FOCUS-aligned FinOps for R1 RCM is contract-based; the engagement is a managed services agreement rather than per-API metering.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: R1 RCM Inc.
  ProviderName: R1 RCM
  PublisherName: R1 RCM Inc.
  ServiceCategory: Healthcare Services
  ServiceName: R1 RCM
layout: finops
meters:
- aggregation: sum
  description: Revenue-cycle services contract; pricing usually scales with collected revenue and service scope rather than API calls.
  dimensions:
  - contract
  name: services_contract
  unit: varies
name: R1 Rcm Finops
provider_name: R1 RCM
provider_slug: r1-rcm
publisher_name: R1 RCM Inc.
service_category: Healthcare Services
slug: r1-rcm-finops
source_filename: r1-rcm-finops.yml
source_heading: FinOps Profile
source_url: https://www.r1rcm.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: R1 RCM\nproviderId: r1-rcm\npublisherName: R1 RCM Inc.\nserviceCategory: Healthcare Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - Revenue Cycle\n  - FinOps\n  - FOCUS\nnotes: R1 RCM does not publish a per-API meter or invoice surface; commercial terms are folded into\n  the broader revenue-cycle services contract.\ndescription: FOCUS-aligned FinOps for R1 RCM is contract-based; the engagement is a managed services\n  agreement rather than per-API metering.\nsources:\n  - https://www.r1rcm.com/\nbillingModel:\n  pricingCategory: Managed Services Contract\n  billingFrequency: Per-Invoice\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: R1 RCM\n  ServiceCategory: Healthcare Services\n  ProviderName: R1 RCM\n  PublisherName: R1 RCM Inc.\n  InvoiceIssuerName: R1 RCM Inc.\n  BillingCurrency: USD\nmeters:\n  - name: services_contract\n    description: Revenue-cycle services contract; pricing usually scales with collected revenue and\n      service scope rather than API calls.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Surface R1 RCM spend through the customer-side procurement and finance systems; the\n      vendor does not publish a self-serve usage API.\n  - name: Allocation\n    description: Allocate the services fee against the patient-financial-services and revenue-cycle\n      cost centers covered by the contract.\n  - name: Optimization\n    description: Optimization happens at services contract renewal; review collection-rate and DSO performance\n      against\
  \ the agreed service levels.\n  - name: Accountability\n    description: Finance and revenue-cycle leadership co-own the R1 RCM relationship; clinical IT routes\n      integration changes through the R1 account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/r1-rcm/refs/heads/main/finops/r1-rcm-finops.yml
sources:
- https://www.r1rcm.com/
specification: FinOps Framework
tags:
- Healthcare
- Revenue Cycle
- FinOps
- FOCUS
---
