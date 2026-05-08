---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: availity-eligibility-openapi.yml
  format: yaml
  label: Availity Eligibility & Benefits API
  slug: availity-eligibility-benefits-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/openapi/availity-eligibility-openapi.yml
- filename: availity-claim-status-openapi.yml
  format: yaml
  label: Availity Claim Status API
  slug: availity-claims-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/openapi/availity-claim-status-openapi.yml
- filename: availity-claim-attachments-openapi.yml
  format: yaml
  label: Availity Claim Attachments API
  slug: availity-claim-attachments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/openapi/availity-claim-attachments-openapi.yml
- filename: availity-service-reviews-openapi.yml
  format: yaml
  label: Availity Service Reviews (Prior Authorization) API
  slug: availity-service-reviews-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/openapi/availity-service-reviews-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Subscription + Per-Transaction
description: 'FOCUS-aligned FinOps for Availity: two-sided market with payer-funded provider portal (zero cost to provider) plus per-transaction clearinghouse fees and subscription RCM/Pro tiers billed to trading partners.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Availity, LLC
  ProviderName: Availity
  PublisherName: Availity, LLC
  ServiceCategory: Healthcare Network / Clearinghouse
  ServiceName: Availity
layout: finops
meters:
- aggregation: sum
  dimensions:
  - transaction_set
  - payer
  - real_time_or_batch
  name: x12_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - payer
  name: eligibility_lookups
  unit: lookup
- aggregation: sum
  dimensions:
  - payer
  - line_of_business
  name: claim_submissions
  unit: claim
- aggregation: sum
  name: era_records
  unit: record
- aggregation: max
  name: essentials_pro_seats
  unit: seat
- aggregation: sum
  name: rcm_subscription
  unit: month
name: Availity Finops
provider_name: availity
provider_slug: availity
publisher_name: Availity, LLC
service_category: Healthcare Network / Clearinghouse
slug: availity-finops
source_filename: availity-finops.yml
source_heading: FinOps Profile
source_url: https://www.availity.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Availity\nproviderId: availity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Availity pricing is two-sided. Provider-side Essentials is free (paid by health plans). Trading\n  partner / clearinghouse and Essentials Pro are quote-based. This artifact models both sides.\ntags:\n  - FinOps\n  - FOCUS\n  - Healthcare\n  - HIPAA\n  - X12 EDI\n  - Clearinghouse\ndescription: 'FOCUS-aligned FinOps for Availity: two-sided market with payer-funded provider portal\n  (zero cost to provider) plus per-transaction clearinghouse fees and subscription RCM/Pro tiers\n  billed to trading partners.'\nsources:\n  - https://www.availity.com/\n  - https://www.availity.com/products\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Availity, LLC\nserviceCategory: Healthcare Network / Clearinghouse\nbillingModel:\n  pricingCategory: Subscription + Per-Transaction\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Availity\n  ServiceCategory: Healthcare Network / Clearinghouse\n  ProviderName: Availity\n  PublisherName: Availity, LLC\n  InvoiceIssuerName: Availity, LLC\n  BillingCurrency: USD\nmeters:\n  - name: x12_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - transaction_set\n      - payer\n      - real_time_or_batch\n  - name: eligibility_lookups\n    unit: lookup\n    aggregation: sum\n    dimensions:\n      - payer\n  - name: claim_submissions\n    unit: claim\n    aggregation: sum\n    dimensions:\n      - payer\n      - line_of_business\n  - name: era_records\n    unit: record\n    aggregation: sum\n  - name: essentials_pro_seats\n\
  \    unit: seat\n    aggregation: max\n  - name: rcm_subscription\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use the Availity reporting dashboards (Trading Partner reports, RCM dashboards) to\n      see transaction counts by payer and transaction set; reconcile against monthly invoices.\n  - name: Allocation\n    description: Allocate by line of business (medical vs dental vs vision), payer, and submitting\n      provider TIN; tag claims with internal cost-center / location codes.\n  - name: Optimization\n    description: Move from batch X12 to real-time eligibility for high-touch encounters; consolidate\n      vendor connections through Availity to drop redundant clearinghouse fees.\n  - name: Accountability\n    description: Revenue cycle director typically owns Availity spend; payer-relations team owns\n      configurations for participating health plans.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/availity/refs/heads/main/finops/availity-finops.yml
sources:
- https://www.availity.com/
- https://www.availity.com/products
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Healthcare
- HIPAA
- X12 EDI
- Clearinghouse
---
