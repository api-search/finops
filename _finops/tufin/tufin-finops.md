---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tufin-securetrack-openapi.yml
  format: yaml
  label: Tufin SecureTrack API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tufin/refs/heads/main/openapi/tufin-securetrack-openapi.yml
- filename: tufin-securechange-openapi.yml
  format: yaml
  label: Tufin SecureChange API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tufin/refs/heads/main/openapi/tufin-securechange-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Tufin sells enterprise network-security policy software via direct sales; no public pricing, metered usage API, or FOCUS-aligned billing export is published. FinOps surface is the contracted product-license line.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tufin Software Technologies
  ProviderName: Tufin
  PublisherName: Tufin Software Technologies
  ServiceCategory: Network Security Policy Management
  ServiceName: Tufin
layout: finops
meters:
- aggregation: sum
  description: Tufin product license / subscription line (SecureTrack+, SecureChange+, Tufin Enterprise, etc.).
  dimensions:
  - product
  name: product_license
  unit: month
name: Tufin Finops
provider_name: Tufin
provider_slug: tufin
publisher_name: Tufin Software Technologies
service_category: Network Security Policy Management
slug: tufin-finops
source_filename: tufin-finops.yml
source_heading: FinOps Profile
source_url: https://www.tufin.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tufin\nproviderId: tufin\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Network Security\n  - Firewall\n  - FinOps\n  - FOCUS\ndescription: Tufin sells enterprise network-security policy software via direct sales; no public pricing,\n  metered usage API, or FOCUS-aligned billing export is published. FinOps surface is the contracted product-license\n  line.\nsources:\n  - https://www.tufin.com/\nnotes: No public pricing or usage telemetry. Trimmed to Contact Sales shape.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tufin Software Technologies\nserviceCategory: Network Security Policy Management\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency:\
  \ Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Tufin\n  ServiceCategory: Network Security Policy Management\n  ProviderName: Tufin\n  PublisherName: Tufin Software Technologies\n  InvoiceIssuerName: Tufin Software Technologies\n  BillingCurrency: USD\nmeters:\n  - name: product_license\n    description: Tufin product license / subscription line (SecureTrack+, SecureChange+, Tufin Enterprise,\n      etc.).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Visibility is limited to the contracted license invoice; usage telemetry stays inside\n      the customer-managed Tufin deployment and is not exposed as a public cost API.\n  - name: Allocation\n    description: Allocate Tufin spend to the network-security / SecOps function that owns firewall and\n      policy automation; sub-allocate by product (SecureTrack vs SecureChange vs AKIPS) where multiple\n      lines\
  \ are licensed.\n  - name: Optimization\n    description: Optimization happens at renewal — review the active product mix against actual policy\n      and change-automation usage, and decide whether modules like AKIPS or TOS Discovery are pulling\n      their weight before resigning.\n  - name: Accountability\n    description: A SecOps / network engineering owner manages the Tufin relationship and renewal; finance\n      approves the annual contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tufin/refs/heads/main/finops/tufin-finops.yml
sources:
- https://www.tufin.com/
specification: FinOps Framework
tags:
- Network Security
- Firewall
- FinOps
- FOCUS
---
