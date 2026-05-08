---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sitefinity-cms-content-api-openapi.yml
  format: yaml
  label: Sitefinity CMS Content API
  slug: content-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitefinity-cms/refs/heads/main/openapi/sitefinity-cms-content-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: 'FOCUS-aligned FinOps placeholder for Progress Sitefinity CMS: contact-sales licensing with no public unit prices; Progress invoices the annual license plus optional cloud / add-on lines.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Progress Software Corporation
  ProviderName: Progress
  PublisherName: Progress Software Corporation
  ServiceCategory: Digital Experience Platform
  ServiceName: Sitefinity CMS
layout: finops
meters:
- aggregation: sum
  description: Annual Sitefinity edition license fee (Standard / Professional / Enterprise).
  dimensions:
  - edition
  name: license_subscription
  unit: varies
- aggregation: max
  description: Sitefinity Cloud-managed deployment capacity charge.
  dimensions:
  - environment
  - region
  name: sitefinity_cloud_capacity
  unit: varies
- aggregation: sum
  description: Add-on subscriptions (Sitefinity Insight, Commerce) negotiated alongside the core license.
  dimensions:
  - addon
  name: addon_subscription
  unit: varies
name: Sitefinity Cms Finops
provider_name: Sitefinity CMS
provider_slug: sitefinity-cms
publisher_name: Progress Software Corporation
service_category: Digital Experience Platform
slug: sitefinity-cms-finops
source_filename: sitefinity-cms-finops.yml
source_heading: FinOps Profile
source_url: https://www.progress.com/sitefinity
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sitefinity CMS\nproviderId: sitefinity-cms\npublisherName: Progress Software Corporation\nserviceCategory: Digital Experience Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Content Management\n  - DXP\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Progress Sitefinity CMS: contact-sales licensing\n  with no public unit prices; Progress invoices the annual license plus optional cloud / add-on lines.'\nsources:\n  - https://www.progress.com/sitefinity\nnotes: |\n  Progress does not publish public Sitefinity prices; meters below describe the typical invoice-line\n  shape (license, cloud\
  \ capacity, add-ons) but unit prices are set per signed agreement.\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Sitefinity CMS\n  ServiceCategory: Digital Experience Platform\n  ProviderName: Progress\n  PublisherName: Progress Software Corporation\n  InvoiceIssuerName: Progress Software Corporation\n  BillingCurrency: USD\nmeters:\n  - name: license_subscription\n    description: Annual Sitefinity edition license fee (Standard / Professional / Enterprise).\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - edition\n  - name: sitefinity_cloud_capacity\n    description: Sitefinity Cloud-managed deployment capacity charge.\n    unit: varies\n    aggregation: max\n    dimensions:\n      - environment\n      - region\n  - name: addon_subscription\n    description: Add-on subscriptions (Sitefinity Insight, Commerce) negotiated alongside the core\n      license.\n\
  \    unit: varies\n    aggregation: sum\n    dimensions:\n      - addon\nprinciples:\n  - name: Visibility\n    description: Track environment counts, hosted-cloud capacity, and add-on activation against the\n      signed Progress agreement; no consumption-API export is offered.\n  - name: Allocation\n    description: Allocate per brand or per digital property by mapping each Sitefinity site to its\n      consuming business unit on the signed order form.\n  - name: Optimization\n    description: Renewal is the optimization lever — reconcile actual environment counts and add-on\n      usage before the annual renewal to negotiate scope.\n  - name: Accountability\n    description: CMS platform owner reconciles the annual invoice against actual deployed sites,\n      environments, and add-ons.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sitefinity-cms/refs/heads/main/finops/sitefinity-cms-finops.yml
sources:
- https://www.progress.com/sitefinity
specification: FinOps Framework
tags:
- Content Management
- DXP
- FinOps
- FOCUS
---
