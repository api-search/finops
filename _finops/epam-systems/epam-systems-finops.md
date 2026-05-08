---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (per SOW)
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract / Professional Services
description: 'FinOps view of EPAM Systems: invoicing is contract-driven (T&M, fixed-fee, or managed-service retainers) rather than usage-metered. The FOCUS shape is closer to professional-services billing than to a metered API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: EPAM Systems, Inc.
  ProviderName: EPAM Systems
  PublisherName: EPAM Systems, Inc.
  ServiceCategory: IT Services / Consulting
  ServiceName: EPAM Systems
layout: finops
meters:
- aggregation: sum
  dimensions:
  - sow
  - cost_center
  name: engagement_fees
  unit: month
- aggregation: sum
  dimensions:
  - role
  - sow
  name: time_and_materials_hours
  unit: hour
name: Epam Systems Finops
provider_name: EPAM Systems
provider_slug: epam-systems
publisher_name: EPAM Systems, Inc.
service_category: IT Services / Consulting
slug: epam-systems-finops
source_filename: epam-systems-finops.yml
source_heading: FinOps Profile
source_url: https://www.epam.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: EPAM Systems\nproviderId: epam-systems\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Software Engineering\n  - Consulting\ndescription: 'FinOps view of EPAM Systems: invoicing is contract-driven (T&M, fixed-fee, or managed-service\n  retainers) rather than usage-metered. The FOCUS shape is closer to professional-services billing than\n  to a metered API.'\nsources:\n  - https://www.epam.com\n  - https://developer.epam.com\nnotes: No public pricing or metered billing. FinOps controls focus on engagement-level budget tracking\n  rather than per-API consumption.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: EPAM Systems, Inc.\n\
  serviceCategory: IT Services / Consulting\nbillingModel:\n  pricingCategory: Custom Contract / Professional Services\n  billingFrequency: Monthly (per SOW)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: EPAM Systems\n  ServiceCategory: IT Services / Consulting\n  ProviderName: EPAM Systems\n  PublisherName: EPAM Systems, Inc.\n  InvoiceIssuerName: EPAM Systems, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: engagement_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - sow\n      - cost_center\n  - name: time_and_materials_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - role\n      - sow\nprinciples:\n  - name: Visibility\n    description: Track EPAM SOW spend in your AP system; reconcile invoices monthly against agreed milestones\n      or T&M caps.\n  - name: Allocation\n    description: Tag SOWs with the consuming business unit/product so engagement spend can be allocated.\n  - name:\
  \ Optimization\n    description: Right-size engagement scope; renegotiate rates at renewal; fold managed-service work\n      into fixed-fee where volume is predictable.\n  - name: Accountability\n    description: Engagement owner (named on the SOW) approves invoices; finance reviews variance from\n      forecast monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/epam-systems/refs/heads/main/finops/epam-systems-finops.yml
sources:
- https://www.epam.com
- https://developer.epam.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Software Engineering
- Consulting
---
