---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: qlik-sense-enterprise-repository-service-openapi.yml
  format: yaml
  label: Qlik Sense Repository Service
  slug: qlik-sense-repository-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-repository-service-openapi.yml
- filename: qlik-sense-enterprise-proxy-service-openapi.yml
  format: yaml
  label: Qlik Sense Proxy Service
  slug: qlik-sense-proxy-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-proxy-service-openapi.yml
- filename: qlik-sense-enterprise-about-service-openapi.yml
  format: yaml
  label: Qlik Sense About Service
  slug: qlik-sense-about-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-about-service-openapi.yml
- filename: qlik-sense-enterprise-data-connection-openapi.yml
  format: yaml
  label: Qlik Sense Data Connection
  slug: qlik-sense-data-connection
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-data-connection-openapi.yml
- filename: qlik-sense-enterprise-licenses-openapi.yml
  format: yaml
  label: Qlik Sense Licenses
  slug: qlik-sense-licenses
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-licenses-openapi.yml
- filename: qlik-sense-enterprise-odag-service-openapi.yml
  format: yaml
  label: Qlik Sense ODAG
  slug: qlik-sense-odag
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-odag-service-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Enterprise License
description: FOCUS-aligned FinOps for Qlik Sense Enterprise is bound to the platform license rather than per-API metering; usage data is collected inside the customer's Qlik deployment.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Qlik
  ProviderName: Qlik
  PublisherName: Qlik
  ServiceCategory: Analytics
  ServiceName: Qlik Sense Enterprise
layout: finops
meters:
- aggregation: sum
  description: Qlik Sense Enterprise platform license; billed per the customer's negotiated contract.
  dimensions:
  - contract
  name: platform_license
  unit: varies
name: Qlik Sense Enterprise Finops
provider_name: Qlik Sense Enterprise
provider_slug: qlik-sense-enterprise
publisher_name: Qlik
service_category: Analytics
slug: qlik-sense-enterprise-finops
source_filename: qlik-sense-enterprise-finops.yml
source_heading: FinOps Profile
source_url: https://www.qlik.com/us/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Qlik Sense Enterprise\nproviderId: qlik-sense-enterprise\npublisherName: Qlik\nserviceCategory: Analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Analytics\n  - Business Intelligence\n  - FinOps\n  - FOCUS\nnotes: Qlik Sense Enterprise is a license-based on-premises analytics platform; Qlik does not publish\n  per-API meter pricing or usage telemetry on its public site. FinOps mapping is left at the platform\n  license level until the customer contract terms are reconciled.\ndescription: FOCUS-aligned FinOps for Qlik Sense Enterprise is bound to the platform license rather\n  than per-API metering; usage data\
  \ is collected inside the customer's Qlik deployment.\nsources:\n  - https://www.qlik.com/us/pricing\nbillingModel:\n  pricingCategory: Enterprise License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Qlik Sense Enterprise\n  ServiceCategory: Analytics\n  ProviderName: Qlik\n  PublisherName: Qlik\n  InvoiceIssuerName: Qlik\n  BillingCurrency: USD\nmeters:\n  - name: platform_license\n    description: Qlik Sense Enterprise platform license; billed per the customer's negotiated contract.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Qlik Sense Enterprise emits internal usage telemetry through the Qlik Management Console\n      and the QMC logs; consumers must collect this data inside their own deployment.\n  - name: Allocation\n    description: Allocate platform license cost against the analytics teams and business units consuming\n \
  \     Qlik dashboards; sub-allocation within the platform requires custom tagging on apps and streams.\n  - name: Optimization\n    description: Right-size the Qlik deployment (engine memory, proxy capacity) and consolidate streams\n      and apps to keep license consumption inside the contracted capacity.\n  - name: Accountability\n    description: License renewal and capacity expansion are owned by the analytics platform team; engage\n      Qlik sales for true-up or downgrade conversations.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/finops/qlik-sense-enterprise-finops.yml
sources:
- https://www.qlik.com/us/pricing
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- FinOps
- FOCUS
---
