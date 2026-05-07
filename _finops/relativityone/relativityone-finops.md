---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: relativityone-legal-hold-openapi.yml
  format: yaml
  label: Legal Hold API
  slug: legal-hold-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/relativityone/refs/heads/main/openapi/relativityone-legal-hold-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Contact Sales
description: FinOps shape for RelativityOne. Customers pay a tenant subscription plus matter-driven consumption (data ingested, processed, hosted, reviewed). Public per-unit prices are not published; the meters listed correspond to the categories Relativity invoices use, not to fabricated request-rate meters.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Relativity ODA LLC
  ProviderName: Relativity
  PublisherName: Relativity ODA LLC
  ServiceCategory: eDiscovery
  ServiceName: RelativityOne
layout: finops
meters:
- aggregation: sum
  dimensions:
  - matter
  - workspace
  name: data_hosted
  unit: GB-month
- aggregation: sum
  dimensions:
  - matter
  - workspace
  name: data_processed
  unit: GB
- aggregation: sum
  dimensions:
  - role
  name: review_users
  unit: seat
name: Relativityone Finops
provider_name: RelativityOne
provider_slug: relativityone
publisher_name: Relativity ODA LLC
service_category: eDiscovery
slug: relativityone-finops
source_filename: relativityone-finops.yml
source_heading: FinOps Profile
source_url: https://www.relativity.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: RelativityOne\nproviderId: relativityone\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - eDiscovery\n  - Legal\ndescription: FinOps shape for RelativityOne. Customers pay a tenant subscription plus matter-driven\n  consumption (data ingested, processed, hosted, reviewed). Public per-unit prices are not published;\n  the meters listed correspond to the categories Relativity invoices use, not to fabricated request-rate\n  meters.\nsources:\n  - https://www.relativity.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Relativity ODA LLC\nserviceCategory: eDiscovery\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: RelativityOne\n  ServiceCategory: eDiscovery\n  ProviderName: Relativity\n  PublisherName: Relativity ODA LLC\n  InvoiceIssuerName: Relativity ODA LLC\n  BillingCurrency: USD\nmeters:\n  - name: data_hosted\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - matter\n      - workspace\n  - name: data_processed\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - matter\n      - workspace\n  - name: review_users\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - role\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Relativity invoice and tenant usage reports, broken down by\n      workspace and matter; surface those reports to legal-ops and finance.\n  - name: Allocation\n    description: Allocate hosted / processed GB and reviewer seats to the matter and the legal team\n      that owns the matter; matter is\
  \ the primary cost-allocation key.\n  - name: Optimization\n    description: Optimization levers are matter lifecycle (close out completed matters, reduce hosted\n      volume), early case assessment, and use of analytics / aiR to cut review hours.\n  - name: Accountability\n    description: Owner is legal operations / litigation support, who manages the Relativity tenant and\n      assigns matter budgets to case teams.\nnotes: Subscription + matter-consumption model; meters reflect Relativity's invoice categories. Generic\n  per-request meters and FOCUS per-call columns removed.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/relativityone/refs/heads/main/finops/relativityone-finops.yml
sources:
- https://www.relativity.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- eDiscovery
- Legal
---
