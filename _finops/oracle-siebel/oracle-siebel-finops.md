---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.json
  format: json
  label: Oracle Siebel REST API
  slug: oracle-siebel-rest-api
  spec_type: OpenAPI
  url: https://{siebel-server}/siebel/v1.0/swagger.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Per-User / Per-Processor License (BYOL)
description: 'FOCUS-aligned FinOps view for Oracle Siebel CRM: contractual Oracle Applications licenses (per Application User, Component User, or Processor) plus the underlying infrastructure cost (on-premises hardware or OCI compute, block storage, and networking) used to host the Siebel Application Object Manager, Application Server, Web Server, and Database. REST, SOAP, EAI, and Object Interface APIs are bundled with the license.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: License + Support
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: CRM
  ServiceName: Oracle Siebel CRM
layout: finops
meters:
- aggregation: max
  description: Active Application User licenses contracted with Oracle
  dimensions:
  - business_unit
  name: siebel_application_user_license
  unit: user
- aggregation: max
  description: Active Component User licenses contracted with Oracle
  dimensions:
  - component
  - business_unit
  name: siebel_component_user_license
  unit: user
- aggregation: max
  description: Per-processor licenses contracted with Oracle
  dimensions:
  - environment
  name: siebel_per_processor_license
  unit: processor
- aggregation: sum
  description: Annual support and update license fee (typically a percentage of contract value)
  name: support_and_update_license
  unit: usd-annual
- aggregation: sum
  description: Underlying infrastructure compute cost (on-premises or OCI) for the Siebel deployment
  dimensions:
  - environment
  - region
  name: hosting_compute
  unit: ocpu-hour
name: Oracle Siebel Finops
provider_name: Oracle Siebel
provider_slug: oracle-siebel
publisher_name: Oracle America, Inc.
service_category: CRM
slug: oracle-siebel-finops
source_filename: oracle-siebel-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/cx/siebel/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Siebel\nproviderId: oracle-siebel\npublisherName: Oracle America, Inc.\nserviceCategory: CRM\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - CRM\n  - Enterprise Software\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle Siebel CRM: contractual Oracle\n  Applications licenses (per Application User, Component User, or Processor)\n  plus the underlying infrastructure cost (on-premises hardware or OCI\n  compute, block storage, and networking) used to host the Siebel\n  Application Object Manager, Application Server, Web Server, and Database.\n  REST, SOAP, EAI, and\
  \ Object Interface APIs are bundled with the license.\nsources:\n  - https://www.oracle.com/cx/siebel/\n  - https://docs.oracle.com/cd/F26413_01/\nnotes: >-\n  No per-API meter exists. Track contractual license counts per metric and\n  the underlying compute / storage cost for the Siebel deployment; reconcile\n  annually against the Oracle support and update license invoice.\nbillingModel:\n  pricingCategory: Per-User / Per-Processor License (BYOL)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle Siebel CRM\n  ServiceCategory: CRM\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: License + Support\n  ChargeCategory: Purchase\nmeters:\n  - name: siebel_application_user_license\n    description: Active Application User licenses contracted with Oracle\n    unit:\
  \ user\n    aggregation: max\n    dimensions:\n      - business_unit\n  - name: siebel_component_user_license\n    description: Active Component User licenses contracted with Oracle\n    unit: user\n    aggregation: max\n    dimensions:\n      - component\n      - business_unit\n  - name: siebel_per_processor_license\n    description: Per-processor licenses contracted with Oracle\n    unit: processor\n    aggregation: max\n    dimensions:\n      - environment\n  - name: support_and_update_license\n    description: Annual support and update license fee (typically a percentage of contract value)\n    unit: usd-annual\n    aggregation: sum\n  - name: hosting_compute\n    description: Underlying infrastructure compute cost (on-premises or OCI) for the Siebel deployment\n    unit: ocpu-hour\n    aggregation: sum\n    dimensions:\n      - environment\n      - region\nprinciples:\n  - name: Visibility\n    description: >-\n      Maintain a contract-level inventory of Siebel license counts per\n\
  \      metric, plus an infrastructure inventory of the AOM, Application\n      Server, Web Server, and Database tiers; reconcile each annually.\n  - name: Allocation\n    description: >-\n      Tag each Siebel environment (development, test, production, DR) and\n      allocate license + infrastructure cost to the consuming sales,\n      marketing, or service organization.\n  - name: Optimization\n    description: >-\n      Reclaim inactive Application User accounts, retire unused Siebel\n      modules to reduce support fees, and right-size the AOM, Application\n      Server, and Database tiers when migrating to OCI compute.\n  - name: Accountability\n    description: >-\n      Pair the Siebel applications administrator with the customer-experience\n      finance partner; review license utilization annually before the\n      support and update renewal.\napis:\n  - name: Oracle Siebel REST API\n    serviceName: Oracle Siebel REST API\n    serviceCategory: CRM\n  - name: Oracle Siebel SOAP\
  \ Web Services\n    serviceName: Oracle Siebel SOAP Web Services\n    serviceCategory: CRM\n  - name: Oracle Siebel Business Service API\n    serviceName: Oracle Siebel Business Service API\n    serviceCategory: CRM\n  - name: Oracle Siebel EAI (Enterprise Application Integration)\n    serviceName: Oracle Siebel EAI (Enterprise Application Integration)\n    serviceCategory: CRM\n  - name: Oracle Siebel Object Interfaces API\n    serviceName: Oracle Siebel Object Interfaces API\n    serviceCategory: CRM\n  - name: Oracle Siebel Open UI JavaScript API\n    serviceName: Oracle Siebel Open UI JavaScript API\n    serviceCategory: CRM\n  - name: Oracle Siebel Event Pub/Sub API\n    serviceName: Oracle Siebel Event Pub/Sub API\n    serviceCategory: CRM\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-siebel/refs/heads/main/finops/oracle-siebel-finops.yml
sources:
- https://www.oracle.com/cx/siebel/
- https://docs.oracle.com/cd/F26413_01/
specification: FinOps Framework
tags:
- CRM
- Enterprise Software
- Oracle Cloud
- FinOps
- FOCUS
---
