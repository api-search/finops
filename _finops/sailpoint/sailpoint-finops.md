---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud V3 API
  slug: identity-security-cloud-v3-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/v3/identity-security-cloud-v-3-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud V2024 API
  slug: identity-security-cloud-v2024-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/v2024/identity-security-cloud-v-2024-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud V2025 API
  slug: identity-security-cloud-v2025-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/v2025/identity-security-cloud-v-2025-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud Beta API
  slug: identity-security-cloud-beta-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/beta/identity-security-cloud-beta-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint IdentityIQ SCIM API
  slug: identityiq-scim-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/iiq/identityiq-scim-rest-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud V2026 API
  slug: identity-security-cloud-v2026-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/v2026/identity-security-cloud-v-2026-api/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription / Contact Sales
description: 'FOCUS-aligned FinOps shape for SailPoint Identity Security Cloud: annual subscription priced per identity / per module rather than per API call. API consumption is bounded by a 100 / 10s per-token rate limit and is not separately metered for billing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SailPoint Technologies, Inc.
  ProviderName: SailPoint
  PublisherName: SailPoint Technologies, Inc.
  ServiceCategory: Identity Security
  ServiceName: SailPoint Identity Security Cloud
layout: finops
meters:
- aggregation: max
  dimensions:
  - tier
  name: subscribed_identities
  unit: identity
- aggregation: count
  name: enabled_modules
  unit: module
- aggregation: sum
  dimensions:
  - access_token
  name: api_requests
  unit: request
name: Sailpoint Finops
provider_name: SailPoint
provider_slug: sailpoint
publisher_name: SailPoint Technologies, Inc.
service_category: Identity Security / IGA
slug: sailpoint-finops
source_filename: sailpoint-finops.yml
source_heading: FinOps Profile
source_url: https://www.sailpoint.com/products/identity-security-cloud
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SailPoint\nproviderId: sailpoint\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Identity Security\n  - IAM\n  - B2B\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for SailPoint Identity Security Cloud: annual subscription priced\n  per identity / per module rather than per API call. API consumption is bounded by a 100 / 10s per-token\n  rate limit and is not separately metered for billing.'\nsources:\n  - https://www.sailpoint.com/products/identity-security-cloud\n  - https://developer.sailpoint.com/docs/api/getting-started\nnotes: SailPoint does not publish per-identity prices or invoice-line schemas publicly. The financial\n  unit of consumption is the identity covered by the subscription, not the API request.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SailPoint Technologies, Inc.\nserviceCategory: Identity Security / IGA\nbillingModel:\n  pricingCategory: Subscription / Contact Sales\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: SailPoint Identity Security Cloud\n  ServiceCategory: Identity Security\n  ProviderName: SailPoint\n  PublisherName: SailPoint Technologies, Inc.\n  InvoiceIssuerName: SailPoint Technologies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscribed_identities\n    unit: identity\n    aggregation: max\n    dimensions:\n      - tier\n  - name: enabled_modules\n    unit: module\n    aggregation: count\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - access_token\nprinciples:\n  - name: Visibility\n    description: Pull identity counts, source coverage, and module enablement\
  \ from the SailPoint admin\n      console; correlate with internal HR and joiner/mover/leaver feeds to validate billed identity counts\n      against active workforce.\n  - name: Allocation\n    description: Allocate the SailPoint subscription by business unit using identity ownership (HR org\n      mapping). Tag non-employee identities (contractors, vendors) separately, since they often drive\n      add-on cost.\n  - name: Optimization\n    description: Reduce orphaned and dormant identities ahead of renewal; consolidate sources where possible;\n      avoid token-spam patterns that hit the 100 / 10s gateway limit and cause runaway retry traffic.\n  - name: Accountability\n    description: Identity / IAM team owns SailPoint spend with finance; renewal review cycles should reconcile\n      paid identity counts against active populations and model expected delta for the next term.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sailpoint/refs/heads/main/finops/sailpoint-finops.yml
sources:
- https://www.sailpoint.com/products/identity-security-cloud
- https://developer.sailpoint.com/docs/api/getting-started
specification: FinOps Framework
tags:
- Identity Security
- IAM
- B2B
- FinOps
- FOCUS
---
