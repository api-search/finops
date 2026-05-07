---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: linkedin-marketing-audience-insights.yml
  format: yaml
  label: LinkedIn Marketing API
  slug: linkedin-marketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkedin/refs/heads/main/openapi/linkedin-marketing-audience-insights.yml
- filename: linkedin-learning-activity-reports.yml
  format: yaml
  label: LinkedIn Learning Solutions
  slug: linkedin-learning-solutions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkedin/refs/heads/main/openapi/linkedin-learning-activity-reports.yml
- filename: linkedin-talent-job-posting.yml
  format: yaml
  label: LinkedIn Talent Solutions
  slug: linkedin-talent-solutions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkedin/refs/heads/main/openapi/linkedin-talent-job-posting.yml
- filename: linkedin-compliance-events.yml
  format: yaml
  label: LinkedIn Compliance Solutions
  slug: linkedin-compliance-solutions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkedin/refs/heads/main/openapi/linkedin-compliance-events.yml
- filename: linkedin-sales-navigator.yml
  format: yaml
  label: LinkedIn Sales Navigator API
  slug: linkedin-sales-navigator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkedin/refs/heads/main/openapi/linkedin-sales-navigator.yml
- filename: linkedin-regulations-data-portability.yml
  format: yaml
  label: LinkedIn Regulatory API
  slug: linkedin-regulatory-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkedin/refs/heads/main/openapi/linkedin-regulations-data-portability.yml
billing_model:
  billingCurrency: USD/EUR/GBP
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Ad Spend
description: 'FOCUS-aligned FinOps for LinkedIn: APIs themselves are free, but they front paid LinkedIn products. Spend lives in three places — ad spend (Marketing API drives Campaign Manager invoices), per-seat subscriptions (Recruiter, Sales Navigator, Learning), and a no-charge consumer surface (Sign In / Share / Verified / Portability).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: LinkedIn Ireland Unlimited Company / LinkedIn Corporation
  ProviderName: LinkedIn
  PublisherName: LinkedIn Corporation
  ServiceCategory: Marketing / Recruiting
  ServiceName: LinkedIn
layout: finops
meters:
- aggregation: sum
  dimensions:
  - ad_account
  - campaign
  - creative
  - objective
  - country
  name: ad_spend
  unit: USD
- aggregation: sum
  dimensions:
  - campaign
  - audience
  name: ad_impressions
  unit: impression
- aggregation: count
  dimensions:
  - contract
  - product_variant
  name: recruiter_seats
  unit: seat
- aggregation: count
  dimensions:
  - contract
  - product_variant
  name: sales_navigator_seats
  unit: seat
- aggregation: count
  dimensions:
  - contract
  name: learning_seats
  unit: seat
- aggregation: sum
  dimensions:
  - api_product
  - endpoint
  - app_tier
  name: api_calls
  unit: request
name: Linkedin Finops
provider_name: LinkedIn
provider_slug: linkedin
publisher_name: LinkedIn Corporation
service_category: Marketing / Recruiting / Professional Networking
slug: linkedin-finops
source_filename: linkedin-finops.yml
source_heading: FinOps Profile
source_url: https://www.linkedin.com/developers/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LinkedIn\nproviderId: linkedin\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Marketing\n  - Recruiting\n  - Sales Enablement\n  - Social Media\ndescription: 'FOCUS-aligned FinOps for LinkedIn: APIs themselves are free, but they front paid LinkedIn\n  products. Spend lives in three places — ad spend (Marketing API drives Campaign Manager invoices),\n  per-seat subscriptions (Recruiter, Sales Navigator, Learning), and a no-charge consumer surface (Sign\n  In / Share / Verified / Portability).'\nsources:\n  - https://www.linkedin.com/developers/products\n  - https://learn.microsoft.com/en-us/linkedin/marketing/quick-start\n  - https://learn.microsoft.com/en-us/linkedin/shared/api-guide/concepts/rate-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: LinkedIn Corporation\nserviceCategory: Marketing / Recruiting / Professional Networking\nbillingModel:\n  pricingCategory: Subscription + Ad Spend\n  billingFrequency: Monthly\n  billingCurrency: USD/EUR/GBP\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: LinkedIn\n  ServiceCategory: Marketing / Recruiting\n  ProviderName: LinkedIn\n  PublisherName: LinkedIn Corporation\n  InvoiceIssuerName: LinkedIn Ireland Unlimited Company / LinkedIn Corporation\n  BillingCurrency: USD\nmeters:\n  - name: ad_spend\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - ad_account\n      - campaign\n      - creative\n      - objective\n      - country\n  - name: ad_impressions\n    unit: impression\n    aggregation: sum\n    dimensions:\n      - campaign\n      - audience\n  - name: recruiter_seats\n\
  \    unit: seat\n    aggregation: count\n    dimensions:\n      - contract\n      - product_variant\n  - name: sales_navigator_seats\n    unit: seat\n    aggregation: count\n    dimensions:\n      - contract\n      - product_variant\n  - name: learning_seats\n    unit: seat\n    aggregation: count\n    dimensions:\n      - contract\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_product\n      - endpoint\n      - app_tier\nprinciples:\n  - name: Visibility\n    description: Use Campaign Manager + Marketing Reporting API for ad spend; LinkedIn Business Manager\n      for invoices; the Developer Portal Analytics tab for per-app / per-endpoint API usage and tier\n      headroom.\n  - name: Allocation\n    description: Tag campaigns, accounts, and Recruiter / Sales Navigator seats with cost-center / business-unit\n      metadata; allocate ad spend by Campaign objective and Recruiter seats by hiring team.\n  - name: Optimization\n    description:\
  \ Use Conversions API to lift attribution and reduce wasted spend; reclaim idle Recruiter\n      / Sales Navigator seats; upgrade apps from Development to Standard tier only when production volume\n      justifies the partner-program effort.\n  - name: Accountability\n    description: Assign one owner per LinkedIn ad account and one per Recruiter / Sales Navigator contract;\n      review monthly seat utilization and CPM / CPC against plan targets.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/linkedin/refs/heads/main/finops/linkedin-finops.yml
sources:
- https://www.linkedin.com/developers/products
- https://learn.microsoft.com/en-us/linkedin/marketing/quick-start
- https://learn.microsoft.com/en-us/linkedin/shared/api-guide/concepts/rate-limits
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Marketing
- Recruiting
- Sales Enablement
- Social Media
---
