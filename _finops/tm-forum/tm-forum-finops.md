---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tm-forum-tmf620-product-catalog-openapi.yaml
  format: yaml
  label: TMF620 Product Catalog Management
  slug: tmf620-product-catalog
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf620-product-catalog-openapi.yaml
- filename: tm-forum-tmf621-trouble-ticket-openapi.yaml
  format: yaml
  label: TMF621 Trouble Ticket Management
  slug: tmf621-trouble-ticket
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf621-trouble-ticket-openapi.yaml
- filename: tm-forum-tmf622-product-ordering-openapi.yaml
  format: yaml
  label: TMF622 Product Order Management
  slug: tmf622-product-ordering
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf622-product-ordering-openapi.yaml
- filename: tm-forum-tmf629-customer-management-openapi.yaml
  format: yaml
  label: TMF629 Customer Management
  slug: tmf629-customer-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf629-customer-management-openapi.yaml
- filename: tm-forum-tmf632-party-management-openapi.yaml
  format: yaml
  label: TMF632 Party Management
  slug: tmf632-party-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf632-party-management-openapi.yaml
- filename: tm-forum-tmf633-service-catalog-openapi.json
  format: json
  label: TMF633 Service Catalog Management
  slug: tmf633-service-catalog
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf633-service-catalog-openapi.json
- filename: tm-forum-tmf634-resource-catalog-openapi.json
  format: json
  label: TMF634 Resource Catalog Management
  slug: tmf634-resource-catalog
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf634-resource-catalog-openapi.json
- filename: tm-forum-tmf637-product-inventory-openapi.yaml
  format: yaml
  label: TMF637 Product Inventory Management
  slug: tmf637-product-inventory
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf637-product-inventory-openapi.yaml
- filename: tm-forum-tmf641-service-ordering-openapi.json
  format: json
  label: TMF641 Service Order Management
  slug: tmf641-service-ordering
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf641-service-ordering-openapi.json
- filename: tm-forum-tmf648-quote-management-openapi.json
  format: json
  label: TMF648 Quote Management
  slug: tmf648-quote-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf648-quote-management-openapi.json
- filename: tm-forum-tmf651-agreement-management-openapi.json
  format: json
  label: TMF651 Agreement Management
  slug: tmf651-agreement-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf651-agreement-management-openapi.json
- filename: tm-forum-tmf666-account-management-openapi.json
  format: json
  label: TMF666 Account Management
  slug: tmf666-account-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/openapi/tm-forum-tmf666-account-management-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Membership
description: TM Forum is a not-for-profit industry association whose direct customer billing surface is association membership rather than API consumption. There is no FOCUS-aligned per-request meter at the TM Forum level; FinOps for "TMF APIs" applies to the operator that implements them.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: TM Forum
  ProviderName: TM Forum
  PublisherName: TM Forum
  ServiceCategory: Industry Standards Body
  ServiceName: TM Forum Membership
layout: finops
meters:
- aggregation: sum
  description: One year of TM Forum association membership at the contracted tier.
  dimensions:
  - tier
  - organization
  name: tm_forum_membership_year
  unit: year
name: Tm Forum Finops
provider_name: TM Forum
provider_slug: tm-forum
publisher_name: TM Forum
service_category: Industry Standards Body
slug: tm-forum-finops
source_filename: tm-forum-finops.yml
source_heading: FinOps Profile
source_url: https://www.tmforum.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: TM Forum\nproviderId: tm-forum\npublisherName: TM Forum\nserviceCategory: Industry Standards Body\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Telco\n  - Telecommunications\n  - Open APIs\n  - Standards\n  - FinOps\n  - FOCUS\ndescription: 'TM Forum is a not-for-profit industry association whose direct customer billing surface\n  is association membership rather than API consumption. There is no FOCUS-aligned per-request meter at\n  the TM Forum level; FinOps for \"TMF APIs\" applies to the operator that implements them.'\nsources:\n  - https://www.tmforum.org/\nnotes: TM Forum membership pricing not retrievable (403).\
  \ FOCUS columns and meters here describe membership\n  billing only; per-request meters belong to the implementing CSP or vendor.\nbillingModel:\n  pricingCategory: Membership\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: TM Forum Membership\n  ServiceCategory: Industry Standards Body\n  ProviderName: TM Forum\n  PublisherName: TM Forum\n  InvoiceIssuerName: TM Forum\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: tm_forum_membership_year\n    description: One year of TM Forum association membership at the contracted tier.\n    unit: year\n    aggregation: sum\n    dimensions:\n      - tier\n      - organization\nprinciples:\n  - name: Visibility\n    description: Track the TM Forum membership invoice as a fixed annual line; for downstream API costs,\n      visibility is the responsibility of the implementer that runs the TMF API.\n  - name: Allocation\n\
  \    description: Allocate the membership fee to the central architecture/standards function that uses\n      the conformance program; do not attempt to per-call attribute it.\n  - name: Optimization\n    description: Review the membership tier annually against actual use of conformance, working groups,\n      and event credits.\n  - name: Accountability\n    description: Designate the standards/architecture lead as the membership owner.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tm-forum/refs/heads/main/finops/tm-forum-finops.yml
sources:
- https://www.tmforum.org/
specification: FinOps Framework
tags:
- Telco
- Telecommunications
- Open APIs
- Standards
- FinOps
- FOCUS
---
