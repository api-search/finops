---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: comeet-careers-api-openapi.yml
  format: yaml
  label: Comeet Careers API
  slug: comeet-careers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/comeet/refs/heads/main/openapi/comeet-careers-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Comeet (Spark Hire Recruit): annual ATS subscription scaled by employee count, with included annual AI resume-review allotments per tier. API access is bundled, not metered.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Spark Hire, Inc.
  ProviderName: Spark Hire
  PublisherName: Spark Hire, Inc.
  ServiceCategory: HR Software
  ServiceName: Comeet (Spark Hire Recruit)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  - employee_band
  name: ats_subscription
  unit: month
- aggregation: sum
  dimensions:
  - tier
  name: ai_resume_reviews
  unit: review
- aggregation: sum
  name: video_interview_addon
  unit: month
- aggregation: sum
  name: behavioral_assessment_addon
  unit: month
name: Comeet Finops
provider_name: Comeet
provider_slug: comeet
publisher_name: Spark Hire, Inc.
service_category: HR Software
slug: comeet-finops
source_filename: comeet-finops.yml
source_heading: FinOps Profile
source_url: https://www.sparkhire.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Comeet\nproviderId: comeet\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - HR Tech\n  - Recruiting\ndescription: 'FOCUS-aligned FinOps for Comeet (Spark Hire Recruit): annual ATS subscription scaled by\n  employee count, with included annual AI resume-review allotments per tier. API access is bundled, not\n  metered.'\nsources:\n  - https://www.sparkhire.com/pricing\n  - https://developers.comeet.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Spark Hire, Inc.\nserviceCategory: HR Software\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    -\
  \ Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Comeet (Spark Hire Recruit)\n  ServiceCategory: HR Software\n  ProviderName: Spark Hire\n  PublisherName: Spark Hire, Inc.\n  InvoiceIssuerName: Spark Hire, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: ats_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - employee_band\n  - name: ai_resume_reviews\n    unit: review\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: video_interview_addon\n    unit: month\n    aggregation: sum\n  - name: behavioral_assessment_addon\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track AI-resume-review consumption against the annual allotment in the Spark Hire admin\n      console; monitor active hiring seats and pipeline volume.\n  - name: Allocation\n    description: Tag requisitions and hires by department/cost center to attribute ATS spend.\n  - name: Optimization\n\
  \    description: Right-size tier at annual renewal based on employee count and reviewer volume; bundle\n      video-interview/assessment add-ons only where used.\n  - name: Accountability\n    description: Talent acquisition leadership owns ATS license; finance owns annual renewal and add-on\n      spend.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/comeet/refs/heads/main/finops/comeet-finops.yml
sources:
- https://www.sparkhire.com/pricing
- https://developers.comeet.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- HR Tech
- Recruiting
---
