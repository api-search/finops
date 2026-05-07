---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: red-hat-3scale-service-management-openapi.yml
  format: yaml
  label: Red Hat 3scale Service Management API
  slug: service-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-service-management-openapi.yml
- filename: red-hat-3scale-account-management-openapi.yml
  format: yaml
  label: Red Hat 3scale Account Management API
  slug: account-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-account-management-openapi.yml
- filename: red-hat-3scale-analytics-openapi.yml
  format: yaml
  label: Red Hat 3scale Analytics API
  slug: analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-analytics-openapi.yml
- filename: red-hat-3scale-billing-openapi.yml
  format: yaml
  label: Red Hat 3scale Billing API
  slug: billing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-billing-openapi.yml
- filename: red-hat-3scale-apicast-management-openapi.yml
  format: yaml
  label: Red Hat 3scale APIcast Management API
  slug: apicast-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-apicast-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shape for Red Hat 3scale. Pricing is contact-sales, so the meter list reflects subscription/term structure rather than usage-based billing.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Red Hat, Inc.
  ProviderName: Red Hat
  PublisherName: Red Hat, Inc.
  ServiceCategory: API Management
  ServiceName: Red Hat 3scale API Management
layout: finops
meters:
- aggregation: sum
  description: Annual 3scale subscription (sized by deployment scope and call volume)
  dimensions:
  - deployment_model
  - support_level
  - term_length
  name: subscription_term
  unit: contract
name: Red Hat 3Scale Finops
provider_name: Red Hat 3scale
provider_slug: red-hat-3scale
publisher_name: Red Hat, Inc.
service_category: API Management
slug: red-hat-3scale-finops
source_filename: red-hat-3scale-finops.yml
source_heading: FinOps Profile
source_url: https://www.redhat.com/en/technologies/jboss-middleware/3scale
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat 3scale\nproviderId: red-hat-3scale\npublisherName: Red Hat, Inc.\nserviceCategory: API Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - API Management\n  - Gateway\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Red Hat 3scale. Pricing is contact-sales, so the\n  meter list reflects subscription/term structure rather than usage-based billing.\nsources:\n  - https://www.redhat.com/en/technologies/jboss-middleware/3scale\nnotes: No public price list or usage-billing API; FOCUS columns reflect the assumed annual-subscription\n  shape, not a fetched billing surface.\nbillingModel:\n\
  \  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Red Hat 3scale API Management\n  ServiceCategory: API Management\n  ProviderName: Red Hat\n  PublisherName: Red Hat, Inc.\n  InvoiceIssuerName: Red Hat, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_term\n    description: Annual 3scale subscription (sized by deployment scope and call volume)\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - deployment_model\n      - support_level\n      - term_length\nprinciples:\n  - name: Visibility\n    description: 3scale's own analytics service exposes per-application and per-method call\n      counts that customers can use for internal showback against the Red Hat subscription cost.\n  - name: Allocation\n    description: Allocate the 3scale subscription to the platform team that operates the gateway;\n      use 3scale account/application metadata to attribute downstream\
  \ API spend to consumers.\n  - name: Optimization\n    description: Right-size deployment topology (single vs multi-tenant, OpenShift-native vs\n      hosted), consolidate API portfolios behind a shared 3scale instance, and renegotiate term\n      length at renewal.\n  - name: Accountability\n    description: Platform engineering owns the 3scale subscription; product API teams own their\n      consumer plan design.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/finops/red-hat-3scale-finops.yml
sources:
- https://www.redhat.com/en/technologies/jboss-middleware/3scale
specification: FinOps Framework
tags:
- API Management
- Gateway
- FinOps
- FOCUS
---
