---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cigna-patient-access-api-openapi.yml
  format: yaml
  label: Cigna Patient Access API
  slug: patient-access-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-patient-access-api-openapi.yml
- filename: cigna-provider-directory-api-openapi.yml
  format: yaml
  label: Cigna Provider Directory API
  slug: provider-directory-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-provider-directory-api-openapi.yml
- filename: cigna-drug-formulary-api-openapi.yml
  format: yaml
  label: Cigna Drug Formulary API
  slug: drug-formulary-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-drug-formulary-api-openapi.yml
- filename: cigna-provider-access-api-openapi.yml
  format: yaml
  label: Cigna Provider Access API
  slug: provider-access-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-provider-access-api-openapi.yml
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A
  chargeCategories:
  - Adjustment
  pricingCategory: No Customer Charge (Regulatory)
description: 'FOCUS-aligned FinOps for Cigna FHIR APIs: there is no commercial billing surface — the endpoints are CMS-mandated and provided at no charge to compliant third-party applications. Cost-of-ownership for the Cigna engineering team manifests as internal infrastructure spend (cloud, gateway, identity) tracked by Cigna FinOps, not as customer-facing line items.'
focus_columns:
  BillingCurrency: N/A
  ChargeCategory: Adjustment
  InvoiceIssuerName: N/A
  PricingCategory: No Charge (Regulatory)
  ProviderName: Cigna
  PublisherName: Cigna Health and Life Insurance Company
  ServiceCategory: Healthcare / Interoperability
  ServiceName: Cigna Developer FHIR APIs
layout: finops
meters:
- aggregation: sum
  description: FHIR API request volume (operational signal — not a customer billing meter)
  dimensions:
  - api
  - application
  - environment
  name: api_requests
  unit: request
- aggregation: sum
  description: SMART on FHIR / OAuth 2.0 token issuance events
  dimensions:
  - application
  name: token_issuance
  unit: token
- aggregation: max
  description: Distinct third-party applications registered against the developer portal
  dimensions:
  - environment
  name: registered_applications
  unit: application
- aggregation: sum
  description: Bytes of FHIR Bundle data returned to clients (network cost signal)
  dimensions:
  - api
  name: bytes_egressed
  unit: GB
name: Cigna Finops
provider_name: Cigna
provider_slug: cigna
publisher_name: Cigna Health and Life Insurance Company
service_category: Healthcare / Health Insurance
slug: cigna-finops
source_filename: cigna-finops.yml
source_heading: FinOps Profile
source_url: https://developer.cigna.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cigna\nproviderId: cigna\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - CMS Interoperability\n  - FHIR\n  - Healthcare\n  - Patient Access\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Cigna FHIR APIs: there is no commercial billing surface — the\n  endpoints are CMS-mandated and provided at no charge to compliant third-party applications.\n  Cost-of-ownership for the Cigna engineering team manifests as internal infrastructure spend\n  (cloud, gateway, identity) tracked by Cigna FinOps, not as customer-facing line items.'\nnotes: Cigna does not bill external developers for FHIR API access. The FinOps shape below describes\n  Cigna's internal cost surface for operating the developer platform.\nsources:\n  - https://developer.cigna.com/\n  - https://developer.cigna.com/docs/service-apis\nalignedWith:\n  framework: FinOps\
  \ Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cigna Health and Life Insurance Company\nserviceCategory: Healthcare / Health Insurance\nbillingModel:\n  pricingCategory: No Customer Charge (Regulatory)\n  billingFrequency: N/A\n  billingCurrency: N/A\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Cigna Developer FHIR APIs\n  ServiceCategory: Healthcare / Interoperability\n  ProviderName: Cigna\n  PublisherName: Cigna Health and Life Insurance Company\n  InvoiceIssuerName: N/A\n  BillingCurrency: N/A\n  ChargeCategory: Adjustment\n  PricingCategory: No Charge (Regulatory)\nmeters:\n  - name: api_requests\n    description: FHIR API request volume (operational signal — not a customer billing meter)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - application\n      - environment\n  -\
  \ name: token_issuance\n    description: SMART on FHIR / OAuth 2.0 token issuance events\n    unit: token\n    aggregation: sum\n    dimensions:\n      - application\n  - name: registered_applications\n    description: Distinct third-party applications registered against the developer portal\n    unit: application\n    aggregation: max\n    dimensions:\n      - environment\n  - name: bytes_egressed\n    description: Bytes of FHIR Bundle data returned to clients (network cost signal)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\nprinciples:\n  - name: Visibility\n    description: Track FHIR API usage internally through API gateway logs, the OAuth issuer, and the\n      developer portal. Surface the operational cost back to interoperability and compliance teams.\n  - name: Allocation\n    description: Allocate developer-platform infrastructure cost to interoperability / regulatory\n      compliance and to the digital member-experience program rather than to a customer\
  \ cost center.\n  - name: Optimization\n    description: Cache Provider Directory and Drug Formulary FHIR responses, scale gateway capacity to\n      the diurnal Patient Access curve, and decommission stale registered applications.\n  - name: Accountability\n    description: Compliance / regulatory affairs owns rule conformance; digital health engineering\n      owns FHIR platform uptime; security owns SMART on FHIR consent and token issuance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/finops/cigna-finops.yml
sources:
- https://developer.cigna.com/
- https://developer.cigna.com/docs/service-apis
specification: FinOps Framework
tags:
- CMS Interoperability
- FHIR
- Healthcare
- Patient Access
- FinOps
- FOCUS
---
