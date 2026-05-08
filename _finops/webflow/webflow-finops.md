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
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-data-api-openapi.yml
- filename: webflow-meta-openapi.yml
  format: yaml
  label: Webflow Meta API
  slug: meta-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-meta-openapi.yml
- filename: webflow-sites-openapi.yml
  format: yaml
  label: Webflow Sites API
  slug: sites-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-sites-openapi.yml
- filename: webflow-pages-openapi.yml
  format: yaml
  label: Webflow Pages API
  slug: pages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-pages-openapi.yml
- filename: webflow-collections-openapi.yml
  format: yaml
  label: Webflow Collections API
  slug: collections-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-collections-openapi.yml
- filename: webflow-items-openapi.yml
  format: yaml
  label: Webflow CMS Items API
  slug: items-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-items-openapi.yml
- filename: webflow-components-openapi.yml
  format: yaml
  label: Webflow Components API
  slug: components-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-components-openapi.yml
- filename: webflow-assets-openapi.yml
  format: yaml
  label: Webflow Assets API
  slug: assets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-assets-openapi.yml
- filename: webflow-forms-openapi.yml
  format: yaml
  label: Webflow Forms API
  slug: forms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-forms-openapi.yml
- filename: webflow-products-openapi.yml
  format: yaml
  label: Webflow Products and SKUs API
  slug: products-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-products-openapi.yml
- filename: webflow-orders-openapi.yml
  format: yaml
  label: Webflow Orders API
  slug: orders-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-orders-openapi.yml
- filename: webflow-inventory-openapi.yml
  format: yaml
  label: Webflow Inventory API
  slug: inventory-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-inventory-openapi.yml
- filename: webflow-ecommerce-settings-openapi.yml
  format: yaml
  label: Webflow Ecommerce Settings API
  slug: ecommerce-settings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-ecommerce-settings-openapi.yml
- filename: webflow-webhooks-openapi.yml
  format: yaml
  label: Webflow Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-webhooks-openapi.yml
- filename: webflow-custom-code-openapi.yml
  format: yaml
  label: Webflow Custom Code API
  slug: custom-code-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-custom-code-openapi.yml
- filename: webflow-comments-openapi.yml
  format: yaml
  label: Webflow Comments API
  slug: comments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/openapi/webflow-comments-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Webflow. Webflow bills as tiered subscriptions across three product surfaces — Site Plans (per-site), Workspace Plans (per-seat), and Ecommerce Plans (per-store + transaction-fee on Standard) — invoiced monthly or annually in USD. The Data API itself is bundled with the Site Plan and rate-limited rather than metered, so cost optimization centers on right-sizing Site / Workspace / Ecommerce tiers.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Webflow, Inc.
  ProviderName: Webflow
  PublisherName: Webflow, Inc.
  ServiceCategory: Web Publishing / CMS
  ServiceName: Webflow
layout: finops
meters:
- aggregation: sum
  description: Recurring Site Plan subscription (Starter / Basic / CMS / Business / Enterprise) per hosted site.
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
  description: 2% Webflow transaction fee on the Ecommerce Standard plan; 0% on Plus and Advanced.
  dimensions:
  - site
  - tier
  name: ecommerce_transaction_fee
  unit: transaction
- aggregation: sum
  description: Bandwidth consumed against the Site Plan's monthly bandwidth quota; overage handling is per the Site Plan tier.
  dimensions:
  - site
  - tier
  name: bandwidth_overage
  unit: GB
name: Webflow Finops
provider_name: Webflow
provider_slug: webflow
publisher_name: Webflow, Inc.
service_category: Web Publishing / CMS
slug: webflow-finops
source_filename: webflow-finops.yml
source_heading: FinOps Profile
source_url: https://webflow.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Webflow\nproviderId: webflow\npublisherName: Webflow, Inc.\nserviceCategory: Web Publishing / CMS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - CMS\n  - Ecommerce\n  - No-Code\n  - Web Development\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Webflow. Webflow bills as tiered subscriptions across three\n  product surfaces — Site Plans (per-site), Workspace Plans (per-seat), and Ecommerce Plans (per-store\n  + transaction-fee on Standard) — invoiced monthly or annually in USD. The Data API itself is bundled\n  with the Site Plan and rate-limited rather than metered, so cost optimization centers on right-sizing\n\
  \  Site / Workspace / Ecommerce tiers.\nsources:\n  - https://webflow.com/pricing\n  - https://developers.webflow.com/data/reference/rate-limits\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Webflow\n  ServiceCategory: Web Publishing / CMS\n  ProviderName: Webflow\n  PublisherName: Webflow, Inc.\n  InvoiceIssuerName: Webflow, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: site_subscription\n    description: Recurring Site Plan subscription (Starter / Basic / CMS / Business / Enterprise) per\n      hosted site.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - site\n      - tier\n  - name: workspace_seat\n    description: Workspace seat subscription (Starter / Core / Growth / Freelancer / Agency / Enterprise).\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - workspace\n      - tier\n  - name: ecommerce_subscription\n\
  \    description: Ecommerce Plan subscription (Standard / Plus / Advanced) per store.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - site\n      - tier\n  - name: ecommerce_transaction_fee\n    description: 2% Webflow transaction fee on the Ecommerce Standard plan; 0% on Plus and Advanced.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - site\n      - tier\n  - name: bandwidth_overage\n    description: Bandwidth consumed against the Site Plan's monthly bandwidth quota; overage handling\n      is per the Site Plan tier.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - site\n      - tier\nprinciples:\n  - name: Visibility\n    description: Cost visibility is via the Workspace billing dashboard at webflow.com — review the\n      site / seat / ecommerce subscriptions per workspace and the bandwidth meter on each site dashboard.\n  - name: Allocation\n    description: Allocate Webflow spend by workspace (one workspace per business unit /\
  \ agency client),\n      site (one per brand or property), and seat (named designer / developer). Workspace billing\n      consolidates all sites under a workspace into one invoice.\n  - name: Optimization\n    description: Cost levers are (1) move stores from Standard (2% fee) to Plus (0%) once monthly GMV\n      makes the $74 vs $29 delta worthwhile; (2) consolidate underused workspaces; (3) drop unused\n      Site Plans on staging projects; (4) keep API calls under the per-key per-minute limit to avoid\n      forcing an Enterprise upgrade for rate alone — use webhooks instead of polling.\n  - name: Accountability\n    description: Workspace owner / billing admin holds accountability; design / engineering owners\n      review site bandwidth, CMS-item counts, and API rate-limit alerts before adding new sites or\n      higher-traffic launches.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/webflow/refs/heads/main/finops/webflow-finops.yml
sources:
- https://webflow.com/pricing
- https://developers.webflow.com/data/reference/rate-limits
specification: FinOps Framework
tags:
- CMS
- Ecommerce
- No-Code
- Web Development
- FinOps
- FOCUS
---
