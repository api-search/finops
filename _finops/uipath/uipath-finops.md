---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: uipath-orchestrator-openapi.yml
  format: yaml
  label: UiPath Orchestrator API
  slug: uipath-orchestrator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uipath/refs/heads/main/openapi/uipath-orchestrator-openapi.yml
- filename: uipath-automation-hub-openapi.yml
  format: yaml
  label: UiPath Automation Hub API
  slug: uipath-automation-hub-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uipath/refs/heads/main/openapi/uipath-automation-hub-openapi.yml
- filename: uipath-document-understanding-openapi.yml
  format: yaml
  label: UiPath Document Understanding API
  slug: uipath-document-understanding-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uipath/refs/heads/main/openapi/uipath-document-understanding-openapi.yml
- filename: uipath-data-service-openapi.yml
  format: yaml
  label: UiPath Data Service API
  slug: uipath-data-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uipath/refs/heads/main/openapi/uipath-data-service-openapi.yml
- filename: uipath-platform-management-openapi.yml
  format: yaml
  label: UiPath Platform Management API
  slug: uipath-platform-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uipath/refs/heads/main/openapi/uipath-platform-management-openapi.yml
- filename: uipath-test-manager-openapi.yml
  format: yaml
  label: UiPath Test Manager API
  slug: uipath-test-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uipath/refs/heads/main/openapi/uipath-test-manager-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for UiPath: tiered subscription model with one self-service Basic tier ($25/month, EU only) and contact-sales Standard / Enterprise tiers covering Automation Cloud and Test Cloud. Billable units are users, robots, AI agent calls, and document-understanding consumption.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: UiPath, Inc.
  ProviderName: UiPath
  PublisherName: UiPath, Inc.
  ServiceCategory: Automation / RPA
  ServiceName: UiPath Automation Cloud
layout: finops
meters:
- aggregation: max
  description: User entitlements (Basic, Plus, Pro) per organization
  dimensions:
  - user_type
  - tier
  name: user_seats
  unit: seat
- aggregation: max
  description: Attended and unattended robots licensed per organization
  dimensions:
  - robot_type
  - tier
  name: robots
  unit: robot
- aggregation: sum
  description: AI agent invocations (Standard / Enterprise tiers, unlimited inside contract terms)
  dimensions:
  - agent
  - tier
  name: ai_agent_calls
  unit: invocation
- aggregation: sum
  description: Pages processed by document classification / extraction
  dimensions:
  - model
  name: document_understanding_pages
  unit: page
- aggregation: sum
  description: Identity Server / Orchestrator API calls (subject to per-org rate limits)
  dimensions:
  - service
  - http_method
  name: api_requests
  unit: request
name: Uipath Finops
provider_name: UiPath
provider_slug: uipath
publisher_name: UiPath, Inc.
service_category: Automation / RPA
slug: uipath-finops
source_filename: uipath-finops.yml
source_heading: FinOps Profile
source_url: https://www.uipath.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: UiPath\nproviderId: uipath\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Automation\n  - RPA\n  - AI\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for UiPath: tiered subscription model with one self-service Basic\n  tier ($25/month, EU only) and contact-sales Standard / Enterprise tiers covering Automation Cloud and\n  Test Cloud. Billable units are users, robots, AI agent calls, and document-understanding consumption.'\nsources:\n  - https://www.uipath.com/pricing\n  - https://docs.uipath.com/automation-cloud/automation-cloud/latest/api-guide/api-rate-limits-for-identity-server\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: UiPath, Inc.\nserviceCategory: Automation / RPA\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: UiPath Automation Cloud\n  ServiceCategory: Automation / RPA\n  ProviderName: UiPath\n  PublisherName: UiPath, Inc.\n  InvoiceIssuerName: UiPath, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    description: User entitlements (Basic, Plus, Pro) per organization\n    unit: seat\n    aggregation: max\n    dimensions:\n      - user_type\n      - tier\n  - name: robots\n    description: Attended and unattended robots licensed per organization\n    unit: robot\n    aggregation: max\n    dimensions:\n      - robot_type\n      - tier\n  - name: ai_agent_calls\n    description: AI agent invocations (Standard / Enterprise tiers, unlimited inside contract terms)\n    unit: invocation\n    aggregation: sum\n\
  \    dimensions:\n      - agent\n      - tier\n  - name: document_understanding_pages\n    description: Pages processed by document classification / extraction\n    unit: page\n    aggregation: sum\n    dimensions:\n      - model\n  - name: api_requests\n    description: Identity Server / Orchestrator API calls (subject to per-org rate limits)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - http_method\nprinciples:\n  - name: Visibility\n    description: Use the Automation Cloud admin console, Insights dashboards, and Orchestrator audit\n      APIs to attribute robot, user, and agent consumption per tenant and folder.\n  - name: Allocation\n    description: Tag automations and Orchestrator folders with consuming team / process owner so robot-hours,\n      AI agent calls, and document-understanding pages can be charged back.\n  - name: Optimization\n    description: Right-size between Basic / Standard / Enterprise tiers, retire idle robots, batch documents\n\
  \      to amortize per-page costs, and design integrations to stay under the Identity Server 5-minute\n      method limits to avoid 429-driven retries.\n  - name: Accountability\n    description: Center-of-Excellence and platform owners review tier entitlement vs actual robot, agent,\n      and document consumption ahead of each renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/uipath/refs/heads/main/finops/uipath-finops.yml
sources:
- https://www.uipath.com/pricing
- https://docs.uipath.com/automation-cloud/automation-cloud/latest/api-guide/api-rate-limits-for-identity-server
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Automation
- RPA
- AI
- FinOps
- FOCUS
---
