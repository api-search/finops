---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: calendly-scheduling-api-openapi.yml
  format: yaml
  label: Calendly Scheduling API
  slug: scheduling-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/calendly/refs/heads/main/openapi/calendly-scheduling-api-openapi.yml
- filename: calendly-webhook-api-asyncapi.yml
  format: yaml
  label: Calendly Webhook API
  slug: webhook-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/calendly/refs/heads/main/asyncapi/calendly-webhook-api-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Calendly: per-seat SaaS subscription priced monthly or annually, with an enterprise floor of $15,000/year. The cost shape is dominated by seat count; API and webhook usage are not separately metered against the customer.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Calendly, LLC
  PricingCategory: Subscription
  PricingUnit: seat
  ProviderName: Calendly
  PublisherName: Calendly, LLC
  ServiceCategory: Productivity / Scheduling
  ServiceName: Calendly
layout: finops
meters:
- aggregation: max
  description: Number of paid seats on the account in a billing month.
  dimensions:
  - plan
  - billing_term
  name: seats
  unit: seat
- aggregation: sum
  description: The recurring monthly or annual fee for the chosen plan tier.
  dimensions:
  - plan
  - billing_term
  name: plan_subscription
  unit: month
- aggregation: sum
  description: Annual contract floor for the Enterprise plan ($15,000/year baseline).
  dimensions:
  - contract_id
  name: enterprise_minimum
  unit: year
- aggregation: sum
  description: SSO/SAML add-on (priced separately on Standard and Teams; included in Enterprise).
  dimensions:
  - plan
  name: addon_sso_saml
  unit: month
- aggregation: sum
  description: Volume of v2 Scheduling API calls. Not directly billed but tracked for capacity and rate-limit observability.
  dimensions:
  - endpoint
  - oauth_app
  name: api_requests
  unit: request
- aggregation: sum
  description: Outbound webhook POSTs. Not directly billed but tracked for delivery-success accounting.
  dimensions:
  - subscription
  - event_type
  name: webhook_deliveries
  unit: event
name: Calendly Finops
provider_name: Calendly
provider_slug: calendly
publisher_name: Calendly, LLC
service_category: Productivity / Scheduling SaaS
slug: calendly-finops
source_filename: calendly-finops.yml
source_heading: FinOps Profile
source_url: https://calendly.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Calendly\nproviderId: calendly\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Scheduling\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Calendly: per-seat SaaS subscription priced monthly or annually,\n  with an enterprise floor of $15,000/year. The cost shape is dominated by seat count; API and webhook\n  usage are not separately metered against the customer.'\nsources:\n  - https://calendly.com/pricing\n  - https://developer.calendly.com/api-docs\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Calendly, LLC\nserviceCategory: Productivity / Scheduling SaaS\nbillingModel:\n\
  \  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Calendly\n  ServiceCategory: Productivity / Scheduling\n  ProviderName: Calendly\n  PublisherName: Calendly, LLC\n  InvoiceIssuerName: Calendly, LLC\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  PricingUnit: seat\n  ChargeCategory: Purchase\nmeters:\n  - name: seats\n    description: Number of paid seats on the account in a billing month.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n      - billing_term\n  - name: plan_subscription\n    description: The recurring monthly or annual fee for the chosen plan tier.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_term\n  - name: enterprise_minimum\n    description: Annual contract floor for the Enterprise plan ($15,000/year baseline).\n    unit: year\n  \
  \  aggregation: sum\n    dimensions:\n      - contract_id\n  - name: addon_sso_saml\n    description: SSO/SAML add-on (priced separately on Standard and Teams; included in Enterprise).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: api_requests\n    description: Volume of v2 Scheduling API calls. Not directly billed but tracked for capacity and rate-limit\n      observability.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - oauth_app\n  - name: webhook_deliveries\n    description: Outbound webhook POSTs. Not directly billed but tracked for delivery-success accounting.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - subscription\n      - event_type\nprinciples:\n  - name: Visibility\n    description: Use the Calendly admin billing page and the Organization API to see active seat counts,\n      plan tier, and renewal date. Pull invoices from the customer billing portal monthly.\n  - name: Allocation\n\
  \    description: Allocate seats by department or cost-center using Calendly groups; tag OAuth applications\n      to product teams so API-driven scheduling can be attributed back to the consuming product.\n  - name: Optimization\n    description: Reclaim inactive seats before each renewal; right-size between Standard and Teams based\n      on whether Salesforce routing and round-robin events are actually used; negotiate Enterprise floor\n      only when seat count warrants it (typically 75+ seats at Teams pricing).\n  - name: Accountability\n    description: Designate a workspace owner per organization, route renewal alerts to procurement 60+\n      days ahead of the annual term, and review seat utilization quarterly with department leads.\nmaintainers:\n  - FN: API Evangelist\n    url: http://apievangelist.com\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/calendly/refs/heads/main/finops/calendly-finops.yml
sources:
- https://calendly.com/pricing
- https://developer.calendly.com/api-docs
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Scheduling
- SaaS
- FinOps
- FOCUS
---
