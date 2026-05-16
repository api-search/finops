---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-marketing-cloud-openapi.yml
  format: yaml
  label: Marketing Cloud REST API
  slug: marketing-cloud-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-marketing-cloud/refs/heads/main/openapi/salesforce-marketing-cloud-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps artifact for Salesforce Marketing Cloud. Pricing is gated; meters and principles describe the expected billing surface. Salesforce publishes per-edition pricing on its product pages, but those pages are not retrievable via automated fetch (HTTP 403). All editions are sold via Salesforce Sales; API access is included with the underlying CRM license rather than priced as a discrete API SKU. Treat this artifact as a contact-sales placeholder until pricing pages can be reconciled manually.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Salesforce, Inc.
  ProviderName: Salesforce Marketing Cloud
  PublisherName: Salesforce, Inc.
  ServiceCategory: Marketing Automation
  ServiceName: Salesforce Marketing Cloud
  ServiceSubcategory: Marketing Automation
layout: finops
meters:
- aggregation: sum
  dimensions:
  - edition
  - license_type
  - org
  name: user_subscription
  unit: seat-month
- aggregation: sum
  dimensions:
  - edition
  - org
  - named_credential
  name: api_requests
  unit: request
- aggregation: max
  dimensions:
  - org
  - object
  name: data_storage
  unit: GB-month
- aggregation: max
  dimensions:
  - org
  name: file_storage
  unit: GB-month
name: Salesforce Marketing Cloud Finops
provider_name: Salesforce Marketing Cloud
provider_slug: salesforce-marketing-cloud
publisher_name: Salesforce, Inc.
service_category: Marketing Automation
slug: salesforce-marketing-cloud-finops
source_filename: salesforce-marketing-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://www.salesforce.com/marketing/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Salesforce Marketing Cloud\nproviderId: salesforce-marketing-cloud\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- CRM\n- Email Marketing\n- Marketing Automation\n- Marketing Cloud\n- Personalization\n- FinOps\n- FOCUS\ndescription: FOCUS-aligned FinOps artifact for Salesforce Marketing Cloud. Pricing is gated; meters and\n  principles describe the expected billing surface. Salesforce publishes per-edition pricing on its product\n  pages, but those pages are not retrievable via automated fetch (HTTP 403). All editions are sold via\n  Salesforce Sales; API access is included with the underlying CRM license rather than priced as a discrete\n  API SKU. Treat this artifact as a contact-sales placeholder until pricing pages can be reconciled manually.\nsources:\n- https://www.salesforce.com/marketing/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\n\
  - https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Salesforce, Inc.\nserviceCategory: Marketing Automation\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Tax\n  - Adjustment\n  - Credit\nfocusColumns:\n  ServiceName: Salesforce Marketing Cloud\n  ServiceCategory: Marketing Automation\n  ServiceSubcategory: Marketing Automation\n  ProviderName: Salesforce Marketing Cloud\n  PublisherName: Salesforce, Inc.\n  InvoiceIssuerName: Salesforce, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: user_subscription\n  unit: seat-month\n  aggregation: sum\n  dimensions:\n  - edition\n  - license_type\n  - org\n- name: api_requests\n  unit: request\n\
  \  aggregation: sum\n  dimensions:\n  - edition\n  - org\n  - named_credential\n- name: data_storage\n  unit: GB-month\n  aggregation: max\n  dimensions:\n  - org\n  - object\n- name: file_storage\n  unit: GB-month\n  aggregation: max\n  dimensions:\n  - org\nprinciples:\n- name: Visibility\n  description: Monitor Setup > System Overview for licensed users, API requests over the trailing 24 hours,\n    and data/file storage. Use the Event Monitoring (Shield) API for per-user request telemetry where\n    licensed.\n- name: Allocation\n  description: Tag each consuming integration with a Connected App / Named Credential and attribute API\n    consumption by Connected App in Event Monitoring.\n- name: Optimization\n  description: Reduce API consumption by using Composite, SOQL Query, and Bulk API 2.0 instead of per-record\n    REST calls; right-size editions at renewal; archive to Big Objects to reduce data-storage overage.\n- name: Accountability\n  description: CRM platform owner is accountable\
  \ for per-org consumption and renewal terms; integration\n    owners are accountable for staying within the org-wide 24-hour API quota.\nnotes: Salesforce publishes per-edition pricing on its product pages, but those pages are not retrievable\n  via automated fetch (HTTP 403). All editions are sold via Salesforce Sales; API access is included with\n  the underlying CRM license rather than priced as a discrete API SKU. Treat this artifact as a contact-sales\n  placeholder until pricing pages can be reconciled manually.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-marketing-cloud/refs/heads/main/finops/salesforce-marketing-cloud-finops.yml
sources:
- https://www.salesforce.com/marketing/pricing/
- https://focus.finops.org/focus-specification/v1-3/
- https://www.finops.org/framework/
specification: FinOps Framework
tags:
- CRM
- Email Marketing
- Marketing Automation
- Marketing Cloud
- Personalization
- FinOps
- FOCUS
---
