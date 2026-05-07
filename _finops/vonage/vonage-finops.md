---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage SMS API
  slug: vonage-sms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Voice API
  slug: vonage-voice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Messages API
  slug: vonage-messages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Verify API
  slug: vonage-verify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Numbers API
  slug: vonage-numbers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Application API
  slug: vonage-application-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay As You Go (Per-Message/Minute)
description: FOCUS-aligned FinOps for Vonage.
focus_columns:
  BillingCurrency: USD
  ProviderName: Vonage
  PublisherName: Vonage
  ServiceCategory: Communications
  ServiceName: Vonage
layout: finops
meters:
- aggregation: sum
  dimensions:
  - direction
  - country
  - number_type
  name: sms_messages
  unit: message
- aggregation: sum
  dimensions:
  - direction
  - country
  name: voice_minutes
  unit: minute
- aggregation: sum
  dimensions:
  - channel
  - country
  name: verify_checks
  unit: check
- aggregation: max
  name: phone_numbers
  unit: number-month
name: Vonage Finops
provider_name: Vonage
provider_slug: vonage
publisher_name: Vonage
service_category: Communications
slug: vonage-finops
source_filename: vonage-finops.yml
source_heading: FinOps Profile
source_url: https://www.vonage.com/communications-apis/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Vonage\nproviderId: vonage\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Communications\ndescription: FOCUS-aligned FinOps for Vonage.\nsources:\n  - https://www.vonage.com/communications-apis/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Vonage\nserviceCategory: Communications\nbillingModel:\n  pricingCategory: Pay As You Go (Per-Message/Minute)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Vonage\n  ServiceCategory: Communications\n  ProviderName: Vonage\n  PublisherName: Vonage\n  BillingCurrency: USD\nmeters:\n  - name: sms_messages\n    unit: message\n    aggregation: sum\n\
  \    dimensions:\n      - direction\n      - country\n      - number_type\n  - name: voice_minutes\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - direction\n      - country\n  - name: verify_checks\n    unit: check\n    aggregation: sum\n    dimensions:\n      - channel\n      - country\n  - name: phone_numbers\n    unit: number-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Vonage consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/finops/vonage-finops.yml
sources:
- https://www.vonage.com/communications-apis/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Communications
---
