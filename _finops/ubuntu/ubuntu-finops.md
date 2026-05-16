---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ubuntu-launchpad-openapi.yml
  format: yaml
  label: Launchpad API
  slug: launchpad-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ubuntu/refs/heads/main/openapi/ubuntu-launchpad-openapi.yml
- filename: ubuntu-snap-store-openapi.yml
  format: yaml
  label: Snap Store API
  slug: snap-store-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ubuntu/refs/heads/main/openapi/ubuntu-snap-store-openapi.yml
- filename: ubuntu-cve-openapi.yml
  format: yaml
  label: Ubuntu CVE API
  slug: ubuntu-cve-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ubuntu/refs/heads/main/openapi/ubuntu-cve-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Subscription (Per-Machine)
description: 'FOCUS-aligned FinOps for Ubuntu Pro: per-machine annual subscription with a free Personal/Community track, separate Workstation and Server tiers, and optional 24/7 support add-ons.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Canonical Ltd
  ProviderName: Ubuntu
  PublisherName: Canonical Ltd
  ServiceCategory: Operating System / Security Maintenance
  ServiceName: Ubuntu Pro
layout: finops
meters:
- aggregation: sum
  description: Annual Ubuntu Pro subscription per workstation
  dimensions:
  - support_tier
  name: workstation_subscription
  unit: machine
- aggregation: sum
  description: Annual Ubuntu Pro subscription per physical server (unlimited VMs per host)
  dimensions:
  - support_tier
  name: server_subscription
  unit: machine
- aggregation: sum
  description: 24/7 infrastructure or full-stack support uplift
  dimensions:
  - support_tier
  name: support_add_on
  unit: machine
name: Ubuntu Finops
provider_name: Ubuntu
provider_slug: ubuntu
publisher_name: Canonical Ltd
service_category: Operating System / Security Maintenance
slug: ubuntu-finops
source_filename: ubuntu-finops.yml
source_heading: FinOps Profile
source_url: https://ubuntu.com/pricing/pro
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ubuntu\nproviderId: ubuntu\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Linux\n  - Open Source\n  - Security\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Ubuntu Pro: per-machine annual subscription with a free Personal/Community\n  track, separate Workstation and Server tiers, and optional 24/7 support add-ons.'\nsources:\n  - https://ubuntu.com/pricing/pro\n  - https://ubuntu.com/pro/subscribe\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Canonical Ltd\nserviceCategory: Operating System / Security Maintenance\nbillingModel:\n  pricingCategory: Subscription (Per-Machine)\n\
  \  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Ubuntu Pro\n  ServiceCategory: Operating System / Security Maintenance\n  ProviderName: Ubuntu\n  PublisherName: Canonical Ltd\n  InvoiceIssuerName: Canonical Ltd\n  BillingCurrency: USD\nmeters:\n  - name: workstation_subscription\n    description: Annual Ubuntu Pro subscription per workstation\n    unit: machine\n    aggregation: sum\n    dimensions:\n      - support_tier\n  - name: server_subscription\n    description: Annual Ubuntu Pro subscription per physical server (unlimited VMs per host)\n    unit: machine\n    aggregation: sum\n    dimensions:\n      - support_tier\n  - name: support_add_on\n    description: 24/7 infrastructure or full-stack support uplift\n    unit: machine\n    aggregation: sum\n    dimensions:\n      - support_tier\nprinciples:\n  - name: Visibility\n    description: Track machines under Ubuntu Pro\
  \ via the Pro Contracts API and the Ubuntu Pro dashboard;\n      reconcile against Canonical's annual invoices.\n  - name: Allocation\n    description: Tag each pro-attached machine with team / environment so per-machine subscriptions can\n      be charged back to the workload owner.\n  - name: Optimization\n    description: Move dev / staging fleets to the free Personal track where eligible; consolidate VMs\n      onto Pro-licensed physical hosts to amortize the per-machine fee; right-size support tier (Base\n      vs Infra vs Full).\n  - name: Accountability\n    description: Platform / infrastructure owners review attached-machine count vs entitlement before\n      annual renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ubuntu/refs/heads/main/finops/ubuntu-finops.yml
sources:
- https://ubuntu.com/pricing/pro
- https://ubuntu.com/pro/subscribe
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Linux
- Open Source
- Security
- FinOps
- FOCUS
---
