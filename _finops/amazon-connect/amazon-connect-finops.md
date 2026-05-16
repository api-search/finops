---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-connect-openapi.yml
  format: yaml
  label: Amazon Connect Service API
  slug: amazon-connect-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-connect/refs/heads/main/openapi/amazon-connect-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Amazon Connect: pure pay-as-you-go billing per channel-minute or channel-message, with included AI capabilities and no seat-based licensing. Charges flow through the AWS invoice and Cost Explorer / FOCUS-formatted Cost & Usage Reports. Per-minute / per-message rates vary by region and third-party telephony provider; carrier and PSTN charges are billed in addition to channel rates.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: Amazon Web Services
  PublisherName: Amazon Web Services, Inc.
  RegionId: aws-region
  ServiceCategory: Contact Center
  ServiceName: Amazon Connect
layout: finops
meters:
- aggregation: sum
  description: Per-minute voice channel consumption (PSTN + WebRTC inbound/outbound)
  dimensions:
  - region
  - direction
  - country
  - instance
  name: voice_minutes
  unit: minute
- aggregation: sum
  description: Chat messages sent or received
  dimensions:
  - region
  - instance
  - direction
  name: chat_messages
  unit: message
- aggregation: sum
  description: Email messages sent or received
  dimensions:
  - region
  - instance
  - direction
  name: email_messages
  unit: message
- aggregation: sum
  description: SMS / third-party messaging messages sent or received
  dimensions:
  - region
  - instance
  - direction
  - carrier
  name: sms_messages
  unit: message
- aggregation: sum
  description: Task contacts processed
  dimensions:
  - region
  - instance
  name: tasks
  unit: contact
- aggregation: sum
  description: Pass-through PSTN / carrier charges separate from channel rate
  dimensions:
  - country
  - carrier
  name: pstn_charges
  unit: minute
name: Amazon Connect Finops
provider_name: Amazon Connect
provider_slug: amazon-connect
publisher_name: Amazon Web Services, Inc.
service_category: Contact Center
slug: amazon-connect-finops
source_filename: amazon-connect-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/connect/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amazon Connect\nproviderId: amazon-connect\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Contact Center\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud\n  - Contact Center\n  - Customer Engagement\n  - AI\n  - AWS\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Amazon Connect: pure pay-as-you-go billing per channel-minute or\n  channel-message, with included AI capabilities and no seat-based licensing. Charges flow through the\n  AWS invoice and Cost Explorer / FOCUS-formatted Cost & Usage Reports. Per-minute / per-message rates\n  vary by region and third-party telephony provider; carrier\
  \ and PSTN charges are billed in addition to\n  channel rates.'\nsources:\n  - https://aws.amazon.com/connect/pricing/\n  - https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Amazon Connect\n  ServiceCategory: Contact Center\n  ProviderName: Amazon Web Services\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  RegionId: aws-region\nmeters:\n  - name: voice_minutes\n    description: Per-minute voice channel consumption (PSTN + WebRTC inbound/outbound)\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - region\n      - direction\n      - country\n  \
  \    - instance\n  - name: chat_messages\n    description: Chat messages sent or received\n    unit: message\n    aggregation: sum\n    dimensions:\n      - region\n      - instance\n      - direction\n  - name: email_messages\n    description: Email messages sent or received\n    unit: message\n    aggregation: sum\n    dimensions:\n      - region\n      - instance\n      - direction\n  - name: sms_messages\n    description: SMS / third-party messaging messages sent or received\n    unit: message\n    aggregation: sum\n    dimensions:\n      - region\n      - instance\n      - direction\n      - carrier\n  - name: tasks\n    description: Task contacts processed\n    unit: contact\n    aggregation: sum\n    dimensions:\n      - region\n      - instance\n  - name: pstn_charges\n    description: Pass-through PSTN / carrier charges separate from channel rate\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - country\n      - carrier\nprinciples:\n  - name: Visibility\n    description:\
  \ Use AWS Cost Explorer, AWS Cost & Usage Reports (CUR with FOCUS export), and CloudWatch\n      contact-center metrics (ConcurrentCalls, ConcurrentChats, ConcurrentEmailsPercentage) to see per-channel\n      consumption. Tag Connect instances and AWS resources for granular reporting.\n  - name: Allocation\n    description: Allocate Connect cost to lines of business by tagging the Connect instance, breaking\n      out per-region usage, and using Cost Categories in AWS Cost Explorer for consolidated billing accounts.\n  - name: Optimization\n    description: Reduce per-minute spend by tuning IVR flows, leveraging chat/email/SMS where appropriate,\n      adopting persistent chat to avoid idle-chat quota consumption, using included AI capabilities (forecasting,\n      scheduling, conversational analytics) instead of paid third-party tools, and right-sizing concurrent-call\n      / chat / email quotas pre-go-live to avoid throttle-driven contact loss.\n  - name: Accountability\n    description:\
  \ Contact-center / CX leadership owns the Connect spend; integrate per-channel cost into\n      monthly call-center reviews; configure CloudWatch alarms at 80% of quota and Service Quotas requests\n      ahead of growth.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-connect/refs/heads/main/finops/amazon-connect-finops.yml
sources:
- https://aws.amazon.com/connect/pricing/
- https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Cloud
- Contact Center
- Customer Engagement
- AI
- FinOps
- FOCUS
---
