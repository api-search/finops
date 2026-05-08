---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox Conversational AI API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox Company API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox Candidates API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox Users API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox Scheduling API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox Locations API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox Candidate Attributes API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
- filename: paradox-api-openapi.yml
  format: yaml
  label: Paradox User Permissions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/openapi/paradox-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: Subscription (Enterprise)
description: Structural FinOps definition for Paradox. Subscription-based HR tech sold via sales motion; meters reflect plausible enterprise shape pending contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Paradox, Inc.
  ProviderName: Paradox
  PublisherName: Paradox, Inc.
  ServiceCategory: HR Technology
  ServiceName: Paradox
layout: finops
meters:
- aggregation: sum
  description: Hires or applications processed through Olivia (typical HR-tech billable unit)
  dimensions:
  - org
  - location
  name: hires_processed
  unit: hire
- aggregation: sum
  description: SMS / chat conversations handled by Olivia
  dimensions:
  - channel
  - org
  name: messages_sent
  unit: message
- aggregation: max
  description: Recruiter seats with access to Paradox
  dimensions:
  - org
  name: subscription_seats
  unit: seat-month
name: Paradox Finops
provider_name: Paradox
provider_slug: paradox
publisher_name: Paradox, Inc.
service_category: HR Technology
slug: paradox-finops
source_filename: paradox-finops.yml
source_heading: FinOps Profile
source_url: https://www.paradox.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Paradox\nproviderId: paradox\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: No public pricing or usage API. Structural FinOps placeholder; meters reflect typical\n  HR-tech subscription shape pending contract disclosure.\ntags:\n  - FinOps\n  - FOCUS\n  - HR Technology\n  - Conversational AI\n  - Recruiting\ndescription: Structural FinOps definition for Paradox. Subscription-based HR tech sold via\n  sales motion; meters reflect plausible enterprise shape pending contract.\nsources:\n  - https://www.paradox.ai/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Paradox, Inc.\nserviceCategory:\
  \ HR Technology\nbillingModel:\n  pricingCategory: Subscription (Enterprise)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: Paradox\n  ServiceCategory: HR Technology\n  ProviderName: Paradox\n  PublisherName: Paradox, Inc.\n  InvoiceIssuerName: Paradox, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: hires_processed\n    description: Hires or applications processed through Olivia (typical HR-tech billable\n      unit)\n    unit: hire\n    aggregation: sum\n    dimensions:\n      - org\n      - location\n  - name: messages_sent\n    description: SMS / chat conversations handled by Olivia\n    unit: message\n    aggregation: sum\n    dimensions:\n      - channel\n      - org\n  - name: subscription_seats\n    description: Recruiter seats with access to Paradox\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - org\nprinciples:\n  - name: Visibility\n    description:\
  \ Visibility relies on Paradox reporting dashboards; usage breakdown is contract-\n      and tenant-specific.\n  - name: Allocation\n    description: Allocate by hiring location/org and recruiter team using Paradox's role-based\n      access model.\n  - name: Optimization\n    description: Optimize by routing high-volume requisitions through Olivia automation and\n      retiring unused recruiter seats.\n  - name: Accountability\n    description: Talent-acquisition leader accountable for Paradox spend; reviews at renewal\n      against hires/messages realized.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/paradox/refs/heads/main/finops/paradox-finops.yml
sources:
- https://www.paradox.ai/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- HR Technology
- Conversational AI
- Recruiting
---
