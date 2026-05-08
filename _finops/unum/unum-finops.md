---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: unum-hr-connect-openapi.yml
  format: yaml
  label: Unum HR Connect API
  slug: hr-connect
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unum/refs/heads/main/openapi/unum-hr-connect-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Bundled with Insurance Contract
description: 'FinOps shape for Unum: API access is bundled into a partner or employer benefits contract rather than billed as a developer plan, so a public FOCUS line-item model is not available.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Unum Group
  ProviderName: Unum
  PublisherName: Unum Group
  ServiceCategory: Insurance
  ServiceName: Unum
layout: finops
meters:
- aggregation: count
  description: Access provisioned under a partner or employer agreement; not metered as a developer billing line
  name: contracted_access
  unit: varies
name: Unum Finops
provider_name: Unum
provider_slug: unum
publisher_name: Unum Group
service_category: Insurance
slug: unum-finops
source_filename: unum-finops.yml
source_heading: FinOps Profile
source_url: https://www.unum.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Unum\nproviderId: unum\npublisherName: Unum Group\nserviceCategory: Insurance\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Benefits Administration\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for Unum: API access is bundled into a partner or employer benefits contract rather than billed as a developer plan, so a public FOCUS line-item model is not available.'\nsources:\n  - https://www.unum.com/\nnotes: No public usage-based billing surface for Unum APIs. Costs are embedded in the underlying group insurance/benefits contract; FinOps observability is not exposed by Unum directly.\nbillingModel:\n\
  \  pricingCategory: Bundled with Insurance Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Unum\n  ServiceCategory: Insurance\n  ProviderName: Unum\n  PublisherName: Unum Group\n  InvoiceIssuerName: Unum Group\n  BillingCurrency: USD\nmeters:\n  - name: contracted_access\n    description: Access provisioned under a partner or employer agreement; not metered as a developer billing line\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: API consumption is not surfaced via a public usage API; partners must request usage reports through their Unum account team.\n  - name: Allocation\n    description: Costs flow through the parent benefits/HRIS contract; allocation happens in the customer's HR/finance system, not in Unum-provided telemetry.\n  - name: Optimization\n    description: Optimization is contract-driven (benefit design, integration scope) rather than runtime\
  \ (API call patterns).\n  - name: Accountability\n    description: Owned by the HR / benefits sponsor inside the customer organization, with the integration partner accountable for technical use.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unum/refs/heads/main/finops/unum-finops.yml
sources:
- https://www.unum.com/
specification: FinOps Framework
tags:
- Insurance
- Benefits Administration
- FinOps
- FOCUS
---
