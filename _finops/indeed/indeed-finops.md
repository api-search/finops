---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: indeed-employer-api-openapi.yml
  format: yaml
  label: Indeed Job Sync API
  slug: job-sync
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/indeed/refs/heads/main/openapi/indeed-employer-api-openapi.yml
- filename: indeed-employer-api-openapi.yml
  format: yaml
  label: Indeed Employer API
  slug: employer
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/indeed/refs/heads/main/openapi/indeed-employer-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Auction-Priced Advertising
description: FOCUS-aligned FinOps shape for Indeed. The dominant cost line is sponsored-job advertising spend (cost-per-click or pay-per-applicant) consumed through the auction; API access for partners is bundled into partner agreements rather than separately metered. FinOps practice for Indeed therefore focuses on advertising-spend governance, not API-call accounting.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Indeed, Inc.
  PricingCategory: Pay-As-You-Go
  PricingUnit: click
  ProviderName: Indeed
  PublisherName: Indeed, Inc.
  ServiceCategory: Recruiting + Job Advertising
  ServiceName: Indeed Sponsored Jobs
layout: finops
meters:
- aggregation: sum
  description: Clicks on sponsored job postings (CPC model)
  dimensions:
  - requisition
  - department
  - region
  name: sponsored_clicks
  unit: click
- aggregation: sum
  description: Applicants attributed to sponsored placement (PPA model)
  dimensions:
  - requisition
  - department
  - region
  name: sponsored_applicants
  unit: applicant
- aggregation: max
  description: Daily / monthly campaign budgets configured
  dimensions:
  - campaign
  - department
  name: campaign_budget
  unit: USD-day
name: Indeed Finops
provider_name: Indeed
provider_slug: indeed
publisher_name: Indeed, Inc.
service_category: Recruiting + Job Advertising
slug: indeed-finops
source_filename: indeed-finops.yml
source_heading: FinOps Profile
source_url: https://www.indeed.com/hire/how-indeed-works
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Indeed\nproviderId: indeed\npublisherName: Indeed, Inc.\nserviceCategory: Recruiting + Job Advertising\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Careers\n  - Employment\n  - Hiring\n  - Recruiting\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Indeed. The dominant cost line is sponsored-job advertising\n  spend (cost-per-click or pay-per-applicant) consumed through the auction; API access for partners is\n  bundled into partner agreements rather than separately metered. FinOps practice for Indeed therefore\n  focuses on advertising-spend governance, not API-call accounting.\nnotes: API itself\
  \ is not separately billed; the FinOps focus is the advertising auction (CPC/PPA) and\n  the per-applicant economics it produces.\nsources:\n  - https://www.indeed.com/hire/how-indeed-works\n  - https://partners.indeed.com/\nprinciples:\n  - name: Visibility\n    description: Use the Indeed Employer dashboard and Conversion Tracking / Apply API events to see\n      sponsored-job spend, clicks, applies, and hires per requisition.\n  - name: Allocation\n    description: Tag sponsored campaigns by department, requisition, and recruiter so spend can be charged\n      back to the hiring team.\n  - name: Optimization\n    description: Tune daily budgets and bids based on cost-per-applicant and quality-of-applicant signal;\n      pause low-performing campaigns automatically via the Sponsored Jobs API.\n  - name: Accountability\n    description: Designate a recruiting-marketing owner with monthly Indeed-spend budget; review cost-per-hire\n      and cost-per-quality-applicant in monthly hiring\
  \ reviews.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Auction-Priced Advertising\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Indeed Sponsored Jobs\n  ServiceCategory: Recruiting + Job Advertising\n  ProviderName: Indeed\n  PublisherName: Indeed, Inc.\n  InvoiceIssuerName: Indeed, Inc.\n\
  \  PricingCategory: Pay-As-You-Go\n  PricingUnit: click\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: sponsored_clicks\n    description: Clicks on sponsored job postings (CPC model)\n    unit: click\n    aggregation: sum\n    dimensions:\n      - requisition\n      - department\n      - region\n  - name: sponsored_applicants\n    description: Applicants attributed to sponsored placement (PPA model)\n    unit: applicant\n    aggregation: sum\n    dimensions:\n      - requisition\n      - department\n      - region\n  - name: campaign_budget\n    description: Daily / monthly campaign budgets configured\n    unit: USD-day\n    aggregation: max\n    dimensions:\n      - campaign\n      - department\napis:\n  - name: Indeed Job Sync API\n    baseURL: https://apis.indeed.com\n    serviceCategory: API\n  - name: Indeed Disposition Sync API\n    baseURL: https://apis.indeed.com\n    serviceCategory: API\n  - name: Indeed Sponsored Jobs API\n    baseURL: https://apis.indeed.com\n\
  \    serviceCategory: API\n  - name: Indeed Apply API\n    baseURL: https://apis.indeed.com\n    serviceCategory: API\n  - name: Indeed Real-time API\n    baseURL: https://apis.indeed.com\n    serviceCategory: API\n  - name: Indeed Employer API\n    baseURL: https://apis.indeed.com\n    serviceCategory: API\n  - name: Indeed Conversion Tracking API\n    baseURL: https://apis.indeed.com\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Applicant\n    metric: sponsored_spend / sponsored_applicants\n    target: TBD\n  - name: Cost per Hire\n    metric: sponsored_spend / hires\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/indeed/refs/heads/main/finops/indeed-finops.yml
sources:
- https://www.indeed.com/hire/how-indeed-works
- https://partners.indeed.com/
specification: FinOps Framework
tags:
- Careers
- Employment
- Hiring
- Recruiting
- FinOps
- FOCUS
---
