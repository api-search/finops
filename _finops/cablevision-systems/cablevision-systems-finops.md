---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories: []
  pricingCategory: Not Applicable
description: FOCUS-aligned FinOps scaffold for Cablevision Systems. The provider does not publish a metered developer API or chargeable API surface, so this artifact captures the corporate publisher and service category for cataloging purposes only — there are no API meters, FOCUS columns are minimal, and consumers should treat this as a placeholder.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Altice USA, Inc.
  ProviderName: Cablevision Systems
  PublisherName: Altice USA, Inc.
  ServiceCategory: Telecommunications / Cable ISP
  ServiceName: Cablevision Systems
layout: finops
meters: []
name: Cablevision Systems Finops
provider_name: Cablevision Systems
provider_slug: cablevision-systems
publisher_name: Altice USA, Inc.
service_category: Telecommunications / Cable ISP
slug: cablevision-systems-finops
source_filename: cablevision-systems-finops.yml
source_heading: FinOps Profile
source_url: https://www.alticeusa.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cablevision Systems\nproviderId: cablevision-systems\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Telecommunications\n  - Cable\n  - Internet\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Cablevision Systems. The provider does not publish a metered\n  developer API or chargeable API surface, so this artifact captures the corporate publisher and service\n  category for cataloging purposes only — there are no API meters, FOCUS columns are minimal, and consumers\n  should treat this as a placeholder.\nsources:\n  - https://www.alticeusa.com/\n  - https://www.optimum.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Altice USA, Inc.\nserviceCategory: Telecommunications / Cable ISP\nbillingModel:\n  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Cablevision Systems\n  ServiceCategory: Telecommunications / Cable ISP\n  ProviderName: Cablevision Systems\n  PublisherName: Altice USA, Inc.\n  InvoiceIssuerName: Altice USA, Inc.\n  BillingCurrency: USD\nmeters: []\nnotes: |\n  Cablevision Systems was acquired by Altice and now operates as part of Altice USA under the Optimum\n  brand. It does not publish a public, general-purpose developer API or developer pricing. Consumer\n  broadband, TV, and voice services are sold via standard residential / business pricing schedules;\n  B2B integrations are governed by private contracts.\nprinciples:\n  - name: Visibility\n    description: No API spend to make visible because no public API is published. Procurement / facilities / IT\n      visibility\
  \ for this entity is handled through standard vendor-management tooling, not a developer-cost surface.\n  - name: Allocation\n    description: Not applicable to API consumption. Corporate spend allocation is handled by the publisher's\n      standard accounting and cost-center processes.\n  - name: Optimization\n    description: Not applicable to API consumption. Standard procurement-side optimization (contract negotiation,\n      consolidated buying) applies if the entity is engaged commercially.\n  - name: Accountability\n    description: Not applicable to API consumption. Corporate accountability is governed by the publisher's\n      enterprise procurement and finance functions.\nmaintainers:\n  - FN: API Evangelist\n    url: http://apievangelist.com\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cablevision-systems/refs/heads/main/finops/cablevision-systems-finops.yml
sources:
- https://www.alticeusa.com/
- https://www.optimum.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Telecommunications
- Cable
- Internet
- FinOps
- FOCUS
---
