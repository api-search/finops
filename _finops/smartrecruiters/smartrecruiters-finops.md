---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: smartrecruiters-posting-openapi.yml
  format: yaml
  label: SmartRecruiters Posting API
  slug: posting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/smartrecruiters/refs/heads/main/openapi/smartrecruiters-posting-openapi.yml
- filename: smartrecruiters-jobs-openapi.yml
  format: yaml
  label: SmartRecruiters Job API
  slug: job-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/smartrecruiters/refs/heads/main/openapi/smartrecruiters-jobs-openapi.yml
- filename: smartrecruiters-candidates-openapi.yml
  format: yaml
  label: SmartRecruiters Candidate API
  slug: candidate-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/smartrecruiters/refs/heads/main/openapi/smartrecruiters-candidates-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for SmartRecruiters: tiered annual subscription with Essential starting at USD 14,995; higher tiers contact-sales. Plan caps cover SMS messaging volume, job distribution capacity, and AI screening usage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: SmartRecruiters, Inc.
  ProviderName: SmartRecruiters
  PublisherName: SmartRecruiters, Inc.
  ServiceCategory: Talent Acquisition / ATS
  ServiceName: SmartRecruiters
layout: finops
meters:
- aggregation: sum
  description: Annual subscription fee for the selected plan tier (Essential, Professional, High Volume, Complete).
  dimensions:
  - plan
  name: subscription_year
  unit: year
- aggregation: sum
  description: SMS messages sent through SmartRecruiters; volume cap varies by tier.
  dimensions:
  - plan
  - country
  name: sms_messages
  unit: varies
- aggregation: sum
  description: Job-board distribution events; capacity varies by tier.
  dimensions:
  - plan
  - job_board
  name: job_distributions
  unit: varies
- aggregation: sum
  description: AI candidate-screening invocations (High Volume and above).
  dimensions:
  - plan
  name: ai_screenings
  unit: varies
- aggregation: sum
  description: Public API calls subject to the documented per-credential request-rate and concurrency caps.
  dimensions:
  - credential
  - endpoint_class
  name: api_calls
  unit: request
name: Smartrecruiters Finops
provider_name: SmartRecruiters
provider_slug: smartrecruiters
publisher_name: SmartRecruiters, Inc.
service_category: Talent Acquisition / ATS
slug: smartrecruiters-finops
source_filename: smartrecruiters-finops.yml
source_heading: FinOps Profile
source_url: https://www.smartrecruiters.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SmartRecruiters\nproviderId: smartrecruiters\npublisherName: SmartRecruiters, Inc.\nserviceCategory: Talent Acquisition / ATS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Human Resources\n  - Recruiting\n  - Applicant Tracking\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for SmartRecruiters: tiered annual subscription with Essential\n  starting at USD 14,995; higher tiers contact-sales. Plan caps cover SMS messaging volume, job\n  distribution capacity, and AI screening usage.'\nsources:\n  - https://www.smartrecruiters.com/pricing/\n  - https://developers.smartrecruiters.com/docs/rate-limiting\nbillingModel:\n\
  \  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SmartRecruiters\n  ServiceCategory: Talent Acquisition / ATS\n  ProviderName: SmartRecruiters\n  PublisherName: SmartRecruiters, Inc.\n  InvoiceIssuerName: SmartRecruiters, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_year\n    description: Annual subscription fee for the selected plan tier (Essential, Professional, High\n      Volume, Complete).\n    unit: year\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: sms_messages\n    description: SMS messages sent through SmartRecruiters; volume cap varies by tier.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - plan\n      - country\n  - name: job_distributions\n    description: Job-board distribution events; capacity varies by tier.\n    unit: varies\n    aggregation:\
  \ sum\n    dimensions:\n      - plan\n      - job_board\n  - name: ai_screenings\n    description: AI candidate-screening invocations (High Volume and above).\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: api_calls\n    description: Public API calls subject to the documented per-credential request-rate and\n      concurrency caps.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - credential\n      - endpoint_class\nprinciples:\n  - name: Visibility\n    description: Use SmartRecruiters reporting + Reporting API for hiring-funnel telemetry; track\n      X-RateLimit-Remaining and X-RateLimit-Concurrent-Remaining headers to spot integration cost\n      pressure points.\n  - name: Allocation\n    description: Allocate spend per hiring department / region using SmartRecruiters' org structure;\n      tag SMS and job-distribution charges by requisition owner.\n  - name: Optimization\n    description: Reduce job-distribution waste by deactivating\
  \ boards with low conversion; throttle\n      integrations against the documented 10 RPS / 8 concurrent caps to avoid retry storms; use the\n      Reporting API for bulk extracts rather than transactional endpoints.\n  - name: Accountability\n    description: Talent-acquisition platform owner reviews monthly tier utilization (SMS, jobs, AI\n      screenings, seats) and sponsors tier-upgrade or renewal decisions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/smartrecruiters/refs/heads/main/finops/smartrecruiters-finops.yml
sources:
- https://www.smartrecruiters.com/pricing/
- https://developers.smartrecruiters.com/docs/rate-limiting
specification: FinOps Framework
tags:
- Human Resources
- Recruiting
- Applicant Tracking
- FinOps
- FOCUS
---
