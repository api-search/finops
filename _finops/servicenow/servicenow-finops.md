---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: servicenow-table-api-openapi.yml
  format: yaml
  label: ServiceNow Table API
  slug: servicenow-table-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-table-api-openapi.yml
- filename: servicenow-aggregate-api-openapi.yml
  format: yaml
  label: ServiceNow Aggregate API
  slug: servicenow-aggregate-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-aggregate-api-openapi.yml
- filename: servicenow-attachment-api-openapi.yml
  format: yaml
  label: ServiceNow Attachment API
  slug: servicenow-attachment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-attachment-api-openapi.yml
- filename: servicenow-import-set-api-openapi.yml
  format: yaml
  label: ServiceNow Import Set API
  slug: servicenow-import-set-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-import-set-api-openapi.yml
- filename: servicenow-change-management-api-openapi.yml
  format: yaml
  label: ServiceNow Change Management API
  slug: servicenow-change-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-change-management-api-openapi.yml
- filename: servicenow-service-catalog-api-openapi.yml
  format: yaml
  label: ServiceNow Service Catalog API
  slug: servicenow-service-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-service-catalog-api-openapi.yml
- filename: servicenow-cmdb-instance-api-openapi.yml
  format: yaml
  label: ServiceNow CMDB Instance API
  slug: servicenow-cmdb-instance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/servicenow-cmdb-instance-api-openapi.yml
- filename: contact-api-openapi.yaml
  format: yaml
  label: ServiceNow Contact API
  slug: servicenow-contact-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/contact-api-openapi.yaml
- filename: trouble-ticket-openapi.yaml
  format: yaml
  label: ServiceNow Trouble Ticket Open API
  slug: servicenow-trouble-ticket-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/openapi/trouble-ticket-openapi.yaml
- filename: servicenow-events-asyncapi.yml
  format: yaml
  label: ServiceNow Event Management Topic Open API
  slug: servicenow-event-management-topic-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/asyncapi/servicenow-events-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription + Consumption Units
description: FinOps shape for ServiceNow — a quote-based enterprise SaaS platform. Cost is dominated by negotiated subscription line items (fulfiller / requester users, named modules, Now Assist consumption units, Integration Hub transactions). Numeric pricing is not published and is negotiated per contract. Integration consumption (table API calls, Integration Hub transactions, Now Assist tokens) maps to internal instance meters that ServiceNow exposes through Subscription Management Lifecycle and Performance Analytics.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ServiceNow, Inc.
  ProviderName: ServiceNow
  PublisherName: ServiceNow, Inc.
  ServiceCategory: Enterprise Workflow / ITSM
  ServiceName: ServiceNow Now Platform
layout: finops
meters:
- aggregation: max
  description: Named fulfiller / agent users (primary subscription driver)
  dimensions:
  - role
  name: fulfiller_users
  unit: seat
- aggregation: max
  description: Requester / employee users where licensed
  name: requester_users
  unit: seat
- aggregation: sum
  description: Integration Hub transactions consumed against the subscription pool
  dimensions:
  - flow
  - spoke
  name: integration_hub_transactions
  unit: transaction
- aggregation: sum
  description: Now Assist generative-AI consumption units (where licensed)
  dimensions:
  - module
  name: now_assist_consumption_units
  unit: consumption-unit
- aggregation: sum
  description: Custom Table Updates / table API write volume against the entitlement
  dimensions:
  - table
  name: custom_table_updates
  unit: update
- aggregation: sum
  description: Negotiated annual subscription fee (modules + seats)
  dimensions:
  - module
  name: subscription_fee
  unit: year
name: Servicenow Finops
provider_name: ServiceNow
provider_slug: servicenow
publisher_name: ServiceNow, Inc.
service_category: Enterprise Workflow / Now Platform
slug: servicenow-finops
source_filename: servicenow-finops.yml
source_heading: FinOps Profile
source_url: https://www.servicenow.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ServiceNow\nproviderId: servicenow\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - ITSM\n  - Now Platform\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for ServiceNow — a quote-based enterprise SaaS platform. Cost is dominated\n  by negotiated subscription line items (fulfiller / requester users, named modules, Now Assist consumption\n  units, Integration Hub transactions). Numeric pricing is not published and is negotiated per contract.\n  Integration consumption (table API calls, Integration Hub transactions, Now Assist tokens) maps to internal\n  instance meters that ServiceNow exposes through Subscription Management Lifecycle and Performance Analytics.\nsources:\n  - https://www.servicenow.com/\nnotes: Pricing line items, FOCUS column mappings, and meter unit prices are not publicly disclosed; reconciled\n  to known commercial\
  \ structure only.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ServiceNow, Inc.\nserviceCategory: Enterprise Workflow / Now Platform\nbillingModel:\n  pricingCategory: Subscription + Consumption Units\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: ServiceNow Now Platform\n  ServiceCategory: Enterprise Workflow / ITSM\n  ProviderName: ServiceNow\n  PublisherName: ServiceNow, Inc.\n  InvoiceIssuerName: ServiceNow, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: fulfiller_users\n    description: Named fulfiller / agent users (primary subscription driver)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n  - name: requester_users\n    description: Requester / employee users where licensed\n    unit:\
  \ seat\n    aggregation: max\n  - name: integration_hub_transactions\n    description: Integration Hub transactions consumed against the subscription pool\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - flow\n      - spoke\n  - name: now_assist_consumption_units\n    description: Now Assist generative-AI consumption units (where licensed)\n    unit: consumption-unit\n    aggregation: sum\n    dimensions:\n      - module\n  - name: custom_table_updates\n    description: Custom Table Updates / table API write volume against the entitlement\n    unit: update\n    aggregation: sum\n    dimensions:\n      - table\n  - name: subscription_fee\n    description: Negotiated annual subscription fee (modules + seats)\n    unit: year\n    aggregation: sum\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n    description: Use ServiceNow Subscription Management Lifecycle, Performance Analytics, and the SAM\n      Pro app to track entitlement burn for users, transactions,\
  \ and Now Assist consumption units. Custom\n      reports on sys_audit and the integration_hub.transaction tables expose granular activity.\n  - name: Allocation\n    description: Allocate subscription cost by user role / department from the user table, and tag integrations\n      with a consuming-application reference so Integration Hub transaction usage rolls up to the right\n      cost center.\n  - name: Optimization\n    description: Right-size fulfiller seats annually against actual login activity; consolidate redundant\n      Integration Hub flows; cap Now Assist usage with platform guardrails before approving generative-AI\n      features in production.\n  - name: Accountability\n    description: ServiceNow CoE / Platform owner is accountable for entitlement burn and rate-limit\n      configuration; finance leads contract renegotiation; module owners (ITSM, HRSD, CSM) defend their\n      seat counts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/servicenow/refs/heads/main/finops/servicenow-finops.yml
sources:
- https://www.servicenow.com/
specification: FinOps Framework
tags:
- ITSM
- Now Platform
- FinOps
- FOCUS
---
