---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-exchange-graph-mail-openapi.yml
  format: yaml
  label: Microsoft Graph Mail API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-mail-openapi.yml
- filename: microsoft-exchange-graph-calendar-openapi.yml
  format: yaml
  label: Microsoft Graph Calendar API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-calendar-openapi.yml
- filename: microsoft-exchange-graph-contacts-openapi.yml
  format: yaml
  label: Microsoft Graph Contacts API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-contacts-openapi.yml
- filename: microsoft-exchange-graph-people-openapi.yml
  format: yaml
  label: Microsoft Graph People API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-people-openapi.yml
- filename: microsoft-exchange-admin-api-openapi.yml
  format: yaml
  label: Exchange Online Admin API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-admin-api-openapi.yml
- filename: microsoft-exchange-graph-import-export-openapi.yml
  format: yaml
  label: Microsoft Graph Mailbox Import Export API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-import-export-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Microsoft Exchange Online: per-user-per-month subscription (Plan 1 / Plan 2) or bundled into Microsoft 365 Business / Enterprise plans; mailbox storage and APIs included in seat licence with no incremental per-call charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Email and Collaboration
  ServiceName: Microsoft Exchange Online
layout: finops
meters:
- aggregation: sum
  description: Exchange Online seat licences (standalone Plan 1 / Plan 2 or bundled M365 SKU)
  dimensions:
  - tenant
  - sku
  name: exchange_seats
  unit: seat
- aggregation: sum
  description: Mailbox storage in use across primary and archive
  dimensions:
  - mailbox
  - mailbox_type
  name: mailbox_storage
  unit: GB
- aggregation: sum
  description: Microsoft Graph mail / calendar / contacts API calls (no charge; tracked for throttling)
  dimensions:
  - application
  - tenant
  name: mail_api_requests
  unit: request
- aggregation: sum
  description: Outbound SMTP messages per mailbox (subject to 30 msg/min and 10K recipients/day caps)
  dimensions:
  - mailbox
  name: smtp_messages
  unit: message
name: Microsoft Exchange Finops
provider_name: Microsoft Exchange
provider_slug: microsoft-exchange
publisher_name: Microsoft Corporation
service_category: Email and Collaboration
slug: microsoft-exchange-finops
source_filename: microsoft-exchange-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-365/exchange/compare-microsoft-exchange-online-plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Exchange\nproviderId: microsoft-exchange\npublisherName: Microsoft Corporation\nserviceCategory: Email and Collaboration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Email\n  - Calendar\n  - Microsoft 365\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Exchange Online: per-user-per-month subscription (Plan\n  1 / Plan 2) or bundled into Microsoft 365 Business / Enterprise plans; mailbox storage and APIs included\n  in seat licence with no incremental per-call charge.'\nsources:\n  - https://www.microsoft.com/en-us/microsoft-365/exchange/compare-microsoft-exchange-online-plans\n\
  \  - https://learn.microsoft.com/en-us/exchange/exchange-online\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Exchange Online\n  ServiceCategory: Email and Collaboration\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: exchange_seats\n    description: Exchange Online seat licences (standalone Plan 1 / Plan 2 or bundled M365 SKU)\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: mailbox_storage\n    description: Mailbox storage in use across primary and archive\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - mailbox\n      - mailbox_type\n  - name: mail_api_requests\n    description: Microsoft Graph mail / calendar / contacts\
  \ API calls (no charge; tracked for throttling)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - application\n      - tenant\n  - name: smtp_messages\n    description: Outbound SMTP messages per mailbox (subject to 30 msg/min and 10K recipients/day caps)\n    unit: message\n    aggregation: sum\n    dimensions:\n      - mailbox\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin centre licence report, Exchange admin centre mailbox usage\n      report, and the Message Trace API to observe consumption.\n  - name: Allocation\n    description: Map Exchange seats to Entra groups bound to cost-centres; tag programmatic mail traffic\n      by application via Graph application identity.\n  - name: Optimization\n    description: Right-size Plan 1 vs Plan 2 (auto-expanding archive only on Plan 2); reduce shared-mailbox\n      sprawl (shared mailboxes <50 GB don't need a paid licence); migrate from EWS to Graph for better\n      throttling headroom.\n\
  \  - name: Accountability\n    description: Workplace IT owns mailbox SKU mix and quota policy; security owns DLP / compliance hold\n      policies that affect storage growth.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/finops/microsoft-exchange-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-365/exchange/compare-microsoft-exchange-online-plans
- https://learn.microsoft.com/en-us/exchange/exchange-online
specification: FinOps Framework
tags:
- Email
- Calendar
- Microsoft 365
- Microsoft
- FinOps
- FOCUS
---
