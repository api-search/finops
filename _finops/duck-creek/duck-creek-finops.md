---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: duck-creek-policy-openapi.yml
  format: yaml
  label: Duck Creek Anywhere REST API
  slug: duck-creek-anywhere-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/duck-creek/refs/heads/main/openapi/duck-creek-policy-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: Enterprise SaaS
description: FOCUS-aligned FinOps shape for Duck Creek. Billing is enterprise SaaS contract per carrier tenant; per-API-call pricing is not surfaced, though carriers often see Anywhere call volumes feed internal capacity planning.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Duck Creek Technologies, Inc.
  ProviderName: Duck Creek Technologies
  PublisherName: Duck Creek Technologies, Inc.
  ServiceCategory: Insurance Core SaaS
  ServiceName: Duck Creek Suite
layout: finops
meters:
- aggregation: count
  description: Active Duck Creek Suite tenants
  dimensions:
  - product
  name: tenant_subscription
  unit: tenant
- aggregation: count
  description: Policies under management (typical contractual sizing dimension)
  dimensions:
  - line_of_business
  name: policies_in_force
  unit: policy
- aggregation: sum
  description: Internal observability of calls against Duck Creek Anywhere
  dimensions:
  - api
  - line_of_business
  name: anywhere_api_calls
  unit: request
name: Duck Creek Finops
provider_name: duck-creek
provider_slug: duck-creek
publisher_name: Duck Creek Technologies, Inc.
service_category: Insurance Core SaaS
slug: duck-creek-finops
source_filename: duck-creek-finops.yml
source_heading: FinOps Profile
source_url: https://www.duckcreek.com/duck-creek-anywhere/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Duck Creek\nproviderId: duck-creek\npublisherName: Duck Creek Technologies, Inc.\nserviceCategory: Insurance Core SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Policy\n  - Claims\n  - Billing\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Duck Creek. Billing is enterprise SaaS contract per carrier\n  tenant; per-API-call pricing is not surfaced, though carriers often see Anywhere call volumes feed internal\n  capacity planning.\nnotes: No public per-call meter; reconciled=false.\nsources:\n  - https://www.duckcreek.com/duck-creek-anywhere/\n  - https://www.duckcreek.com/product/duck-creek-platform/\n\
  billingModel:\n  pricingCategory: Enterprise SaaS\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: Duck Creek Suite\n  ServiceCategory: Insurance Core SaaS\n  ProviderName: Duck Creek Technologies\n  PublisherName: Duck Creek Technologies, Inc.\n  InvoiceIssuerName: Duck Creek Technologies, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: tenant_subscription\n    description: Active Duck Creek Suite tenants\n    unit: tenant\n    aggregation: count\n    dimensions:\n      - product\n  - name: policies_in_force\n    description: Policies under management (typical contractual sizing dimension)\n    unit: policy\n    aggregation: count\n    dimensions:\n      - line_of_business\n  - name: anywhere_api_calls\n    description: Internal observability of calls against Duck Creek Anywhere\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - line_of_business\n\
  principles:\n  - name: Visibility\n    description: Reconcile the Duck Creek Suite invoice against contracted policies-in-force, products,\n      and tenant scope; track Anywhere call volumes for internal capacity planning.\n  - name: Allocation\n    description: Allocate Duck Creek cost across personal vs. commercial lines and individual products\n      (Policy, Billing, Claims).\n  - name: Optimization\n    description: Use Anywhere Managed Integrations rather than rebuilding third-party connectors; cache\n      reference data; consolidate Anywhere call patterns to stay within tenant capacity.\n  - name: Accountability\n    description: Carrier IT / digital owner is accountable for Duck Creek spend and contract renewal terms.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/duck-creek/refs/heads/main/finops/duck-creek-finops.yml
sources:
- https://www.duckcreek.com/duck-creek-anywhere/
- https://www.duckcreek.com/product/duck-creek-platform/
specification: FinOps Framework
tags:
- Insurance
- Policy
- Claims
- Billing
- SaaS
- FinOps
- FOCUS
---
