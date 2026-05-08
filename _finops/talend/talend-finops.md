---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: talend-orchestration-openapi.yml
  format: yaml
  label: Talend Cloud Orchestration API
  slug: talend-orchestration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/talend/refs/heads/main/openapi/talend-orchestration-openapi.yml
- filename: talend-processing-openapi.yml
  format: yaml
  label: Talend Cloud Processing API
  slug: talend-processing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/talend/refs/heads/main/openapi/talend-processing-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Custom / Contact Sales
description: FinOps placeholder for Talend (Qlik). Pricing is custom-quoted; consumption-cost mapping is established at contract time and aligned to the Talend / Qlik subscription line items.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: QlikTech International AB
  ProviderName: Talend
  PublisherName: QlikTech International AB
  ServiceCategory: Data Integration
  ServiceName: Talend
layout: finops
meters:
- aggregation: sum
  name: custom_subscription
  unit: varies
name: Talend Finops
provider_name: Talend
provider_slug: talend
publisher_name: QlikTech International AB
service_category: Data Integration
slug: talend-finops
source_filename: talend-finops.yml
source_heading: FinOps Profile
source_url: https://www.talend.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Talend\nproviderId: talend\npublisherName: QlikTech International AB\nserviceCategory: Data Integration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Data Integration\n  - ETL\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Talend (Qlik). Pricing is custom-quoted; consumption-cost mapping\n  is established at contract time and aligned to the Talend / Qlik subscription line items.\nsources:\n  - https://www.talend.com/\n  - https://www.qlik.com/us/pricing/data-integration-products-pricing\nnotes: No public billing or per-meter pricing list. Meters collapsed to custom engagement pending\n  direct subscription\
  \ details.\nbillingModel:\n  pricingCategory: Custom / Contact Sales\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Talend\n  ServiceCategory: Data Integration\n  ProviderName: Talend\n  PublisherName: QlikTech International AB\n  InvoiceIssuerName: QlikTech International AB\n  BillingCurrency: USD\nmeters:\n  - name: custom_subscription\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Subscription consumption is reported through the Talend / Qlik customer success\n      channel and the product's own usage views; no public usage API ships at the platform level.\n  - name: Allocation\n    description: Allocation is performed against the line items on the customer's Talend / Qlik\n      subscription invoice in the consumer's own ERP.\n  - name: Optimization\n    description: Optimization levers are addressed through pipeline consolidation, schedule tuning,\n \
  \     and subscription right-sizing during renewal cycles.\n  - name: Accountability\n    description: Accountability sits with the data engineering or platform owner holding the\n      Talend / Qlik subscription.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/talend/refs/heads/main/finops/talend-finops.yml
sources:
- https://www.talend.com/
- https://www.qlik.com/us/pricing/data-integration-products-pricing
specification: FinOps Framework
tags:
- Data Integration
- ETL
- FinOps
- FOCUS
---
