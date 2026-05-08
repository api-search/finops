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
  pricingCategory: Contract / Negotiated
description: FinOps shape for Trellix cannot be reconciled from public sources; pricing is contact-sales only and consumption telemetry sits behind an authenticated developer portal.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Musarubra US LLC (Trellix)
  ProviderName: Trellix
  PublisherName: Musarubra US LLC (Trellix)
  ServiceCategory: Cybersecurity
  ServiceName: Trellix
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  name: license_seats
  unit: seat
name: Trellix Finops
provider_name: Trellix
provider_slug: trellix
publisher_name: Musarubra US LLC (Trellix)
service_category: Cybersecurity
slug: trellix-finops
source_filename: trellix-finops.yml
source_heading: FinOps Profile
source_url: https://www.trellix.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Trellix\nproviderId: trellix\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cybersecurity\n  - Endpoint Security\n  - XDR\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Trellix cannot be reconciled from public sources; pricing is\n  contact-sales only and consumption telemetry sits behind an authenticated developer portal.\nsources:\n  - https://www.trellix.com/pricing/\nnotes: Public pricing page is gated, and Trellix does not publish per-API meter or invoice\n  documentation. FOCUS column values and meters can only be confirmed once a license contract is\n  active and the authenticated developer portal is reviewed.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Musarubra US LLC (Trellix)\nserviceCategory: Cybersecurity\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Trellix\n  ServiceCategory: Cybersecurity\n  ProviderName: Trellix\n  PublisherName: Musarubra US LLC (Trellix)\n  InvoiceIssuerName: Musarubra US LLC (Trellix)\n  BillingCurrency: USD\nmeters:\n  - name: license_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Per-tenant consumption (endpoints, telemetry volume, API usage) is exposed inside the\n      authenticated Trellix Insights / ePO console rather than a public usage API; finance reconciles\n      against the annual license contract.\n  - name: Allocation\n    description: Allocate cost by Trellix product line (EDR, XDR, NDR, ePO) and by managed-tenant when\n      MSSPs operate multi-customer deployments.\n\
  \  - name: Optimization\n    description: Optimization is contractual — right-size protected endpoint counts, retire unused\n      product modules, and consolidate tenants at renewal.\n  - name: Accountability\n    description: Security operations / CISO organization owns the Trellix contract; procurement\n      manages renewal and true-up against actual seat consumption.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trellix/refs/heads/main/finops/trellix-finops.yml
sources:
- https://www.trellix.com/pricing/
specification: FinOps Framework
tags:
- Cybersecurity
- Endpoint Security
- XDR
- FinOps
- FOCUS
---
