---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: brevo-transactional-email-openapi.yml
  format: yaml
  label: Brevo Transactional Email API
  slug: transactional-email-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/openapi/brevo-transactional-email-openapi.yml
- filename: brevo-email-campaigns-openapi.yml
  format: yaml
  label: Brevo Email Campaigns API
  slug: email-campaigns-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/openapi/brevo-email-campaigns-openapi.yml
- filename: brevo-contacts-openapi.yml
  format: yaml
  label: Brevo Contacts API
  slug: contacts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/openapi/brevo-contacts-openapi.yml
- filename: brevo-transactional-sms-openapi.yml
  format: yaml
  label: Brevo Transactional SMS API
  slug: transactional-sms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/openapi/brevo-transactional-sms-openapi.yml
- filename: brevo-whatsapp-openapi.yml
  format: yaml
  label: Brevo WhatsApp API
  slug: whatsapp-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/openapi/brevo-whatsapp-openapi.yml
- filename: brevo-ecommerce-openapi.yml
  format: yaml
  label: Brevo eCommerce API
  slug: ecommerce-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/openapi/brevo-ecommerce-openapi.yml
- filename: brevo-conversations-openapi.yml
  format: yaml
  label: Brevo Conversations API
  slug: conversations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/openapi/brevo-conversations-openapi.yml
- filename: brevo-webhooks-openapi.yml
  format: yaml
  label: Brevo Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/openapi/brevo-webhooks-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription (volume-based)
description: 'FOCUS-aligned FinOps for Brevo: tiered subscription priced on monthly email send volume, with up to 100K contacts allowed across plans. Free tier caps daily sends at 300; paid tiers (Starter, Business) scale subscription cost with chosen email volume; BrevoPlus / Enterprise is custom-priced.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sendinblue SAS
  PricingCategory: Standard
  PricingUnit: subscription-month
  ProviderName: Brevo
  PublisherName: Sendinblue SAS
  ServiceCategory: Email & Marketing Automation
  ServiceName: Brevo
layout: finops
meters:
- aggregation: sum
  description: Plan subscription fee billed monthly. Price scales with the chosen email volume tier.
  dimensions:
  - plan
  - email_volume_tier
  - billing_cycle
  name: subscription_month
  unit: month
- aggregation: sum
  description: Marketing and transactional emails sent against the plan's monthly volume.
  dimensions:
  - email_type
  - campaign
  name: emails_sent
  unit: email
- aggregation: sum
  description: Transactional and marketing SMS sent; billed per SMS per destination country.
  dimensions:
  - country
  - message_type
  name: sms_sent
  unit: message
- aggregation: max
  description: Stored contacts on the account.
  dimensions:
  - list
  name: contacts
  unit: contact
- aggregation: max
  description: Contacts engaged through marketing automation; capped at 2K on Free.
  dimensions:
  - workflow
  name: automation_contacts
  unit: contact
name: Brevo Finops
provider_name: brevo
provider_slug: brevo
publisher_name: Sendinblue SAS (Brevo)
service_category: Email & Marketing Automation
slug: brevo-finops
source_filename: brevo-finops.yml
source_heading: FinOps Profile
source_url: https://www.brevo.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Brevo\nproviderId: brevo\npublisherName: Sendinblue SAS (Brevo)\nserviceCategory: Email & Marketing Automation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Email\n  - Transactional\n  - SMS\n  - Marketing\n  - CRM\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Brevo: tiered subscription priced on monthly email send volume,\n  with up to 100K contacts allowed across plans. Free tier caps daily sends at 300; paid tiers (Starter,\n  Business) scale subscription cost with chosen email volume; BrevoPlus / Enterprise is custom-priced.'\nsources:\n  - https://www.brevo.com/pricing/\n  - https://developers.brevo.com/docs/api-limits\n\
  billingModel:\n  pricingCategory: Tiered Subscription (volume-based)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Brevo\n  ServiceCategory: Email & Marketing Automation\n  ProviderName: Brevo\n  PublisherName: Sendinblue SAS\n  InvoiceIssuerName: Sendinblue SAS\n  BillingCurrency: USD\n  PricingCategory: Standard\n  PricingUnit: subscription-month\nmeters:\n  - name: subscription_month\n    description: Plan subscription fee billed monthly. Price scales with the chosen email volume tier.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - email_volume_tier\n      - billing_cycle\n  - name: emails_sent\n    description: Marketing and transactional emails sent against the plan's monthly volume.\n    unit: email\n    aggregation: sum\n    dimensions:\n      - email_type\n      - campaign\n  - name: sms_sent\n    description: Transactional and marketing\
  \ SMS sent; billed per SMS per destination country.\n    unit: message\n    aggregation: sum\n    dimensions:\n      - country\n      - message_type\n  - name: contacts\n    description: Stored contacts on the account.\n    unit: contact\n    aggregation: max\n    dimensions:\n      - list\n  - name: automation_contacts\n    description: Contacts engaged through marketing automation; capped at 2K on Free.\n    unit: contact\n    aggregation: max\n    dimensions:\n      - workflow\nprinciples:\n  - name: Visibility\n    description: Pull send-volume, deliverability, and SMS country breakdowns from the Brevo dashboard\n      and the statistics API; reconcile monthly against the chosen email-volume tier.\n  - name: Allocation\n    description: Tag campaigns and transactional templates with the consuming product / brand; use sub-accounts\n      where available so subscription fees can be split.\n  - name: Optimization\n    description: Choose the smallest email-volume tier that fits actual\
  \ sends, suppress inactive contacts\n      to keep within tier limits, and prefer transactional SMTP for triggered messages over marketing\n      sends. Annual billing pricing is sometimes available; large 100K+ senders should compare Starter\n      vs Business at their volume.\n  - name: Accountability\n    description: Designate a messaging-platform owner; alert when daily / monthly send approaches tier\n      cap, and revisit BrevoPlus negotiation at sustained 1M+ send volumes.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/brevo/refs/heads/main/finops/brevo-finops.yml
sources:
- https://www.brevo.com/pricing/
- https://developers.brevo.com/docs/api-limits
specification: FinOps Framework
tags:
- Email
- Transactional
- SMS
- Marketing
- CRM
- FinOps
- FOCUS
---
