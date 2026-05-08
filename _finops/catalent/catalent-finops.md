---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Milestone
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Custom (MSA / Project)
description: FOCUS-aligned FinOps scaffold for Catalent. Catalent invoices are project / MSA-driven CDMO service fees rather than per-API-call charges; meters track integration usage but the dominant cost line is the underlying contract.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Catalent, Inc.
  ProviderName: Catalent
  PublisherName: Catalent, Inc.
  ServiceCategory: Pharmaceutical Services
  ServiceName: Catalent CDMO Services
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - customer
  name: api_requests
  unit: request
- aggregation: count
  dimensions:
  - project
  - service_line
  name: project_milestones_invoiced
  unit: milestone
name: Catalent Finops
provider_name: Catalent
provider_slug: catalent
publisher_name: Catalent, Inc.
service_category: Pharmaceutical Services
slug: catalent-finops
source_filename: catalent-finops.yml
source_heading: FinOps Profile
source_url: https://www.catalent.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Catalent\nproviderId: catalent\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Pharmaceutical Services\n  - Drug Delivery\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps scaffold for Catalent. Catalent invoices are project / MSA-driven CDMO\n  service fees rather than per-API-call charges; meters track integration usage but the dominant cost\n  line is the underlying contract.'\nnotes: Cost surface is contract-driven, not API-priced. Meters reflect integration telemetry useful for\n  partner monitoring, not invoice line items.\nsources:\n  - https://www.catalent.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Catalent, Inc.\nserviceCategory:\
  \ Pharmaceutical Services\nbillingModel:\n  pricingCategory: Custom (MSA / Project)\n  billingFrequency: Per-Milestone\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Catalent CDMO Services\n  ServiceCategory: Pharmaceutical Services\n  ProviderName: Catalent\n  PublisherName: Catalent, Inc.\n  InvoiceIssuerName: Catalent, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - customer\n  - name: project_milestones_invoiced\n    unit: milestone\n    aggregation: count\n    dimensions:\n      - project\n      - service_line\nprinciples:\n  - name: Visibility\n    description: Track Catalent project spend through the MSA-defined reporting; integration call counts\n      provide a secondary signal of system load, not cost.\n  - name: Allocation\n    description: Allocate Catalent fees to the originating drug program / project; tag integration\
  \ calls\n      with the program identifier.\n  - name: Optimization\n    description: Use scope changes, milestone restructuring, and supplier consolidation rather than per-call\n      tuning to reduce CDMO spend.\n  - name: Accountability\n    description: A program / supply-chain owner reconciles Catalent invoices against the MSA; IT owns\n      the integration uptime SLA.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/catalent/refs/heads/main/finops/catalent-finops.yml
sources:
- https://www.catalent.com
specification: FinOps Framework
tags:
- Pharmaceutical Services
- Drug Delivery
- FinOps
- FOCUS
---
