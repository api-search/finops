---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: v3
  format: yaml
  label: Fortify on Demand API
  slug: ''
  spec_type: OpenAPI
  url: https://api.ams.fortify.com/swagger/docs/v3
- filename: fortify-software-security-center-openapi.yml
  format: yaml
  label: Fortify Software Security Center API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fortify/refs/heads/main/openapi/fortify-software-security-center-openapi.yml
- filename: fortify-scancentral-dast-openapi.yml
  format: yaml
  label: Fortify ScanCentral DAST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fortify/refs/heads/main/openapi/fortify-scancentral-dast-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps mapping for Fortify (OpenText) — annual subscription application-security tooling billed per application (Fortify on Demand SaaS) or per developer seat / scan engine (self-hosted SCA + SSC + WebInspect).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Open Text Corporation
  ProviderName: Open Text Corporation
  PublisherName: Open Text Corporation
  ServiceCategory: Application Security
  ServiceName: Fortify (OpenText)
layout: finops
meters:
- aggregation: max
  description: Distinct applications under Fortify on Demand subscription
  dimensions:
  - product
  - business_unit
  name: applications_scanned
  unit: application-year
- aggregation: max
  description: Developer / contributor seats licensed for self-hosted Fortify
  dimensions:
  - product
  name: developer_seats
  unit: seat-year
- aggregation: max
  description: SCA / WebInspect / ScanCentral engine licenses
  dimensions:
  - engine_type
  name: scan_engines
  unit: engine-year
- aggregation: sum
  description: Static, dynamic, mobile, or SCA scans executed
  dimensions:
  - scan_type
  - application
  name: scans_executed
  unit: scan
- aggregation: sum
  description: LOC analyzed (used as a tier-sizing metric for some FoD agreements)
  dimensions:
  - language
  name: lines_of_code_scanned
  unit: line
name: Fortify Finops
provider_name: Fortify
provider_slug: fortify
publisher_name: Open Text Corporation
service_category: Application Security
slug: fortify-finops
source_filename: fortify-finops.yml
source_heading: FinOps Profile
source_url: https://www.opentext.com/products/fortify-on-demand
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Fortify\nproviderId: fortify\npublisherName: Open Text Corporation\nserviceCategory: Application Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Security\n  - DevSecOps\n  - SAST\n  - DAST\n  - SCA\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps mapping for Fortify (OpenText) — annual subscription application-security tooling billed per application (Fortify on Demand SaaS) or per developer seat / scan engine (self-hosted SCA + SSC + WebInspect).\nnotes: No public price list. Meters reflect typical OpenText/Fortify invoice line items.\nsources:\n  - https://www.opentext.com/products/fortify-on-demand\n\
  \  - https://www.opentext.com/products/fortify\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Fortify (OpenText)\n  ServiceCategory: Application Security\n  ProviderName: Open Text Corporation\n  PublisherName: Open Text Corporation\n  InvoiceIssuerName: Open Text Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: applications_scanned\n    description: Distinct applications under Fortify on Demand subscription\n    unit: application-year\n    aggregation: max\n    dimensions:\n      - product\n      - business_unit\n  - name: developer_seats\n    description: Developer / contributor seats licensed for self-hosted Fortify\n    unit: seat-year\n    aggregation: max\n    dimensions:\n      - product\n  - name: scan_engines\n    description: SCA / WebInspect / ScanCentral engine\
  \ licenses\n    unit: engine-year\n    aggregation: max\n    dimensions:\n      - engine_type\n  - name: scans_executed\n    description: Static, dynamic, mobile, or SCA scans executed\n    unit: scan\n    aggregation: sum\n    dimensions:\n      - scan_type\n      - application\n  - name: lines_of_code_scanned\n    description: LOC analyzed (used as a tier-sizing metric for some FoD agreements)\n    unit: line\n    aggregation: sum\n    dimensions:\n      - language\nprinciples:\n  - name: Visibility\n    description: Pull Fortify on Demand and SSC reporting APIs into your data warehouse; track scans-per-application and scan-pass-rate to expose unused application licenses.\n  - name: Allocation\n    description: Tag applications in FoD/SSC with business-unit metadata so license consumption is allocable.\n  - name: Optimization\n    description: Right-size FoD application tier (LOC bands) annually based on actual codebase size; consolidate dormant applications; consider on-prem ScanCentral\
  \ for high-volume CI scanning where it is cheaper than per-app FoD subscriptions.\n  - name: Accountability\n    description: AppSec engineering owns the Fortify contract; finance reviews application count and scan utilization quarterly ahead of OpenText renewal.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fortify/refs/heads/main/finops/fortify-finops.yml
sources:
- https://www.opentext.com/products/fortify-on-demand
- https://www.opentext.com/products/fortify
specification: FinOps Framework
tags:
- Application Security
- DevSecOps
- SAST
- DAST
- SCA
- FinOps
- FOCUS
---
