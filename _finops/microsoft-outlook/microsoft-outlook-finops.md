---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-graph-mail-api-openapi.yml
  format: yaml
  label: Microsoft Graph Mail API
  slug: microsoft-graph-mail-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-outlook/refs/heads/main/openapi/microsoft-graph-mail-api-openapi.yml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Calendar API
  slug: microsoft-graph-calendar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Contacts API
  slug: microsoft-graph-contacts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Tasks API
  slug: microsoft-graph-tasks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph People API
  slug: microsoft-graph-people-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Change Notifications API
  slug: microsoft-graph-change-notifications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Focused Inbox API
  slug: microsoft-graph-focused-inbox-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Mail Rules API
  slug: microsoft-graph-mail-rules-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Categories API
  slug: microsoft-graph-categories-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Bundled with Microsoft 365 / Exchange Online
description: 'FOCUS-aligned FinOps for Microsoft Outlook: free with a consumer Microsoft account (Outlook.com), bundled into Microsoft 365 / Office 365 / Exchange Online for work and school. APIs included with the seat licence; no per-call charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Email and Calendar
  ServiceName: Microsoft Outlook
layout: finops
meters:
- aggregation: sum
  description: Outlook entitlement via Microsoft 365 / Exchange Online seat licences
  dimensions:
  - tenant
  - sku
  name: outlook_seats
  unit: seat
- aggregation: sum
  description: Mailbox storage in use (primary + archive)
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
  - resource
  name: graph_mail_calendar_requests
  unit: request
- aggregation: sum
  description: Outbound SMTP messages per mailbox
  dimensions:
  - mailbox
  name: smtp_messages_sent
  unit: message
name: Microsoft Outlook Finops
provider_name: Microsoft Outlook
provider_slug: microsoft-outlook
publisher_name: Microsoft Corporation
service_category: Email and Calendar
slug: microsoft-outlook-finops
source_filename: microsoft-outlook-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-365/outlook/email-and-calendar-software-microsoft-outlook
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Outlook\nproviderId: microsoft-outlook\npublisherName: Microsoft Corporation\nserviceCategory: Email and Calendar\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Email\n  - Calendar\n  - Microsoft 365\n  - Microsoft\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Microsoft Outlook: free with a consumer Microsoft account (Outlook.com),\n  bundled into Microsoft 365 / Office 365 / Exchange Online for work and school. APIs included with the\n  seat licence; no per-call charge.'\nsources:\n  - https://www.microsoft.com/en-us/microsoft-365/outlook/email-and-calendar-software-microsoft-outlook\n  -\
  \ https://www.microsoft.com/en-us/microsoft-365/exchange/compare-microsoft-exchange-online-plans\nbillingModel:\n  pricingCategory: Bundled with Microsoft 365 / Exchange Online\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Microsoft Outlook\n  ServiceCategory: Email and Calendar\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: outlook_seats\n    description: Outlook entitlement via Microsoft 365 / Exchange Online seat licences\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tenant\n      - sku\n  - name: mailbox_storage\n    description: Mailbox storage in use (primary + archive)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - mailbox\n      - mailbox_type\n  - name: graph_mail_calendar_requests\n    description:\
  \ Microsoft Graph mail / calendar / contacts API calls (no charge; tracked for throttling)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - application\n      - tenant\n      - resource\n  - name: smtp_messages_sent\n    description: Outbound SMTP messages per mailbox\n    unit: message\n    aggregation: sum\n    dimensions:\n      - mailbox\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin centre user-activity reports, Exchange admin centre mailbox\n      usage report, and Message Trace API for inbound / outbound visibility.\n  - name: Allocation\n    description: Tag mailboxes by department / cost-centre via Entra group-based licensing; tag programmatic\n      mail traffic by the Graph application identity.\n  - name: Optimization\n    description: Convert seldom-used user mailboxes to shared mailboxes (no licence under 50 GB); migrate\n      from EWS to Microsoft Graph; replace polling with change notifications; right-size Plan 1 vs Plan\n\
  \      2 based on archive needs.\n  - name: Accountability\n    description: Workplace IT owns Outlook policy and licence assignment; security owns DLP / Defender\n      for Office 365 policy; finance owns Exchange / M365 SKU mix.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-outlook/refs/heads/main/finops/microsoft-outlook-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-365/outlook/email-and-calendar-software-microsoft-outlook
- https://www.microsoft.com/en-us/microsoft-365/exchange/compare-microsoft-exchange-online-plans
specification: FinOps Framework
tags:
- Email
- Calendar
- Microsoft 365
- Microsoft
- FinOps
- FOCUS
---
