---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: acquia-cloud-applications.yml
  format: yaml
  label: Acquia Cloud API
  slug: acquia-cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acquia/refs/heads/main/openapi/acquia-cloud-applications.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription
description: FOCUS-aligned FinOps scaffold for Acquia. Acquia's commercial model is enterprise subscription per product (Cloud Platform, Site Factory, DAM, PIM, CDP, Campaign Studio, Conversion Optimization, Search), sized by sites, environments, profiles, assets, or seats depending on the product.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Acquia, Inc.
  ProviderName: Acquia
  PublisherName: Acquia, Inc.
  ServiceCategory: Digital Experience Platform
  ServiceName: Acquia
layout: finops
meters:
- aggregation: max
  description: Acquia Cloud Platform application + environment subscription.
  dimensions:
  - application
  - environment_size
  - region
  name: cloud_environment
  unit: environment
- aggregation: max
  description: Site managed under Site Factory.
  dimensions:
  - site_factory_tenant
  name: managed_site
  unit: site
- aggregation: max
  description: Named DAM user (Widen) seat.
  dimensions:
  - role
  name: dam_user
  unit: seat
- aggregation: max
  description: Asset storage in Acquia DAM.
  dimensions:
  - tenant
  name: dam_storage
  unit: GB
- aggregation: max
  description: Active customer profile in Acquia CDP.
  dimensions:
  - source_system
  name: cdp_profile
  unit: profile
- aggregation: sum
  description: Behavioral event ingested into CDP.
  dimensions:
  - source_system
  - event_type
  name: cdp_event
  unit: event
- aggregation: max
  description: Active marketable contact in Campaign Studio.
  dimensions:
  - segment
  name: campaign_contact
  unit: contact
- aggregation: max
  description: Search index / core in Acquia Search.
  dimensions:
  - environment
  name: search_index
  unit: index
name: Acquia Finops
provider_name: Acquia
provider_slug: acquia
publisher_name: Acquia, Inc.
service_category: Digital Experience Platform
slug: acquia-finops
source_filename: acquia-finops.yml
source_heading: FinOps Profile
source_url: https://www.acquia.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Acquia\nproviderId: acquia\npublisherName: Acquia, Inc.\nserviceCategory: Digital Experience Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Content\n  - Experience\n  - Drupal\n  - DXP\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Acquia. Acquia's commercial model is enterprise subscription\n  per product (Cloud Platform, Site Factory, DAM, PIM, CDP, Campaign Studio, Conversion Optimization,\n  Search), sized by sites, environments, profiles, assets, or seats depending on the product.\nsources:\n  - https://www.acquia.com/products\n  - https://cloudapi-docs.acquia.com/\nnotes: Public\
  \ per-product prices are not published; meters describe the dimensions Acquia uses to size\n  contracts. Replace with the dollar amounts on the customer's order form when reconciling.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Acquia\n  ServiceCategory: Digital Experience Platform\n  ProviderName: Acquia\n  PublisherName: Acquia, Inc.\n  InvoiceIssuerName: Acquia, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: cloud_environment\n    description: Acquia Cloud Platform application + environment subscription.\n    unit: environment\n    aggregation: max\n    dimensions:\n      - application\n      - environment_size\n      - region\n  - name: managed_site\n    description: Site managed under Site Factory.\n    unit: site\n    aggregation: max\n    dimensions:\n      - site_factory_tenant\n  - name: dam_user\n    description:\
  \ Named DAM user (Widen) seat.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n  - name: dam_storage\n    description: Asset storage in Acquia DAM.\n    unit: GB\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: cdp_profile\n    description: Active customer profile in Acquia CDP.\n    unit: profile\n    aggregation: max\n    dimensions:\n      - source_system\n  - name: cdp_event\n    description: Behavioral event ingested into CDP.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - source_system\n      - event_type\n  - name: campaign_contact\n    description: Active marketable contact in Campaign Studio.\n    unit: contact\n    aggregation: max\n    dimensions:\n      - segment\n  - name: search_index\n    description: Search index / core in Acquia Search.\n    unit: index\n    aggregation: max\n    dimensions:\n      - environment\nprinciples:\n  - name: Visibility\n    description: Each Acquia product invoices on different dimensions;\
  \ pull environment, site, profile,\n      and seat counts from the Cloud API and the DAM / CDP admin consoles to build a unified usage view.\n  - name: Allocation\n    description: Allocate Cloud Platform and Site Factory cost to the owning brand / property; allocate\n      DAM, CDP, and Campaign Studio cost to marketing-ops cost centers.\n  - name: Optimization\n    description: Right-size Cloud environments (down-tier non-prod, schedule lower environments off-hours),\n      reclaim DAM / CDP seats from inactive users, archive cold assets out of DAM storage tiers.\n  - name: Accountability\n    description: Engineering platform leads own Cloud / Site Factory; marketing-ops leadership owns DAM,\n      CDP, Campaign Studio, and Conversion Optimization renewals.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/acquia/refs/heads/main/finops/acquia-finops.yml
sources:
- https://www.acquia.com/products
- https://cloudapi-docs.acquia.com/
specification: FinOps Framework
tags:
- Content
- Experience
- Drupal
- DXP
- FinOps
- FOCUS
---
