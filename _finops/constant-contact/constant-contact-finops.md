---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.yaml
  format: yaml
  label: Constant Contact V3 API
  slug: v3
  spec_type: OpenAPI
  url: https://api.cc.email/v3/swagger.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Tiered by Contact Count
description: FOCUS-aligned FinOps for Constant Contact.
focus_columns:
  BillingCurrency: USD
  ProviderName: Constant Contact
  PublisherName: Constant Contact
  ServiceCategory: Email Marketing
  ServiceName: Constant Contact
layout: finops
meters:
- aggregation: max
  dimensions:
  - list
  name: contacts
  unit: contact
- aggregation: sum
  name: emails_sent
  unit: email
- aggregation: max
  dimensions:
  - plan
  name: monthly_subscription
  unit: month
name: Constant Contact Finops
provider_name: Constant Contact
provider_slug: constant-contact
publisher_name: Constant Contact
service_category: Email Marketing
slug: constant-contact-finops
source_filename: constant-contact-finops.yml
source_heading: FinOps Profile
source_url: https://www.constantcontact.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Constant Contact\nproviderId: constant-contact\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Email Marketing\ndescription: FOCUS-aligned FinOps for Constant Contact.\nsources:\n  - https://www.constantcontact.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Constant Contact\nserviceCategory: Email Marketing\nbillingModel:\n  pricingCategory: Tiered by Contact Count\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Constant Contact\n  ServiceCategory: Email Marketing\n  ProviderName: Constant Contact\n  PublisherName: Constant Contact\n  BillingCurrency: USD\nmeters:\n  - name: contacts\n\
  \    unit: contact\n    aggregation: max\n    dimensions:\n      - list\n  - name: emails_sent\n    unit: email\n    aggregation: sum\n  - name: monthly_subscription\n    unit: month\n    aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Track Constant Contact consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/constant-contact/refs/heads/main/finops/constant-contact-finops.yml
sources:
- https://www.constantcontact.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Email Marketing
---
