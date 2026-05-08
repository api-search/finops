---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: quorum-land-management-openapi.yml
  format: yaml
  label: Quorum Land Management API
  slug: quorum-land-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quorum/refs/heads/main/openapi/quorum-land-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Enterprise License
description: FOCUS-aligned FinOps for Quorum Software is contract-based; Land Management, Royalty Accounting, and other modules are licensed per enterprise agreement rather than metered by API call.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Quorum Software
  ProviderName: Quorum Software
  PublisherName: Quorum Software
  ServiceCategory: Energy Software
  ServiceName: Quorum Software
layout: finops
meters:
- aggregation: sum
  description: Enterprise license covering the contracted Quorum modules and API access.
  dimensions:
  - contract
  - module
  name: license_contract
  unit: varies
name: Quorum Finops
provider_name: Quorum Software
provider_slug: quorum
publisher_name: Quorum Software
service_category: Energy Software
slug: quorum-finops
source_filename: quorum-finops.yml
source_heading: FinOps Profile
source_url: https://www.quorumsoftware.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Quorum Software\nproviderId: quorum\npublisherName: Quorum Software\nserviceCategory: Energy Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Oil & Gas\n  - FinOps\n  - FOCUS\nnotes: Quorum Software does not publish a per-API meter or invoice surface; FinOps mapping is anchored\n  to the enterprise software contract.\ndescription: FOCUS-aligned FinOps for Quorum Software is contract-based; Land Management, Royalty Accounting,\n  and other modules are licensed per enterprise agreement rather than metered by API call.\nsources:\n  - https://www.quorumsoftware.com/\nbillingModel:\n  pricingCategory:\
  \ Enterprise License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Quorum Software\n  ServiceCategory: Energy Software\n  ProviderName: Quorum Software\n  PublisherName: Quorum Software\n  InvoiceIssuerName: Quorum Software\n  BillingCurrency: USD\nmeters:\n  - name: license_contract\n    description: Enterprise license covering the contracted Quorum modules and API access.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\n      - module\nprinciples:\n  - name: Visibility\n    description: Surface Quorum spend through the enterprise license register; the platform itself\n      exposes operational telemetry inside the customer deployment but not as a billing meter.\n  - name: Allocation\n    description: Allocate license cost across the upstream business units consuming Land, Royalty, or\n      Production modules; tag well or tract data to the operating asset for downstream FinOps reporting.\n\
  \  - name: Optimization\n    description: Right-size the licensed module set at renewal; deactivate modules and integrations\n      that are no longer in use to avoid carrying capacity beyond steady-state need.\n  - name: Accountability\n    description: The land/operations IT team owns the Quorum contract; finance reviews module utilization\n      against contracted entitlements at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/quorum/refs/heads/main/finops/quorum-finops.yml
sources:
- https://www.quorumsoftware.com/
specification: FinOps Framework
tags:
- Energy
- Oil & Gas
- FinOps
- FOCUS
---
