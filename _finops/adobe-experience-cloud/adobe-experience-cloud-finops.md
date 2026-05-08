---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-analytics-api-openapi.yml
  format: yaml
  label: Adobe Analytics 2.0 API
  slug: analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-experience-cloud/refs/heads/main/openapi/adobe-analytics-api-openapi.yml
- filename: adobe-experience-platform-api-openapi.yml
  format: yaml
  label: Adobe Experience Platform API
  slug: experience-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-experience-cloud/refs/heads/main/openapi/adobe-experience-platform-api-openapi.yml
- filename: adobe-target-api-openapi.yml
  format: yaml
  label: Adobe Target API
  slug: target-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-experience-cloud/refs/heads/main/openapi/adobe-target-api-openapi.yml
- filename: adobe-journey-optimizer-api-openapi.yml
  format: yaml
  label: Adobe Journey Optimizer API
  slug: journey-optimizer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-experience-cloud/refs/heads/main/openapi/adobe-journey-optimizer-api-openapi.yml
- filename: adobe-campaign-api-openapi.yml
  format: yaml
  label: Adobe Campaign API
  slug: campaign-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-experience-cloud/refs/heads/main/openapi/adobe-campaign-api-openapi.yml
- filename: adobe-io-events-asyncapi.yml
  format: yaml
  label: Adobe I/O Events
  slug: io-events
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-experience-cloud/refs/heads/main/asyncapi/adobe-io-events-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: 'FOCUS-aligned FinOps shape for Adobe Experience Cloud: enterprise contract licensing across multiple SKUs each keyed to a product-specific commit unit. API access is included with each product license.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Marketing + Analytics + DXP SaaS
  ServiceName: Adobe Experience Cloud
layout: finops
meters:
- aggregation: sum
  description: Adobe Analytics server-call commit
  dimensions:
  - report_suite
  name: server_calls
  unit: server_call
- aggregation: max
  description: Real-Time CDP / Journey Optimizer / Campaign profile commit
  dimensions:
  - sandbox
  - product
  name: addressable_profiles
  unit: profile-month
- aggregation: sum
  description: Customer Journey Analytics analyzable-row commit
  dimensions:
  - dataset
  name: cja_rows
  unit: row
- aggregation: sum
  description: Adobe Target qualified-visitor commit
  dimensions:
  - client-code
  name: target_visitors
  unit: visitor
- aggregation: max
  description: AEM Assets storage and bandwidth (where applicable)
  dimensions:
  - tenant
  name: aem_assets_storage
  unit: GB-month
- aggregation: max
  description: Marketo Engage database size commit
  dimensions:
  - workspace
  name: marketo_database
  unit: contact-month
- aggregation: sum
  description: Adobe Workfront named-user licenses
  dimensions:
  - role
  name: workfront_seats
  unit: seat-month
- aggregation: sum
  description: Adobe Commerce GMV-tiered commit
  dimensions:
  - storefront
  name: commerce_gmv
  unit: USD
name: Adobe Experience Cloud Finops
provider_name: Adobe Experience Cloud
provider_slug: adobe-experience-cloud
publisher_name: Adobe Inc.
service_category: Marketing + Analytics + DXP SaaS
slug: adobe-experience-cloud-finops
source_filename: adobe-experience-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://business.adobe.com/products/experience-cloud-products.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Experience Cloud\nproviderId: adobe-experience-cloud\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Experience Cloud\n  - Customer Data Platform\n  - Analytics\nnotes: >-\n  Experience Cloud spans many enterprise SKUs (Analytics, Real-Time CDP,\n  Target, Journey Optimizer, AEM, Marketo, Workfront, Commerce); each has\n  its own commit unit (server calls, profiles, MAUs, GMV, seats). FinOps\n  levers focus on commit / overage management across the bundle.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe Experience Cloud: enterprise\n  contract licensing across multiple SKUs each keyed to a product-specific\n  commit unit. API access is included with each product license.\nsources:\n  - https://business.adobe.com/products/experience-cloud-products.html\n  - https://developer.adobe.com/experience-platform-apis/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\nserviceCategory: Marketing + Analytics + DXP SaaS\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Adobe Experience Cloud\n  ServiceCategory: Marketing + Analytics + DXP SaaS\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: server_calls\n    description: Adobe Analytics server-call commit\n    unit: server_call\n    aggregation: sum\n    dimensions:\n      - report_suite\n  - name: addressable_profiles\n    description: Real-Time CDP / Journey Optimizer / Campaign profile commit\n    unit:\
  \ profile-month\n    aggregation: max\n    dimensions:\n      - sandbox\n      - product\n  - name: cja_rows\n    description: Customer Journey Analytics analyzable-row commit\n    unit: row\n    aggregation: sum\n    dimensions:\n      - dataset\n  - name: target_visitors\n    description: Adobe Target qualified-visitor commit\n    unit: visitor\n    aggregation: sum\n    dimensions:\n      - client-code\n  - name: aem_assets_storage\n    description: AEM Assets storage and bandwidth (where applicable)\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: marketo_database\n    description: Marketo Engage database size commit\n    unit: contact-month\n    aggregation: max\n    dimensions:\n      - workspace\n  - name: workfront_seats\n    description: Adobe Workfront named-user licenses\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - role\n  - name: commerce_gmv\n    description: Adobe Commerce GMV-tiered commit\n    unit: USD\n   \
  \ aggregation: sum\n    dimensions:\n      - storefront\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Adobe Experience Platform Sandbox dashboard, Analytics Server\n      Call Usage report, Target Activations report, and AEM Assets storage\n      meter to track each commit unit against contract.\n  - name: Allocation\n    description: >-\n      Use sandbox-per-business-unit naming, report-suite-per-property, and\n      Marketo workspace partitions to attribute Experience Cloud spend to\n      business owners.\n  - name: Optimization\n    description: >-\n      Right-size commit at renewal; archive unused datasets in Real-Time CDP;\n      consolidate duplicate Target activities; deprecate stale Marketo\n      programs; review AEM asset retention to control storage.\n  - name: Accountability\n    description: >-\n      Adobe TAM / CSM run quarterly business reviews against each product's\n      commit; finance owns true-up reconciliation and overage billing at\n\
  \      year-end.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-experience-cloud/refs/heads/main/finops/adobe-experience-cloud-finops.yml
sources:
- https://business.adobe.com/products/experience-cloud-products.html
- https://developer.adobe.com/experience-platform-apis/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Experience Cloud
- Customer Data Platform
- Analytics
---
