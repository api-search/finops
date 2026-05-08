---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Microsoft Copilot API
  slug: ''
  spec_type: OpenAPI
  url: https://api.copilot.microsoft.com/openapi.json
- filename: openapi.json
  format: json
  label: Microsoft Graph API (Copilot Integration)
  slug: ''
  spec_type: OpenAPI
  url: https://graph.microsoft.com/openapi.json
- filename: microsoft-copilot-openapi.yml
  format: yaml
  label: Microsoft 365 Copilot APIs
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-copilot/refs/heads/main/openapi/microsoft-copilot-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly (annual commitment for enterprise SKU)
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription + Usage-Based (Copilot Studio messages)
description: FOCUS-aligned FinOps for Microsoft Copilot — predominantly per-user-per-month subscription pricing ($30 enterprise, $20 Pro, GitHub Copilot $10–$39) with a metered message-based PAYG layer for Copilot Studio. Largest waste signal is paying for inactive Copilot seats; secondary signal is Copilot Studio message overage. Visibility comes from Microsoft 365 admin center usage reports and Azure Monitor for Copilot Studio.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Subscription
  PricingUnit: user-month
  ProviderName: Microsoft Corporation
  PublisherName: Microsoft Corporation
  ServiceCategory: AI / Productivity
  ServiceName: Microsoft 365 Copilot
layout: finops
meters:
- aggregation: max
  description: Microsoft 365 Copilot enterprise add-on seats ($30/user/month).
  dimensions:
  - tenant
  - department
  - cost_center
  name: m365_copilot_seats
  unit: user-month
- aggregation: max
  description: Copilot Pro consumer seats ($20/user/month).
  dimensions:
  - billing_account
  name: copilot_pro_seats
  unit: user-month
- aggregation: sum
  description: Messages consumed by Copilot Studio agents.
  dimensions:
  - agent_name
  - environment
  - generative_or_classifier
  name: copilot_studio_messages
  unit: message
- aggregation: max
  description: Purchased monthly message-pack capacity.
  dimensions:
  - tenant
  - pack_size
  name: copilot_studio_message_pack
  unit: message-month
- aggregation: max
  description: GitHub Copilot Individual / Business / Enterprise seats.
  dimensions:
  - tier
  - org
  name: github_copilot_seats
  unit: user-month
- aggregation: count
  description: Unique users with at least one Copilot interaction in the period (utilization signal).
  dimensions:
  - app_used
  - period
  name: copilot_active_users
  unit: user
name: Microsoft Copilot Finops
provider_name: Microsoft Copilot
provider_slug: microsoft-copilot
publisher_name: Microsoft Corporation
service_category: AI / Productivity
slug: microsoft-copilot-finops
source_filename: microsoft-copilot-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/microsoft-365-copilot
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Copilot\nproviderId: microsoft-copilot\npublisherName: Microsoft Corporation\nserviceCategory: AI / Productivity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Agents\n  - AI Assistant\n  - Artificial Intelligence\n  - Chatbot\n  - Copilot\n  - Generative AI\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Microsoft Copilot — predominantly per-user-per-month\n  subscription pricing ($30 enterprise, $20 Pro, GitHub Copilot $10–$39) with a metered\n  message-based PAYG layer for Copilot Studio. Largest waste signal is paying for inactive\n  Copilot seats; secondary signal is Copilot Studio message\
  \ overage. Visibility comes from\n  Microsoft 365 admin center usage reports and Azure Monitor for Copilot Studio.\nsources:\n  - https://www.microsoft.com/microsoft-365-copilot\n  - https://learn.microsoft.com/en-us/microsoft-365-copilot/microsoft-365-copilot-licensing\n  - https://learn.microsoft.com/en-us/microsoft-365/admin/activity-reports/microsoft365-copilot-usage\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription + Usage-Based (Copilot Studio messages)\n  billingFrequency: Monthly (annual commitment for enterprise SKU)\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft 365 Copilot\n  ServiceCategory: AI / Productivity\n  ProviderName: Microsoft Corporation\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Subscription\n\
  \  PricingUnit: user-month\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: m365_copilot_seats\n    description: Microsoft 365 Copilot enterprise add-on seats ($30/user/month).\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - tenant\n      - department\n      - cost_center\n  - name: copilot_pro_seats\n    description: Copilot Pro consumer seats ($20/user/month).\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - billing_account\n  - name: copilot_studio_messages\n    description: Messages consumed by Copilot Studio agents.\n    unit: message\n    aggregation: sum\n    dimensions:\n      - agent_name\n      - environment\n      - generative_or_classifier\n  - name: copilot_studio_message_pack\n    description: Purchased monthly message-pack capacity.\n    unit: message-month\n    aggregation: max\n    dimensions:\n      - tenant\n      - pack_size\n  - name: github_copilot_seats\n    description: GitHub Copilot Individual / Business\
  \ / Enterprise seats.\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - tier\n      - org\n  - name: copilot_active_users\n    description: Unique users with at least one Copilot interaction in the period (utilization\n      signal).\n    unit: user\n    aggregation: count\n    dimensions:\n      - app_used\n      - period\nprinciples:\n  - name: Visibility\n    description: Microsoft 365 admin center > Reports > Microsoft 365 Copilot usage shows\n      per-user per-app interactions over the last 180 days. GitHub Copilot org-level usage\n      reports show acceptance rate and active users. Copilot Studio analytics graph message\n      consumption per agent. Cost Management exposes seat line items.\n  - name: Allocation\n    description: Assign seats by Entra ID security group rules tied to department/cost-center.\n      For Copilot Studio, environments map to business units; messages aggregate per\n      environment. Tag GitHub orgs to drive chargeback.\n  - name: Optimization\n\
  \    description: Reclaim seats from users who haven't used Copilot in 30+ days. Right-size\n      Copilot Studio message packs based on actual consumption (don't over-buy headroom).\n      Use the smaller Copilot Business SKU instead of enterprise where capability matches.\n      Avoid duplicating Copilot Pro for users who already have M365 Copilot. Consolidate\n      GitHub Copilot under Business or Enterprise when org has 5+ developers.\n  - name: Accountability\n    description: License manager owns seat assignment and reconciliation. Quarterly review of\n      per-user adoption metrics with line-of-business sponsors. Set alerts on Copilot Studio\n      message consumption to avoid PAYG surprises. Track unit economics — cost per active\n      user, cost per task automated.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.microsoft.com/microsoft-365-copilot\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-copilot/refs/heads/main/finops/microsoft-copilot-finops.yml
sources:
- https://www.microsoft.com/microsoft-365-copilot
- https://learn.microsoft.com/en-us/microsoft-365-copilot/microsoft-365-copilot-licensing
- https://learn.microsoft.com/en-us/microsoft-365/admin/activity-reports/microsoft365-copilot-usage
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Agents
- AI Assistant
- Artificial Intelligence
- Chatbot
- Copilot
- Generative AI
- FinOps
- FOCUS
---
