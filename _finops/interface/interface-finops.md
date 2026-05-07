---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for Interface Inc: a commercial flooring manufacturer with no public API or rate card. FinOps applies primarily to internal IT spend and partner integration cost rather than a public API surface.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Interface, Inc.
  ProviderName: Interface Inc
  PublisherName: Interface, Inc.
  ServiceCategory: Commercial Flooring
  ServiceName: Interface Inc
layout: finops
meters:
- aggregation: sum
  dimensions:
  - partner
  - integration_type
  name: integration_subscription
  unit: month
- aggregation: sum
  dimensions:
  - endpoint
  name: api_requests
  unit: request
name: Interface Finops
provider_name: Interface Inc
provider_slug: interface
publisher_name: Interface, Inc.
service_category: Commercial Flooring
slug: interface-finops
source_filename: interface-finops.yml
source_heading: FinOps Profile
source_url: https://www.interface.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Interface Inc\nproviderId: interface\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Flooring\n  - Commercial\ndescription: 'FOCUS-aligned FinOps placeholder for Interface Inc: a commercial flooring manufacturer\n  with no public API or rate card. FinOps applies primarily to internal IT spend and partner integration\n  cost rather than a public API surface.'\nnotes: Interface Inc does not publish a public API rate card. Meters below model the typical partner-integration\n  surface; cannot be reconciled without a customer contract.\nsources:\n  - https://www.interface.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Interface,\
  \ Inc.\nserviceCategory: Commercial Flooring\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Interface Inc\n  ServiceCategory: Commercial Flooring\n  ProviderName: Interface Inc\n  PublisherName: Interface, Inc.\n  InvoiceIssuerName: Interface, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: integration_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - partner\n      - integration_type\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Track partner integration invoices and shared EDI VAN charges; there is no public\n      Interface usage API.\n  - name: Allocation\n    description: Allocate integration subscription cost to the partner program / customer account that\n      drives it.\n  - name: Optimization\n    description:\
  \ Consolidate EDI partners and shared mappings; review contract scope at renewal.\n  - name: Accountability\n    description: Partner integration owner reviews integration usage and contract renewals annually.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/interface/refs/heads/main/finops/interface-finops.yml
sources:
- https://www.interface.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Flooring
- Commercial
---
