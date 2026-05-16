---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-net-zero-cloud-rest-api-openapi.yml
  format: yaml
  label: Net Zero Cloud REST API
  slug: net-zero-cloud-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-net-zero-cloud/refs/heads/main/openapi/salesforce-net-zero-cloud-rest-api-openapi.yml
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
description: FOCUS-aligned FinOps artifact for Salesforce Net Zero Cloud. Pricing is gated; meters and principles describe the expected billing surface. Salesforce publishes per-edition pricing on its product pages, but those pages are not retrievable via automated fetch (HTTP 403). All editions are sold via Salesforce Sales; API access is included with the underlying CRM license rather than priced as a discrete API SKU. Treat this artifact as a contact-sales placeholder until pricing pages can be reconciled manually.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Salesforce, Inc.
  ProviderName: Salesforce Net Zero Cloud
  PublisherName: Salesforce, Inc.
  ServiceCategory: Sustainability / ESG
  ServiceName: Salesforce Net Zero Cloud
  ServiceSubcategory: Sustainability Reporting
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
name: Salesforce Net Zero Cloud Finops
provider_name: Salesforce Net Zero Cloud
provider_slug: salesforce-net-zero-cloud
publisher_name: Salesforce, Inc.
service_category: Sustainability / ESG
slug: salesforce-net-zero-cloud-finops
source_filename: salesforce-net-zero-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://www.salesforce.com/sustainability/net-zero-cloud/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Salesforce Net Zero Cloud\nproviderId: salesforce-net-zero-cloud\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- CRM\n- ESG\n- Net Zero\n- Salesforce\n- Sustainability\n- FinOps\n- FOCUS\ndescription: FOCUS-aligned FinOps artifact for Salesforce Net Zero Cloud. Pricing is gated; meters and\n  principles describe the expected billing surface. Salesforce publishes per-edition pricing on its product\n  pages, but those pages are not retrievable via automated fetch (HTTP 403). All editions are sold via\n  Salesforce Sales; API access is included with the underlying CRM license rather than priced as a discrete\n  API SKU. Treat this artifact as a contact-sales placeholder until pricing pages can be reconciled manually.\nsources:\n- https://www.salesforce.com/sustainability/net-zero-cloud/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\n\
  - https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Salesforce, Inc.\nserviceCategory: Sustainability / ESG\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Tax\n  - Adjustment\n  - Credit\nfocusColumns:\n  ServiceName: Salesforce Net Zero Cloud\n  ServiceCategory: Sustainability / ESG\n  ServiceSubcategory: Sustainability Reporting\n  ProviderName: Salesforce Net Zero Cloud\n  PublisherName: Salesforce, Inc.\n  InvoiceIssuerName: Salesforce, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: user_subscription\n  unit: seat-month\n  aggregation: sum\n  dimensions:\n  - edition\n  - license_type\n  - org\n- name: api_requests\n  unit: request\n\
  \  aggregation: sum\n  dimensions:\n  - edition\n  - org\n  - named_credential\n- name: data_storage\n  unit: GB-month\n  aggregation: max\n  dimensions:\n  - org\n  - object\n- name: file_storage\n  unit: GB-month\n  aggregation: max\n  dimensions:\n  - org\nprinciples:\n- name: Visibility\n  description: Monitor Setup > System Overview for licensed users, API requests over the trailing 24 hours,\n    and data/file storage. Use the Event Monitoring (Shield) API for per-user request telemetry where\n    licensed.\n- name: Allocation\n  description: Tag each consuming integration with a Connected App / Named Credential and attribute API\n    consumption by Connected App in Event Monitoring.\n- name: Optimization\n  description: Reduce API consumption by using Composite, SOQL Query, and Bulk API 2.0 instead of per-record\n    REST calls; right-size editions at renewal; archive to Big Objects to reduce data-storage overage.\n- name: Accountability\n  description: CRM platform owner is accountable\
  \ for per-org consumption and renewal terms; integration\n    owners are accountable for staying within the org-wide 24-hour API quota.\nnotes: Salesforce publishes per-edition pricing on its product pages, but those pages are not retrievable\n  via automated fetch (HTTP 403). All editions are sold via Salesforce Sales; API access is included with\n  the underlying CRM license rather than priced as a discrete API SKU. Treat this artifact as a contact-sales\n  placeholder until pricing pages can be reconciled manually.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-net-zero-cloud/refs/heads/main/finops/salesforce-net-zero-cloud-finops.yml
sources:
- https://www.salesforce.com/sustainability/net-zero-cloud/pricing/
- https://focus.finops.org/focus-specification/v1-3/
- https://www.finops.org/framework/
specification: FinOps Framework
tags:
- CRM
- ESG
- Net Zero
- Salesforce
- Sustainability
- FinOps
- FOCUS
---
