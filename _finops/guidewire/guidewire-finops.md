---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: guidewire-policycenter-openapi.yml
  format: yaml
  label: Guidewire PolicyCenter API
  slug: guidewire-policycenter-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/guidewire/refs/heads/main/openapi/guidewire-policycenter-openapi.yml
- filename: guidewire-claimcenter-openapi.yml
  format: yaml
  label: Guidewire ClaimCenter API
  slug: guidewire-claimcenter-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/guidewire/refs/heads/main/openapi/guidewire-claimcenter-openapi.yml
- filename: guidewire-integration-gateway-asyncapi.yml
  format: yaml
  label: Guidewire Integration Gateway API
  slug: guidewire-integration-gateway-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/guidewire/refs/heads/main/asyncapi/guidewire-integration-gateway-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for Guidewire InsuranceSuite Cloud: enterprise subscription bundled with Guidewire Cloud, no public pricing. Meters here describe likely invoice-line shapes (subscription seats, transaction volume, environment count) for a P&C carrier consuming Guidewire APIs.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Guidewire Software, Inc.
  PricingCategory: Subscription
  PricingUnit: subscription
  ProviderName: Guidewire
  PublisherName: Guidewire Software, Inc.
  ServiceCategory: Insurance Platform / SaaS
  ServiceName: Guidewire InsuranceSuite Cloud
layout: finops
meters:
- aggregation: sum
  description: Annual Guidewire Cloud InsuranceSuite subscription line
  dimensions:
  - environment
  - line_of_business
  name: insurancesuite_subscription
  unit: subscription-year
- aggregation: sum
  description: Inferred transaction volume across PolicyCenter / ClaimCenter / BillingCenter APIs (capacity allocation meter; see contract for billable thresholds)
  dimensions:
  - api
  - environment
  name: api_transactions
  unit: transaction
- aggregation: sum
  description: Messages flowing through the Integration Gateway (used for capacity allocation)
  dimensions:
  - integration
  - environment
  name: integration_gateway_messages
  unit: message
name: Guidewire Finops
provider_name: Guidewire
provider_slug: guidewire
publisher_name: Guidewire Software, Inc.
service_category: Insurance Platform / SaaS
slug: guidewire-finops
source_filename: guidewire-finops.yml
source_heading: FinOps Profile
source_url: https://www.guidewire.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: guidewire\nproviderId: guidewire\npublisherName: Guidewire Software, Inc.\nserviceCategory: Insurance Platform / SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - P&C\n  - Policy\n  - Claims\n  - Billing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Guidewire InsuranceSuite Cloud: enterprise\n  subscription bundled with Guidewire Cloud, no public pricing. Meters here describe likely\n  invoice-line shapes (subscription seats, transaction volume, environment count) for a P&C carrier\n  consuming Guidewire APIs.'\nnotes: Pricing model is not publicly disclosed;\
  \ meters are inferred from Guidewire Cloud public\n  marketing and typical enterprise SaaS billing shapes. Reconcile against the customer's MSA.\nsources:\n  - https://www.guidewire.com/products\n  - https://www.guidewire.com/developers\nprinciples:\n  - name: Visibility\n    description: Use the Guidewire Cloud Console usage views and integration logs to track per-API\n      call volume against contract entitlements.\n  - name: Allocation\n    description: Tag InsuranceSuite environments (Dev / QA / Prod / DR) and consuming applications\n      so spend can be split across business lines (Personal / Commercial / Specialty).\n  - name: Optimization\n    description: Right-size non-production Guidewire environments; consolidate downstream\n      integrations through the Integration Gateway to reduce per-environment overhead.\n  - name: Accountability\n    description: Designate a Guidewire program owner; review subscription utilization quarterly\n      against the contractual ramp.\ndomains:\n\
  \  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName:\
  \ Guidewire InsuranceSuite Cloud\n  ServiceCategory: Insurance Platform / SaaS\n  ProviderName: Guidewire\n  PublisherName: Guidewire Software, Inc.\n  InvoiceIssuerName: Guidewire Software, Inc.\n  PricingCategory: Subscription\n  PricingUnit: subscription\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: insurancesuite_subscription\n    description: Annual Guidewire Cloud InsuranceSuite subscription line\n    unit: subscription-year\n    aggregation: sum\n    dimensions:\n      - environment\n      - line_of_business\n  - name: api_transactions\n    description: Inferred transaction volume across PolicyCenter / ClaimCenter / BillingCenter\n      APIs (capacity allocation meter; see contract for billable thresholds)\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n  - name: integration_gateway_messages\n    description: Messages flowing through the Integration Gateway (used for capacity allocation)\n    unit: message\n\
  \    aggregation: sum\n    dimensions:\n      - integration\n      - environment\napis:\n  - name: Guidewire PolicyCenter API\n    baseURL: https://api.guidewire.com\n    tags:\n      - Insurance\n      - P&C\n      - Policy\n      - Underwriting\n    serviceName: Guidewire PolicyCenter API\n    serviceCategory: API\n  - name: Guidewire ClaimCenter API\n    baseURL: https://api.guidewire.com\n    tags:\n      - Claims\n      - Insurance\n      - Loss Adjustment\n      - P&C\n    serviceName: Guidewire ClaimCenter API\n    serviceCategory: API\n  - name: Guidewire BillingCenter API\n    baseURL: https://api.guidewire.com\n    tags:\n      - Billing\n      - Insurance\n      - P&C\n      - Payments\n    serviceName: Guidewire BillingCenter API\n    serviceCategory: API\n  - name: Guidewire Integration Gateway API\n    baseURL: https://api.guidewire.com\n    tags:\n      - Insurance\n      - Integration\n      - Middleware\n      - P&C\n    serviceName: Guidewire Integration Gateway API\n\
  \    serviceCategory: API\nunitEconomics:\n  - name: Cost per Policy In-Force\n    metric: billed_cost / policies_in_force\n    target: TBD\n  - name: Cost per Claim Processed\n    metric: billed_cost / claims_processed\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/guidewire/refs/heads/main/finops/guidewire-finops.yml
sources:
- https://www.guidewire.com/products
- https://www.guidewire.com/developers
specification: FinOps Framework
tags:
- Insurance
- P&C
- Policy
- Claims
- Billing
- FinOps
- Cost Management
- FOCUS
---
