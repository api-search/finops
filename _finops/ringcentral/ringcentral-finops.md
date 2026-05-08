---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ringcentral-platform-openapi.yml
  format: yaml
  label: RingCentral Voice API
  slug: ringcentral-voice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ringcentral/refs/heads/main/openapi/ringcentral-platform-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  billingTerm: Annual or Month-to-Month
  chargeCategories:
  - Subscription
  - Usage
  - Adjustment
  - Tax
  commitmentDiscount: Annual prepay discount of approximately 33% versus monthly term
  pricingCategory: Per-Seat Subscription with Usage Overages
description: RingCentral's billing surface is a per-seat SaaS subscription model (RingEX Core/Advanced/Ultra and RingCX agent seats) with usage-priced overages for international calling, SMS/MMS volume, fax pages, and toll-free minutes. The developer API itself is not metered — costs flow through the underlying RingEX/RingCX subscription consumed by the application. Add-on subscriptions (AI Receptionist, SMS Booster, Call Queues Booster, AI Conversation Expert) are flat monthly fees layered on top of seat counts.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  CommitmentDiscountCategory: Spend
  InvoiceIssuerName: RingCentral
  PricingCategory: Standard Pricing
  ProviderName: RingCentral
  PublisherName: RingCentral
  ServiceCategory: Communications
  ServiceName: RingCentral RingEX
layout: finops
meters:
- aggregation: max
  description: Per-user RingEX subscription (Core / Advanced / Ultra).
  dimensions:
  - account
  - user
  - plan_tier
  name: ringex_seats
  unit: seat-month
- aggregation: max
  description: Per-agent RingCX contact-center subscription.
  dimensions:
  - account
  - agent
  - package
  name: ringcx_agent_seats
  unit: seat-month
- aggregation: sum
  description: Outbound minutes outside the bundled US/Canada plan.
  dimensions:
  - account
  - destination_country
  - call_type
  name: international_minutes
  unit: minute
- aggregation: sum
  description: Outbound SMS/MMS segments beyond bundled allotments (A2P 10DLC).
  dimensions:
  - account
  - direction
  - country
  name: sms_segments
  unit: segment
- aggregation: sum
  description: Inbound minutes on toll-free DIDs.
  dimensions:
  - account
  - did
  name: toll_free_minutes
  unit: minute
- aggregation: sum
  description: Outbound fax pages above the bundled allotment.
  dimensions:
  - account
  name: fax_pages
  unit: page
- aggregation: max
  description: Add-on subscriptions (AI Receptionist, SMS Booster, Call Queues Booster, AI Conversation Expert).
  dimensions:
  - account
  - addon_name
  name: addon_subscriptions
  unit: subscription-month
name: Ringcentral Finops
provider_name: RingCentral
provider_slug: ringcentral
publisher_name: RingCentral
service_category: Communications
slug: ringcentral-finops
source_filename: ringcentral-finops.yml
source_heading: FinOps Profile
source_url: https://www.ringcentral.com/office/plansandpricing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: RingCentral\nproviderId: ringcentral\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Communications\n  - UCaaS\n  - Voice\n  - Video\n  - Contact Center\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: >-\n  RingCentral's billing surface is a per-seat SaaS subscription model (RingEX Core/Advanced/Ultra and RingCX agent seats) with usage-priced overages for international calling, SMS/MMS volume, fax pages, and toll-free minutes. The developer API itself is not metered — costs flow through the underlying RingEX/RingCX subscription consumed by the application. Add-on subscriptions (AI Receptionist, SMS Booster, Call Queues Booster, AI Conversation Expert) are flat monthly fees layered on top of seat counts.\nnotes: >-\n  Reconciled against RingCentral published pricing as of 2026-05-08. RingCentral does not publish a public FOCUS-formatted\
  \ billing export; usage detail is available via the Admin Portal and Cost Management exports for enterprise contracts.\nsources:\n  - https://www.ringcentral.com/office/plansandpricing.html\n  - https://www.ringcentral.com/contact-center/overview.html\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: RingCentral\nserviceCategory: Communications\nbillingModel:\n  pricingCategory: Per-Seat Subscription with Usage Overages\n  billingFrequency: Monthly\n  billingTerm: Annual or Month-to-Month\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\n    - Tax\n  commitmentDiscount: Annual prepay discount of approximately 33% versus monthly term\nfocusColumns:\n  ServiceName: RingCentral RingEX\n  ServiceCategory: Communications\n\
  \  ProviderName: RingCentral\n  PublisherName: RingCentral\n  InvoiceIssuerName: RingCentral\n  BillingCurrency: USD\n  ChargeCategory: Subscription\n  PricingCategory: Standard Pricing\n  CommitmentDiscountCategory: Spend\nmeters:\n  - name: ringex_seats\n    description: Per-user RingEX subscription (Core / Advanced / Ultra).\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - account\n      - user\n      - plan_tier\n  - name: ringcx_agent_seats\n    description: Per-agent RingCX contact-center subscription.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - account\n      - agent\n      - package\n  - name: international_minutes\n    description: Outbound minutes outside the bundled US/Canada plan.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - account\n      - destination_country\n      - call_type\n  - name: sms_segments\n    description: Outbound SMS/MMS segments beyond bundled allotments (A2P 10DLC).\n    unit: segment\n \
  \   aggregation: sum\n    dimensions:\n      - account\n      - direction\n      - country\n  - name: toll_free_minutes\n    description: Inbound minutes on toll-free DIDs.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - account\n      - did\n  - name: fax_pages\n    description: Outbound fax pages above the bundled allotment.\n    unit: page\n    aggregation: sum\n    dimensions:\n      - account\n  - name: addon_subscriptions\n    description: Add-on subscriptions (AI Receptionist, SMS Booster, Call Queues Booster, AI Conversation Expert).\n    unit: subscription-month\n    aggregation: max\n    dimensions:\n      - account\n      - addon_name\nprinciples:\n  - name: Visibility\n    description: >-\n      Pull invoice exports and Admin Portal usage reports into your cost-allocation pipeline. RingCentral does not expose a public FOCUS-formatted feed; for very large accounts request a custom usage export from your account team.\n  - name: Allocation\n    description:\
  \ >-\n      Tag seats by department/cost-center via the Admin Portal and reconcile against your HRIS to chargeback by team. Add-ons should be allocated to the function that uses them (e.g., contact-center add-ons to the support BU).\n  - name: Optimization\n    description: >-\n      Right-size seat tier (Core vs Advanced vs Ultra) per persona; reclaim seats for terminated employees promptly; consolidate add-ons where overlapping; renegotiate at renewal once usage data is in hand.\n  - name: Accountability\n    description: >-\n      Designate a contract owner per RingCentral agreement; review monthly invoices against forecast; track international and SMS overages as leading indicators of plan-tier mismatch.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ringcentral/refs/heads/main/finops/ringcentral-finops.yml
sources:
- https://www.ringcentral.com/office/plansandpricing.html
- https://www.ringcentral.com/contact-center/overview.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Communications
- UCaaS
- Voice
- Video
- Contact Center
- FinOps
- Cost Management
- FOCUS
---
