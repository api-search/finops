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
  pricingCategory: Internal
description: Aaron's APIs power consumer-facing lease application and account-management flows and are not sold as a developer product. There is no metered API invoice; FinOps mapping is structural only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Aaron's Company, Inc.
  ProviderName: Aaron's
  PublisherName: The Aaron's Company, Inc.
  ServiceCategory: Retail / Consumer Finance
  ServiceName: Aaron's
layout: finops
meters:
- aggregation: sum
  description: Internal application traffic — not externally billed.
  dimensions:
  - endpoint
  name: internal_traffic
  unit: request
name: Aarons Finops
provider_name: Aaron's
provider_slug: aarons
publisher_name: The Aaron's Company, Inc.
service_category: Retail / Consumer Finance
slug: aarons-finops
source_filename: aarons-finops.yml
source_heading: FinOps Profile
source_url: https://www.aarons.com/apply
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Aaron's\nproviderId: aarons\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Lease-to-Own\n  - Retail\n  - Consumer Finance\n  - FinOps\n  - FOCUS\ndescription: Aaron's APIs power consumer-facing lease application and account-management flows and are\n  not sold as a developer product. There is no metered API invoice; FinOps mapping is structural only.\nnotes: No public developer pricing — placeholder only. Aaron's API surface is a cost of running its retail\n  experience, not a billable product.\nsources:\n  - https://www.aarons.com/apply\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Aaron's Company, Inc.\nserviceCategory: Retail / Consumer Finance\n\
  billingModel:\n  pricingCategory: Internal\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Aaron's\n  ServiceCategory: Retail / Consumer Finance\n  ProviderName: Aaron's\n  PublisherName: The Aaron's Company, Inc.\n  InvoiceIssuerName: The Aaron's Company, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: internal_traffic\n    description: Internal application traffic — not externally billed.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Internal cost visibility comes from Aaron's own observability stack; not an externally\n      metered service.\n  - name: Allocation\n    description: Cost is allocated inside Aaron's IT/digital budget rather than to external API consumers.\n  - name: Optimization\n    description: Optimize internally by caching application status and scaling consumer-facing endpoints\n      to lease-application\
  \ demand.\n  - name: Accountability\n    description: Digital experience leadership owns the consumer surface; finance reviews IT operating\n      costs as part of corporate budgeting.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aarons/refs/heads/main/finops/aarons-finops.yml
sources:
- https://www.aarons.com/apply
specification: FinOps Framework
tags:
- Lease-to-Own
- Retail
- Consumer Finance
- FinOps
- FOCUS
---
