---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Red Hat Subscription Management API
  slug: subscription-management-api
  spec_type: OpenAPI
  url: https://api.access.redhat.com/management/v1/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights API
  slug: insights-api
  spec_type: OpenAPI
  url: https://cloud.redhat.com/api/insights/v1/openapi.json
- filename: rhel-security-data-openapi.yml
  format: yaml
  label: Red Hat Security Data API
  slug: security-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rhel/refs/heads/main/openapi/rhel-security-data-openapi.yml
- filename: openapi.json
  format: json
  label: Red Hat Insights Compliance API
  slug: compliance-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/compliance/v2/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights Vulnerability API
  slug: vulnerability-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/vulnerability/v1/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights Patch API
  slug: patch-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/patch/v3/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights Host Inventory API
  slug: inventory-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/inventory/v1/openapi.json
- filename: openapi.json
  format: json
  label: Red Hat Insights Remediations API
  slug: remediations-api
  spec_type: OpenAPI
  url: https://console.redhat.com/api/remediations/v1/openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps shape for RHEL: per-entitlement annual subscriptions, optionally layered with cloud-marketplace consumption (AWS, Azure, GCP) for pay-as-you-go RHEL hosts. No-cost developer entitlements are excluded from billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Red Hat, Inc.
  ProviderName: Red Hat
  PublisherName: Red Hat, Inc.
  ServiceCategory: Operating System Subscription
  ServiceName: Red Hat Enterprise Linux
layout: finops
meters:
- aggregation: sum
  description: Active RHEL subscription entitlements (host, socket-pair, or virtual datacenter)
  dimensions:
  - sku
  - support_level
  - region
  name: rhel_entitlements
  unit: entitlement
- aggregation: sum
  description: Pay-as-you-go RHEL hours billed via cloud marketplace (AWS, Azure, GCP)
  dimensions:
  - cloud
  - instance_type
  - region
  name: rhel_marketplace_hours
  unit: instance-hour
- aggregation: count
  description: Premium-support incidents opened against entitled subscriptions
  dimensions:
  - severity
  name: support_incidents
  unit: incident
name: Rhel Finops
provider_name: Red Hat Enterprise Linux
provider_slug: rhel
publisher_name: Red Hat, Inc.
service_category: Operating System Subscription
slug: rhel-finops
source_filename: rhel-finops.yml
source_heading: FinOps Profile
source_url: https://www.redhat.com/en/store/linux-platforms
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat Enterprise Linux\nproviderId: rhel\npublisherName: Red Hat, Inc.\nserviceCategory: Operating System Subscription\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Red Hat\n  - RHEL\n  - Linux\n  - Subscription\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps shape for RHEL: per-entitlement annual subscriptions, optionally\n  layered with cloud-marketplace consumption (AWS, Azure, GCP) for pay-as-you-go RHEL hosts.\n  No-cost developer entitlements are excluded from billing.\nsources:\n  - https://www.redhat.com/en/store/linux-platforms\n  - https://developers.redhat.com/products/rhel/overview\n  -\
  \ https://console.redhat.com/\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Red Hat Enterprise Linux\n  ServiceCategory: Operating System Subscription\n  ProviderName: Red Hat\n  PublisherName: Red Hat, Inc.\n  InvoiceIssuerName: Red Hat, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: rhel_entitlements\n    description: Active RHEL subscription entitlements (host, socket-pair, or virtual datacenter)\n    unit: entitlement\n    aggregation: sum\n    dimensions:\n      - sku\n      - support_level\n      - region\n  - name: rhel_marketplace_hours\n    description: Pay-as-you-go RHEL hours billed via cloud marketplace (AWS, Azure, GCP)\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud\n      - instance_type\n      - region\n  - name: support_incidents\n    description: Premium-support\
  \ incidents opened against entitled subscriptions\n    unit: incident\n    aggregation: count\n    dimensions:\n      - severity\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Red Hat Hybrid Cloud Console (Subscription Manager, Subscription Watch) and the\n      cloud marketplace usage feeds to reconcile entitled vs consumed RHEL hosts.\n  - name: Allocation\n    description: >-\n      Tag RHEL hosts in Red Hat Insights and in the parent cloud invoice (AWS / Azure / GCP\n      tags) so spend can be attributed to the consuming team or product.\n  - name: Optimization\n    description: >-\n      Choose between fixed-term entitlements and pay-as-you-go marketplace hours based on\n      utilization; consolidate hosts onto Virtual Datacenter SKUs where guest density is\n      high; retire unused entitlements before renewal.\n  - name: Accountability\n    description: >-\n      Platform engineering owns RHEL entitlement budgets; use Subscription Watch alerts to\n    \
  \  flag over-deployment ahead of the annual renewal cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rhel/refs/heads/main/finops/rhel-finops.yml
sources:
- https://www.redhat.com/en/store/linux-platforms
- https://developers.redhat.com/products/rhel/overview
- https://console.redhat.com/
specification: FinOps Framework
tags:
- Red Hat
- RHEL
- Linux
- Subscription
- FinOps
- FOCUS
---
