---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: None (Partner Agreement)
  chargeCategories:
  - Purchase
  pricingCategory: Bundled with Member Product
description: 'FinOps shape for USAA: there is no developer-billed API surface. Member services are funded through banking/insurance product margins; partner integrations live inside data-sharing agreements rather than a metered API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: USAA
  ProviderName: USAA
  PublisherName: United Services Automobile Association
  ServiceCategory: Financial Services
  ServiceName: USAA
layout: finops
meters:
- aggregation: count
  description: API access provisioned under a partner data-sharing agreement; not metered as a developer billing line
  name: contracted_access
  unit: varies
name: Usaa Finops
provider_name: USAA
provider_slug: usaa
publisher_name: United Services Automobile Association
service_category: Financial Services
slug: usaa-finops
source_filename: usaa-finops.yml
source_heading: FinOps Profile
source_url: https://www.usaa.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: USAA\nproviderId: usaa\npublisherName: United Services Automobile Association\nserviceCategory: Financial Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial Services\n  - Banking\n  - Insurance\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for USAA: there is no developer-billed API surface. Member services are funded through banking/insurance product margins; partner integrations live inside data-sharing agreements rather than a metered API.'\nsources:\n  - https://www.usaa.com/\nnotes: No public usage-based billing surface for USAA APIs. Member-facing services aren't billed per API call; partner\
  \ data-sharing terms are private.\nbillingModel:\n  pricingCategory: Bundled with Member Product\n  billingFrequency: None (Partner Agreement)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: USAA\n  ServiceCategory: Financial Services\n  ProviderName: USAA\n  PublisherName: United Services Automobile Association\n  InvoiceIssuerName: USAA\n  BillingCurrency: USD\nmeters:\n  - name: contracted_access\n    description: API access provisioned under a partner data-sharing agreement; not metered as a developer billing line\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: USAA does not expose a public usage API; partners must reconcile traffic through their own client-side telemetry and any reporting agreed in the data-sharing contract.\n  - name: Allocation\n    description: Costs are not allocated to USAA-issued line items; integration partners absorb their own costs and report internally.\n  - name:\
  \ Optimization\n    description: Optimization is at the integration design level (consumer-permissioned data, refresh cadence, scope minimization) rather than per-call cost.\n  - name: Accountability\n    description: Owned by the integration partner's engineering and risk-management functions, with USAA holding contractual oversight via the data-sharing agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/usaa/refs/heads/main/finops/usaa-finops.yml
sources:
- https://www.usaa.com/
specification: FinOps Framework
tags:
- Financial Services
- Banking
- Insurance
- FinOps
- FOCUS
---
