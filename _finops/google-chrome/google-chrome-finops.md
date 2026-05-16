---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-chrome-management-api-openapi.json
  format: json
  label: Chrome Management API
  slug: chrome-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-chrome/refs/heads/main/openapi/google-chrome-management-api-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (Premium) / One-Time (Webstore)
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: Subscription + One-Time
description: 'FOCUS-aligned FinOps for Chrome: the developer-platform surface is free, with two narrow paid lines - the one-time $5 Chrome Web Store developer registration and the $6/user/month Chrome Enterprise Premium subscription. Premium invoicing flows through Google Workspace billing; CrUX/PageSpeed Insights API costs are zero.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Google LLC
  ProviderName: Google
  PublisherName: Google LLC
  ServiceCategory: Browser / Endpoint Management
  ServiceName: Chrome / Chrome Enterprise
layout: finops
meters:
- aggregation: max
  description: Active Chrome Enterprise Premium licensed users
  dimensions:
  - org_unit
  - region
  name: chrome_enterprise_premium_seats
  unit: seat-month
- aggregation: count
  description: Chrome Web Store developer account one-time fee
  dimensions:
  - publisher
  name: webstore_developer_registration
  unit: account
- aggregation: sum
  description: Cloud-billed CrUX API requests (free at default quota)
  dimensions:
  - api_key
  - origin
  name: crux_api_requests
  unit: request
- aggregation: sum
  description: Cloud-billed PageSpeed Insights API requests
  dimensions:
  - api_key
  name: pagespeed_api_requests
  unit: request
name: Google Chrome Finops
provider_name: Google Chrome
provider_slug: google-chrome
publisher_name: Google LLC
service_category: Browser / Developer Tools
slug: google-chrome-finops
source_filename: google-chrome-finops.yml
source_heading: FinOps Profile
source_url: https://chromeenterprise.google/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Chrome\nproviderId: google-chrome\npublisherName: Google LLC\nserviceCategory: Browser / Developer Tools\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Browser\n  - Chrome Extensions\n  - Developer Tools\n  - Web Platform\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Chrome: the developer-platform surface is free, with two narrow\n  paid lines - the one-time $5 Chrome Web Store developer registration and the $6/user/month Chrome Enterprise\n  Premium subscription. Premium invoicing flows through Google Workspace billing; CrUX/PageSpeed Insights\n  API costs are zero.'\nsources:\n  - https://chromeenterprise.google/pricing/\n\
  \  - https://developer.chrome.com/docs/webstore/register\n  - https://workspace.google.com/pricing\nbillingModel:\n  pricingCategory: Subscription + One-Time\n  billingFrequency: Monthly (Premium) / One-Time (Webstore)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: Chrome / Chrome Enterprise\n  ServiceCategory: Browser / Endpoint Management\n  ProviderName: Google\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: chrome_enterprise_premium_seats\n    description: Active Chrome Enterprise Premium licensed users\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - org_unit\n      - region\n  - name: webstore_developer_registration\n    description: Chrome Web Store developer account one-time fee\n    unit: account\n    aggregation: count\n    dimensions:\n      - publisher\n  - name: crux_api_requests\n    description: Cloud-billed CrUX\
  \ API requests (free at default quota)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - origin\n  - name: pagespeed_api_requests\n    description: Cloud-billed PageSpeed Insights API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\napis:\n  - name: Chrome Extensions API\n    baseURL: chrome://extensions/\n    serviceName: Chrome Extensions API\n    serviceCategory: Browser\n  - name: Chrome User Experience (CrUX) API\n    baseURL: https://chromeuxreport.googleapis.com\n    serviceName: CrUX API\n    serviceCategory: Web Performance\n  - name: PageSpeed Insights API\n    baseURL: https://pagespeedonline.googleapis.com\n    serviceName: PageSpeed Insights API\n    serviceCategory: Web Performance\n  - name: Chrome Web Store Publish API\n    baseURL: https://www.googleapis.com/chromewebstore\n    serviceName: Chrome Web Store Publish API\n    serviceCategory: Distribution\nprinciples:\n  - name: Visibility\n    description:\
  \ For Chrome Enterprise Premium, view per-seat consumption in the Google Workspace Admin\n      console subscriptions page; for the CrUX/PageSpeed Insights APIs, monitor request volume in the\n      Google Cloud Console.\n  - name: Allocation\n    description: Allocate Premium seats by org-unit (department/team) in the Admin console; tag CrUX/PageSpeed\n      API keys per consuming team for per-team usage attribution.\n  - name: Optimization\n    description: Reclaim inactive Premium seats monthly using the Admin console's last-active reports;\n      cache CrUX results since underlying data updates only weekly/monthly; consolidate CrUX/PageSpeed\n      API keys to share quota across teams.\n  - name: Accountability\n    description: Assign a license owner per organizational unit; review Premium seat utilization quarterly\n      and right-size; the Webstore registration is a sunk one-time cost owned by the publisher account\n      holder.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-chrome/refs/heads/main/finops/google-chrome-finops.yml
sources:
- https://chromeenterprise.google/pricing/
- https://developer.chrome.com/docs/webstore/register
- https://workspace.google.com/pricing
specification: FinOps Framework
tags:
- Browser
- Chrome Extensions
- Developer Tools
- Web Platform
- FinOps
- FOCUS
---
