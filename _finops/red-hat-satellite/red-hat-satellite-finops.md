---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: v2.json
  format: json
  label: Red Hat Satellite REST API
  slug: ''
  spec_type: OpenAPI
  url: https://satellite.example.com/apidoc/v2.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for Red Hat Satellite. Pricing is contact-sales, typically sized by managed-host count; meters here reflect the assumed host-based subscription, not a fetched billing surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Red Hat, Inc.
  ProviderName: Red Hat
  PublisherName: Red Hat, Inc.
  ServiceCategory: System Management
  ServiceName: Red Hat Satellite
layout: finops
meters:
- aggregation: sum
  description: Annual Satellite subscription line per managed RHEL host
  dimensions:
  - support_level
  - host_type
  name: managed_host_subscription
  unit: host-year
name: Red Hat Satellite Finops
provider_name: Red Hat Satellite
provider_slug: red-hat-satellite
publisher_name: Red Hat, Inc.
service_category: System Management
slug: red-hat-satellite-finops
source_filename: red-hat-satellite-finops.yml
source_heading: FinOps Profile
source_url: https://www.redhat.com/en/technologies/management/satellite
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat Satellite\nproviderId: red-hat-satellite\npublisherName: Red Hat, Inc.\nserviceCategory: System Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - System Management\n  - Provisioning\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Red Hat Satellite. Pricing is contact-sales, typically\n  sized by managed-host count; meters here reflect the assumed host-based subscription, not a\n  fetched billing surface.\nsources:\n  - https://www.redhat.com/en/technologies/management/satellite\nnotes: No public Satellite price list; meter list reflects the typical managed-host subscription\n  shape\
  \ rather than a fetched billing API.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Red Hat Satellite\n  ServiceCategory: System Management\n  ProviderName: Red Hat\n  PublisherName: Red Hat, Inc.\n  InvoiceIssuerName: Red Hat, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: managed_host_subscription\n    description: Annual Satellite subscription line per managed RHEL host\n    unit: host-year\n    aggregation: sum\n    dimensions:\n      - support_level\n      - host_type\nprinciples:\n  - name: Visibility\n    description: Satellite itself is the inventory tool — use its host registration data to\n      reconcile entitlement counts against the active subscription.\n  - name: Allocation\n    description: Allocate Satellite subscription cost to the platform team that operates the\n      Satellite server; managed-host counts can be attributed to consuming business units\
  \ via\n      host group / organization metadata.\n  - name: Optimization\n    description: Reclaim entitlements from decommissioned hosts via Satellite's host-unregister\n      flow; consolidate Satellite organizations to reduce server footprint.\n  - name: Accountability\n    description: Platform / infrastructure operations owns the Satellite subscription; consuming\n      app teams own their managed-host counts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat-satellite/refs/heads/main/finops/red-hat-satellite-finops.yml
sources:
- https://www.redhat.com/en/technologies/management/satellite
specification: FinOps Framework
tags:
- System Management
- Provisioning
- FinOps
- FOCUS
---
