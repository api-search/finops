---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bandwidth-voice-api-openapi.yml
  format: yaml
  label: Bandwidth Voice API
  slug: voice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bandwidth/refs/heads/main/openapi/bandwidth-voice-api-openapi.yml
- filename: bandwidth-messaging-api-openapi.yml
  format: yaml
  label: Bandwidth Messaging API
  slug: messaging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bandwidth/refs/heads/main/openapi/bandwidth-messaging-api-openapi.yml
- filename: bandwidth-phone-numbers-api-openapi.yml
  format: yaml
  label: Bandwidth Phone Numbers API
  slug: phone-numbers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bandwidth/refs/heads/main/openapi/bandwidth-phone-numbers-api-openapi.yml
- filename: bandwidth-mfa-api-openapi.yml
  format: yaml
  label: Bandwidth Multi-Factor Authentication API
  slug: multi-factor-authentication-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bandwidth/refs/heads/main/openapi/bandwidth-mfa-api-openapi.yml
- filename: bandwidth-emergency-calling-api-openapi.yml
  format: yaml
  label: Bandwidth Emergency Calling API
  slug: emergency-calling-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bandwidth/refs/heads/main/openapi/bandwidth-emergency-calling-api-openapi.yml
- filename: bandwidth-toll-free-verification-api-openapi.yml
  format: yaml
  label: Bandwidth Toll-Free Verification API
  slug: toll-free-verification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bandwidth/refs/heads/main/openapi/bandwidth-toll-free-verification-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay As You Go
description: FOCUS-aligned FinOps for Bandwidth.
focus_columns:
  BillingCurrency: USD
  ProviderName: Bandwidth
  PublisherName: Bandwidth
  ServiceCategory: Communications
  ServiceName: Bandwidth
layout: finops
meters:
- aggregation: sum
  dimensions:
  - direction
  - number_type
  name: sms_messages
  unit: message
- aggregation: sum
  name: mms_messages
  unit: message
- aggregation: sum
  name: voice_minutes
  unit: minute
- aggregation: max
  name: phone_numbers
  unit: number-month
- aggregation: sum
  name: verify_attempts
  unit: attempt
name: Bandwidth Finops
provider_name: Bandwidth
provider_slug: bandwidth
publisher_name: Bandwidth
service_category: Communications
slug: bandwidth-finops
source_filename: bandwidth-finops.yml
source_heading: FinOps Profile
source_url: https://www.bandwidth.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bandwidth\nproviderId: bandwidth\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Communications\ndescription: FOCUS-aligned FinOps for Bandwidth.\nsources:\n  - https://www.bandwidth.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Bandwidth\nserviceCategory: Communications\nbillingModel:\n  pricingCategory: Pay As You Go\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Bandwidth\n  ServiceCategory: Communications\n  ProviderName: Bandwidth\n  PublisherName: Bandwidth\n  BillingCurrency: USD\nmeters:\n  - name: sms_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n\
  \      - direction\n      - number_type\n  - name: mms_messages\n    unit: message\n    aggregation: sum\n  - name: voice_minutes\n    unit: minute\n    aggregation: sum\n  - name: phone_numbers\n    unit: number-month\n    aggregation: max\n  - name: verify_attempts\n    unit: attempt\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Bandwidth consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bandwidth/refs/heads/main/finops/bandwidth-finops.yml
sources:
- https://www.bandwidth.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Communications
---
