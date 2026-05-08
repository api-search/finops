---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: state-farm-renters-insurance-openapi.yml
  format: yaml
  label: Renters Insurance API
  slug: renters-insurance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/state-farm/refs/heads/main/openapi/state-farm-renters-insurance-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: State Farm has no public, metered API surface. There is no FOCUS-billable API line; any cost lives in a private B2B / vendor contract negotiated outside of a self-serve developer program.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: State Farm Mutual Automobile Insurance Company
  ProviderName: State Farm
  PublisherName: State Farm Mutual Automobile Insurance Company
  ServiceCategory: Insurance / Financial Services
  ServiceName: State Farm
layout: finops
meters:
- aggregation: sum
  description: Placeholder for line items defined in a State Farm B2B / partner contract.
  name: contracted_engagement
  unit: varies
name: State Farm Finops
provider_name: State Farm
provider_slug: state-farm
publisher_name: State Farm Mutual Automobile Insurance Company
service_category: Insurance / Financial Services
slug: state-farm-finops
source_filename: state-farm-finops.yml
source_heading: FinOps Profile
source_url: https://www.statefarm.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: State Farm\nproviderId: state-farm\npublisherName: State Farm Mutual Automobile Insurance Company\nserviceCategory: Insurance / Financial Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Insurance\ndescription: State Farm has no public, metered API surface. There is no FOCUS-billable API line; any\n  cost lives in a private B2B / vendor contract negotiated outside of a self-serve developer program.\nsources:\n  - https://www.statefarm.com/\nnotes: No public State Farm API billing surface to reconcile. Meters and FOCUS columns are placeholders\n  pending a contracted engagement.\nbillingModel:\n\
  \  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: State Farm\n  ServiceCategory: Insurance / Financial Services\n  ProviderName: State Farm\n  PublisherName: State Farm Mutual Automobile Insurance Company\n  InvoiceIssuerName: State Farm Mutual Automobile Insurance Company\n  BillingCurrency: USD\nmeters:\n  - name: contracted_engagement\n    description: Placeholder for line items defined in a State Farm B2B / partner contract.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is whatever reporting the negotiated B2B contract exposes — there is no public\n      State Farm usage or billing API.\n  - name: Allocation\n    description: Allocate the partnership cost line in your own ERP; State Farm does not provide a self-serve\n      cost breakdown.\n  - name: Optimization\n    description: Optimization happens at contract / SLA renegotiation,\
  \ not via a self-serve plan change.\n  - name: Accountability\n    description: A single business owner of the State Farm partnership relationship should own the engagement\n      cost line and renewal.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/state-farm/refs/heads/main/finops/state-farm-finops.yml
sources:
- https://www.statefarm.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Insurance
---
