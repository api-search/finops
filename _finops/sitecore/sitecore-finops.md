---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sitecore-xm-cloud-rest-api-openapi.yml
  format: yaml
  label: Sitecore XM Cloud REST API
  slug: xm-cloud-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-xm-cloud-rest-api-openapi.yml
- filename: sitecore-cdp-rest-api-openapi.yml
  format: yaml
  label: Sitecore CDP REST API
  slug: cdp-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-cdp-rest-api-openapi.yml
- filename: sitecore-cdp-stream-api-asyncapi.yml
  format: yaml
  label: Sitecore CDP Stream API
  slug: cdp-stream-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/asyncapi/sitecore-cdp-stream-api-asyncapi.yml
- filename: sitecore-personalize-rest-api-openapi.yml
  format: yaml
  label: Sitecore Personalize REST API
  slug: personalize-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-personalize-rest-api-openapi.yml
- filename: sitecore-content-hub-rest-api-openapi.yml
  format: yaml
  label: Sitecore Content Hub REST API
  slug: content-hub-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-content-hub-rest-api-openapi.yml
- filename: sitecore-ordercloud-api-openapi.yml
  format: yaml
  label: Sitecore OrderCloud API
  slug: ordercloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-ordercloud-api-openapi.yml
- filename: sitecore-discover-api-openapi.yml
  format: yaml
  label: Sitecore Discover API
  slug: discover-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/openapi/sitecore-discover-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Contact Sales
description: 'FOCUS-aligned FinOps placeholder for Sitecore: contact-sales-only pricing means meters and unit prices are defined per signed agreement rather than from a public catalog.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sitecore Corporation A/S
  ProviderName: Sitecore
  PublisherName: Sitecore Corporation A/S
  ServiceCategory: Digital Experience Platform
  ServiceName: Sitecore
layout: finops
meters:
- aggregation: sum
  description: Annual contracted subscription fee per Sitecore product on the order form.
  dimensions:
  - product
  name: contracted_subscription
  unit: varies
- aggregation: max
  description: Sitecore Managed Cloud capacity (environments, regions) negotiated on the order form.
  dimensions:
  - product
  - region
  name: managed_cloud_capacity
  unit: varies
- aggregation: sum
  description: OrderCloud commerce transactions; negotiated as contract volume.
  dimensions:
  - environment
  name: ordercloud_transactions
  unit: transaction
name: Sitecore Finops
provider_name: sitecore
provider_slug: sitecore
publisher_name: Sitecore Corporation A/S
service_category: Digital Experience Platform
slug: sitecore-finops
source_filename: sitecore-finops.yml
source_heading: FinOps Profile
source_url: https://www.sitecore.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: sitecore\nproviderId: sitecore\npublisherName: Sitecore Corporation A/S\nserviceCategory: Digital Experience Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Content Management\n  - Digital Experience\n  - DXP\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Sitecore: contact-sales-only pricing means meters\n  and unit prices are defined per signed agreement rather than from a public catalog.'\nsources:\n  - https://www.sitecore.com/products\nnotes: |\n  No public pricing or invoice-line catalog is published. Meters below are stubs based on the\n  product portfolio; reconcile against\
  \ the customer's signed Sitecore order form for authoritative\n  billable units.\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Sitecore\n  ServiceCategory: Digital Experience Platform\n  ProviderName: Sitecore\n  PublisherName: Sitecore Corporation A/S\n  InvoiceIssuerName: Sitecore Corporation A/S\n  BillingCurrency: USD\nmeters:\n  - name: contracted_subscription\n    description: Annual contracted subscription fee per Sitecore product on the order form.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\n  - name: managed_cloud_capacity\n    description: Sitecore Managed Cloud capacity (environments, regions) negotiated on the order form.\n    unit: varies\n    aggregation: max\n    dimensions:\n      - product\n      - region\n  - name: ordercloud_transactions\n    description: OrderCloud commerce transactions; negotiated as\
  \ contract volume.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - environment\nprinciples:\n  - name: Visibility\n    description: Pull usage telemetry from each Sitecore product's admin (XM Cloud Portal, OrderCloud\n      Portal, CDP / Personalize dashboards) since there is no unified consumption export.\n  - name: Allocation\n    description: Allocate Sitecore spend per product / per brand, matching the order form line items\n      to the consuming digital property or business unit.\n  - name: Optimization\n    description: Optimization is contractual rather than dynamic — negotiate environment counts,\n      managed-cloud regions, and AI agent usage at renewal based on observed activity.\n  - name: Accountability\n    description: Digital experience program owner reconciles monthly product telemetry against the\n      annual contract and signs off on renewal scope.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sitecore/refs/heads/main/finops/sitecore-finops.yml
sources:
- https://www.sitecore.com/products
specification: FinOps Framework
tags:
- Content Management
- Digital Experience
- DXP
- FinOps
- FOCUS
---
