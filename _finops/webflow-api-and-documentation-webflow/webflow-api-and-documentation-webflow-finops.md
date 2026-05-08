---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: webflow-data-api-openapi.yml
  format: yaml
  label: Webflow Data API
  slug: data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow-api-and-documentation-webflow/refs/heads/main/openapi/webflow-data-api-openapi.yml
- filename: webflow-sites-openapi.yml
  format: yaml
  label: Webflow Sites API
  slug: sites-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow-api-and-documentation-webflow/refs/heads/main/openapi/webflow-sites-openapi.yml
- filename: webflow-collections-openapi.yml
  format: yaml
  label: Webflow Collections API
  slug: collections-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow-api-and-documentation-webflow/refs/heads/main/openapi/webflow-collections-openapi.yml
- filename: webflow-items-openapi.yml
  format: yaml
  label: Webflow CMS Items API
  slug: items-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow-api-and-documentation-webflow/refs/heads/main/openapi/webflow-items-openapi.yml
- filename: webflow-webhooks-openapi.yml
  format: yaml
  label: Webflow Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow-api-and-documentation-webflow/refs/heads/main/openapi/webflow-webhooks-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Webflow's Data API and documentation surface. The API itself is bundled with the Site Plan and rate-limited rather than metered, so billable units are the Site, Workspace, and Ecommerce subscriptions plus the 2% Ecommerce Standard transaction fee. Cost optimization is driven by tier selection, not per-call usage.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Webflow, Inc.
  ProviderName: Webflow
  PublisherName: Webflow, Inc.
  ServiceCategory: Web Publishing / CMS
  ServiceName: Webflow API and Documentation
layout: finops
meters:
- aggregation: sum
  description: Site Plan subscription (Starter / Basic / CMS / Business / Enterprise) per hosted site; gates the API rate-limit tier.
  dimensions:
  - site
  - tier
  name: site_subscription
  unit: month
- aggregation: sum
  description: Workspace seat subscription (Starter / Core / Growth / Freelancer / Agency / Enterprise).
  dimensions:
  - workspace
  - tier
  name: workspace_seat
  unit: seat
- aggregation: sum
  description: Ecommerce Plan subscription (Standard / Plus / Advanced) per store.
  dimensions:
  - site
  - tier
  name: ecommerce_subscription
  unit: month
- aggregation: sum
  description: 2% transaction fee on Ecommerce Standard; 0% on Plus and Advanced.
  dimensions:
  - site
  - tier
  name: ecommerce_transaction_fee
  unit: transaction
name: Webflow Api And Documentation Webflow Finops
provider_name: Webflow API and Documentation
provider_slug: webflow-api-and-documentation-webflow
publisher_name: Webflow, Inc.
service_category: Web Publishing / CMS
slug: webflow-api-and-documentation-webflow-finops
source_filename: webflow-api-and-documentation-webflow-finops.yml
source_heading: FinOps Profile
source_url: https://webflow.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Webflow API and Documentation\nproviderId: webflow-api-and-documentation-webflow\npublisherName: Webflow, Inc.\nserviceCategory: Web Publishing / CMS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - CMS\n  - Content Management\n  - Ecommerce\n  - No-Code\n  - Publishing\n  - Web Development\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Webflow's Data API and documentation surface. The API itself is\n  bundled with the Site Plan and rate-limited rather than metered, so billable units are the Site,\n  Workspace, and Ecommerce subscriptions plus the 2% Ecommerce Standard transaction fee. Cost\n  optimization\
  \ is driven by tier selection, not per-call usage.\nsources:\n  - https://webflow.com/pricing\n  - https://developers.webflow.com/data/reference/rate-limits\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Webflow API and Documentation\n  ServiceCategory: Web Publishing / CMS\n  ProviderName: Webflow\n  PublisherName: Webflow, Inc.\n  InvoiceIssuerName: Webflow, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: site_subscription\n    description: Site Plan subscription (Starter / Basic / CMS / Business / Enterprise) per hosted\n      site; gates the API rate-limit tier.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - site\n      - tier\n  - name: workspace_seat\n    description: Workspace seat subscription (Starter / Core / Growth / Freelancer / Agency /\n      Enterprise).\n    unit: seat\n    aggregation: sum\n    dimensions:\n  \
  \    - workspace\n      - tier\n  - name: ecommerce_subscription\n    description: Ecommerce Plan subscription (Standard / Plus / Advanced) per store.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - site\n      - tier\n  - name: ecommerce_transaction_fee\n    description: 2% transaction fee on Ecommerce Standard; 0% on Plus and Advanced.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - site\n      - tier\nprinciples:\n  - name: Visibility\n    description: Workspace billing dashboard at webflow.com lists site / seat / ecommerce subscriptions;\n      per-site dashboards surface bandwidth and CMS-item counts that drive tier decisions.\n  - name: Allocation\n    description: Map workspaces to business units / agency clients, sites to brands / properties, and\n      seats to named users; the workspace invoice rolls these up.\n  - name: Optimization\n    description: Levers are (1) move stores from Ecommerce Standard to Plus when monthly GMV makes the\n\
  \      $74 vs $29 delta cheaper than the 2% fee; (2) consolidate idle workspaces; (3) drop Site Plans\n      from retired projects; (4) prefer webhooks over polling so a Basic site key (60 req/min) does not\n      force an upgrade to a higher-tier Site Plan for rate alone.\n  - name: Accountability\n    description: Workspace billing admin owns the invoice; engineering / design owners review per-site\n      bandwidth and API rate-limit headroom before launches.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/webflow-api-and-documentation-webflow/refs/heads/main/finops/webflow-api-and-documentation-webflow-finops.yml
sources:
- https://webflow.com/pricing
- https://developers.webflow.com/data/reference/rate-limits
specification: FinOps Framework
tags:
- CMS
- Content Management
- Ecommerce
- No-Code
- Publishing
- Web Development
- FinOps
- FOCUS
---
