---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage (overage)
description: FOCUS-aligned FinOps profile for SurveyMonkey. Billing is per-user-per-month on the team plans (Advantage/Premier) with annual response bundles, plus $0.15/response overage. Enterprise contracts are negotiated. SurveyMonkey Audience (paid panel) is metered separately.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: SurveyMonkey
  PricingUnit: user-month / response
  ProviderName: SurveyMonkey
  PublisherName: SurveyMonkey
  ServiceCategory: Surveys
  ServiceName: SurveyMonkey
layout: finops
meters:
- aggregation: max
  description: Active billable seats per plan tier.
  dimensions:
  - workgroup
  - tier
  name: seats
  unit: user-month
- aggregation: sum
  description: Survey responses counted against the annual bundle.
  dimensions:
  - workgroup
  - survey
  name: responses
  unit: response
- aggregation: sum
  description: Responses above the annual bundle billed at $0.15 each.
  dimensions:
  - workgroup
  name: response_overage
  unit: response
- aggregation: sum
  description: SurveyMonkey Audience paid-panel completes.
  dimensions:
  - workgroup
  - survey
  name: audience_panel
  unit: completion
name: Surveymonkey Finops
provider_name: SurveyMonkey
provider_slug: surveymonkey
publisher_name: SurveyMonkey
service_category: Surveys / Feedback
slug: surveymonkey-finops
source_filename: surveymonkey-finops.yml
source_heading: FinOps Profile
source_url: https://www.surveymonkey.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SurveyMonkey\nproviderId: surveymonkey\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Surveys\n- Market Research\n- Feedback\n- NPS\n- Forms\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for SurveyMonkey. Billing is per-user-per-month\n  on the team plans (Advantage/Premier) with annual response bundles, plus\n  $0.15/response overage. Enterprise contracts are negotiated. SurveyMonkey\n  Audience (paid panel) is metered separately.\nnotes: >-\n  Workgroups in Enterprise can be used to allocate cost by business unit;\n  billing is annual and invoiced in USD. Public-app daily 500K request quota\n  has no incremental cost as long as it stays within the API rate-limit\n  schedule.\nsources:\n- https://www.surveymonkey.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n\
  \  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SurveyMonkey\nserviceCategory: Surveys / Feedback\nbillingModel:\n  pricingCategory: Subscription + Usage (overage)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: SurveyMonkey\n  ServiceCategory: Surveys\n  ProviderName: SurveyMonkey\n  PublisherName: SurveyMonkey\n  InvoiceIssuerName: SurveyMonkey\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: user-month / response\nmeters:\n- name: seats\n  description: Active billable seats per plan tier.\n  unit: user-month\n  aggregation: max\n  dimensions:\n  - workgroup\n  - tier\n- name: responses\n  description: Survey responses counted against the annual bundle.\n  unit: response\n  aggregation: sum\n  dimensions:\n\
  \  - workgroup\n  - survey\n- name: response_overage\n  description: Responses above the annual bundle billed at $0.15 each.\n  unit: response\n  aggregation: sum\n  dimensions:\n  - workgroup\n- name: audience_panel\n  description: SurveyMonkey Audience paid-panel completes.\n  unit: completion\n  aggregation: sum\n  dimensions:\n  - workgroup\n  - survey\nprinciples:\n- name: Visibility\n  description: Use the SurveyMonkey admin Usage page; export response counts per survey for chargeback.\n- name: Allocation\n  description: Workgroups for Enterprise; use survey naming conventions otherwise.\n- name: Optimization\n  description: Right-size to Advantage vs Premier annually; consolidate seats; throttle long-running data exports to avoid unnecessary recompute.\n- name: Accountability\n  description: Assign workgroup owners; alert when annual response burn-down exceeds plan trajectory.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/surveymonkey/refs/heads/main/finops/surveymonkey-finops.yml
sources:
- https://www.surveymonkey.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Surveys
- Market Research
- Feedback
- NPS
- Forms
- FinOps
- Cost Management
- FOCUS
---
