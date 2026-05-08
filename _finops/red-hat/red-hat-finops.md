---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi
  format: yaml
  label: Red Hat OpenShift API
  slug: ''
  spec_type: OpenAPI
  url: https://api.openshift.com/api/clusters_mgmt/v1/openapi
- filename: openapi
  format: yaml
  label: Red Hat OpenShift Cluster Manager API
  slug: ''
  spec_type: OpenAPI
  url: https://api.openshift.com/api/clusters_mgmt/v1/openapi
- filename: red-hat-ansible-automation-platform-openapi.yml
  format: yaml
  label: Red Hat Ansible Automation Platform API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/openapi/red-hat-ansible-automation-platform-openapi.yml
- filename: discovery
  format: yaml
  label: Red Hat Quay API
  slug: ''
  spec_type: OpenAPI
  url: https://quay.io/api/v1/discovery
- filename: red-hat-insights-openapi.yml
  format: yaml
  label: Red Hat Insights API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/openapi/red-hat-insights-openapi.yml
- filename: red-hat-satellite-openapi.yml
  format: yaml
  label: Red Hat Satellite API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/openapi/red-hat-satellite-openapi.yml
- filename: red-hat-keycloak-admin-openapi.yml
  format: yaml
  label: Red Hat Build of Keycloak Admin REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/openapi/red-hat-keycloak-admin-openapi.yml
- filename: red-hat-kafka-bridge-asyncapi.yml
  format: yaml
  label: Red Hat Streams for Apache Kafka Bridge API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/asyncapi/red-hat-kafka-bridge-asyncapi.yml
- filename: red-hat-notifications-webhooks-asyncapi.yml
  format: yaml
  label: Red Hat Notifications API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/asyncapi/red-hat-notifications-webhooks-asyncapi.yml
- filename: openapi
  format: yaml
  label: Red Hat Assisted Installer API
  slug: ''
  spec_type: OpenAPI
  url: https://api.openshift.com/api/assisted-install/v2/openapi
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps framing for the Red Hat umbrella subscription business. The fully reconciled meter list lives at the product-repo level (RHEL, OpenShift, Satellite, 3scale).
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Red Hat, Inc.
  ProviderName: Red Hat
  PublisherName: Red Hat, Inc.
  ServiceCategory: Enterprise Software Subscription
  ServiceName: Red Hat
layout: finops
meters:
- aggregation: sum
  description: Annual or multi-year subscription line per Red Hat product SKU
  dimensions:
  - product_sku
  - support_level
  - term_length
  name: subscription_term
  unit: contract
name: Red Hat Finops
provider_name: Red Hat
provider_slug: red-hat
publisher_name: Red Hat, Inc.
service_category: Enterprise Software Subscription
slug: red-hat-finops
source_filename: red-hat-finops.yml
source_heading: FinOps Profile
source_url: https://www.redhat.com/en/about/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat\nproviderId: red-hat\npublisherName: Red Hat, Inc.\nserviceCategory: Enterprise Software Subscription\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Enterprise Software\n  - Subscription\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps framing for the Red Hat umbrella subscription business. The\n  fully reconciled meter list lives at the product-repo level (RHEL, OpenShift, Satellite, 3scale).\nsources:\n  - https://www.redhat.com/en/about/pricing\nnotes: Umbrella red-hat artifact captures only the cross-product subscription shape; per-product\n  meters (RHEL socket-pair, OpenShift core-hour, Satellite\
  \ managed-host, 3scale call) belong in\n  the per-product repos.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Red Hat\n  ServiceCategory: Enterprise Software Subscription\n  ProviderName: Red Hat\n  PublisherName: Red Hat, Inc.\n  InvoiceIssuerName: Red Hat, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_term\n    description: Annual or multi-year subscription line per Red Hat product SKU\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - product_sku\n      - support_level\n      - term_length\nprinciples:\n  - name: Visibility\n    description: Use the Red Hat Customer Portal subscription views and Subscription Management\n      service to inventory active SKUs and entitlement consumption across the estate.\n  - name: Allocation\n    description: Tag subscriptions to consuming business units via the Customer Portal account\n      structure\
  \ or via internal CMDB linkage; entitlements can be partitioned by environment.\n  - name: Optimization\n    description: Consolidate to multi-year terms for discount, right-size between Standard and\n      Premium support, and align the Red Hat product mix at renewal.\n  - name: Accountability\n    description: Procurement holds the Red Hat master agreement; platform engineering owns\n      consumption against the entitlements.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat/refs/heads/main/finops/red-hat-finops.yml
sources:
- https://www.redhat.com/en/about/pricing
specification: FinOps Framework
tags:
- Enterprise Software
- Subscription
- FinOps
- FOCUS
---
