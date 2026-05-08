---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mailchimp-marketing-api-openapi.yml
  format: yaml
  label: Mailchimp Marketing API
  slug: mailchimp-marketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mailchimp/refs/heads/main/openapi/mailchimp-marketing-api-openapi.yml
- filename: mailchimp-transactional-api-openapi.yml
  format: yaml
  label: Mailchimp Transactional API
  slug: mailchimp-transactional-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mailchimp/refs/heads/main/openapi/mailchimp-transactional-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Tiered by Contact Count
description: FOCUS-aligned FinOps for Mailchimp.
focus_columns:
  BillingCurrency: USD
  ProviderName: Mailchimp
  PublisherName: Mailchimp
  ServiceCategory: Email Marketing
  ServiceName: Mailchimp
layout: finops
meters:
- aggregation: max
  dimensions:
  - audience
  name: contacts
  unit: contact
- aggregation: sum
  name: email_sends
  unit: email
- aggregation: max
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: automation_runs
  unit: run
name: Mailchimp Finops
provider_name: Mailchimp
provider_slug: mailchimp
publisher_name: Mailchimp
service_category: Email Marketing
slug: mailchimp-finops
source_filename: mailchimp-finops.yml
source_heading: FinOps Profile
source_url: https://mailchimp.com/pricing/marketing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mailchimp\nproviderId: mailchimp\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Email Marketing\ndescription: FOCUS-aligned FinOps for Mailchimp.\nsources:\n  - https://mailchimp.com/pricing/marketing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mailchimp\nserviceCategory: Email Marketing\nbillingModel:\n  pricingCategory: Tiered by Contact Count\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Mailchimp\n  ServiceCategory: Email Marketing\n  ProviderName: Mailchimp\n  PublisherName: Mailchimp\n  BillingCurrency: USD\nmeters:\n  - name: contacts\n    unit: contact\n    aggregation: max\n\
  \    dimensions:\n      - audience\n  - name: email_sends\n    unit: email\n    aggregation: sum\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n  - name: automation_runs\n    unit: run\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Mailchimp consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mailchimp/refs/heads/main/finops/mailchimp-finops.yml
sources:
- https://mailchimp.com/pricing/marketing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Email Marketing
---
