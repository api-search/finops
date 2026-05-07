---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Custom Enterprise Services
description: Syneos Health sells clinical-research and commercialization services; there is no public usage-metered API surface, so FinOps shape is approximated against the negotiated CRO engagement invoice.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Syneos Health, Inc.
  ProviderName: Syneos Health
  PublisherName: Syneos Health, Inc.
  ServiceCategory: Clinical Research / Biopharmaceutical Services
  ServiceName: Syneos Health
layout: finops
meters:
- aggregation: sum
  description: Contracted clinical and commercialization service consumption defined per engagement.
  name: contracted_services
  unit: varies
name: Syneos Health Finops
provider_name: Syneos Health
provider_slug: syneos-health
publisher_name: Syneos Health, Inc.
service_category: Clinical Research / Biopharmaceutical Services
slug: syneos-health-finops
source_filename: syneos-health-finops.yml
source_heading: FinOps Profile
source_url: https://www.syneoshealth.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Syneos Health\nproviderId: syneos-health\npublisherName: Syneos Health, Inc.\nserviceCategory: Clinical Research / Biopharmaceutical Services\ncreated: '2026-04-19'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Clinical Research\n  - Biopharmaceutical\n  - FinOps\n  - FOCUS\ndescription: Syneos Health sells clinical-research and commercialization services; there is no public usage-metered API surface, so FinOps shape is approximated against the negotiated CRO engagement invoice.\nsources:\n  - https://www.syneoshealth.com\nnotes: No public usage telemetry or FOCUS-aligned export. Cost data must be reconciled from negotiated CRO services\
  \ invoices.\nbillingModel:\n  pricingCategory: Custom Enterprise Services\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Syneos Health\n  ServiceCategory: Clinical Research / Biopharmaceutical Services\n  ProviderName: Syneos Health\n  PublisherName: Syneos Health, Inc.\n  InvoiceIssuerName: Syneos Health, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_services\n    description: Contracted clinical and commercialization service consumption defined per engagement.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Cost visibility flows through Syneos contracted reporting; there is no self-service usage API.\n  - name: Allocation\n    description: Allocation follows the trial / program codes defined in the customer's CRO engagement.\n  - name: Optimization\n    description: Optimization levers are contractual (scope changes, study consolidation, deliverable\
  \ reuse).\n  - name: Accountability\n    description: Sponsor study lead and Syneos engagement manager share accountability for spend versus contracted scope.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/syneos-health/refs/heads/main/finops/syneos-health-finops.yml
sources:
- https://www.syneoshealth.com
specification: FinOps Framework
tags:
- Clinical Research
- Biopharmaceutical
- FinOps
- FOCUS
---
