---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: figma-api-openapi.yml
  format: yaml
  label: Figma API
  slug: figma-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma REST API
  slug: figma-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-files-api-openapi.yml
  format: yaml
  label: Figma Files API
  slug: figma-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-files-api-openapi.yml
- filename: figma-images-api-openapi.yml
  format: yaml
  label: Figma Images API
  slug: figma-images-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-images-api-openapi.yml
- filename: figma-teams-api-openapi.yml
  format: yaml
  label: Figma Teams API
  slug: figma-teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-teams-api-openapi.yml
- filename: figma-projects-api-openapi.yml
  format: yaml
  label: Figma Projects API
  slug: figma-projects-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-projects-api-openapi.yml
- filename: figma-me-api-openapi.yml
  format: yaml
  label: Figma Me API
  slug: figma-me-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-me-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Components API
  slug: figma-components-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-component-sets-api-openapi.yml
  format: yaml
  label: Figma Component Sets API
  slug: figma-component-sets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-component-sets-api-openapi.yml
- filename: figma-styles-api-openapi.yml
  format: yaml
  label: Figma Styles API
  slug: figma-styles-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-styles-api-openapi.yml
- filename: figma-activity-logs-api-openapi.yml
  format: yaml
  label: Figma Activity Logs API
  slug: figma-activity-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-activity-logs-api-openapi.yml
- filename: figma-payments-api-openapi.yml
  format: yaml
  label: Figma Payments API
  slug: figma-payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-payments-api-openapi.yml
- filename: figma-dev-resources-api-openapi.yml
  format: yaml
  label: Figma Dev Resources API
  slug: figma-dev-resources-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-dev-resources-api-openapi.yml
- filename: figma-analytics-api-openapi.yml
  format: yaml
  label: Figma Analytics API
  slug: figma-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-analytics-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Comments API
  slug: figma-comments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Version History API
  slug: figma-version-history-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Variables API
  slug: figma-variables-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Library Analytics API
  slug: figma-library-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for Figma.
focus_columns:
  BillingCurrency: USD
  ProviderName: Figma
  PublisherName: Figma
  ServiceCategory: Design
  ServiceName: Figma
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: full_seats
  unit: seat-month
- aggregation: max
  name: view_seats
  unit: seat-month
- aggregation: sum
  name: ai_credits
  unit: credit
name: Figma Finops
provider_name: Figma
provider_slug: figma
publisher_name: Figma
service_category: Design
slug: figma-finops
source_filename: figma-finops.yml
source_heading: FinOps Profile
source_url: https://www.figma.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Figma\nproviderId: figma\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Design\ndescription: FOCUS-aligned FinOps for Figma.\nsources:\n  - https://www.figma.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Figma\nserviceCategory: Design\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Figma\n  ServiceCategory: Design\n  ProviderName: Figma\n  PublisherName: Figma\n  BillingCurrency: USD\nmeters:\n  - name: full_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n  - name: view_seats\n    unit:\
  \ seat-month\n    aggregation: max\n  - name: ai_credits\n    unit: credit\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Figma consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/finops/figma-finops.yml
sources:
- https://www.figma.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Design
---
