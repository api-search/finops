---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-weblogic-management-openapi.yml
  format: yaml
  label: WebLogic RESTful Management Services API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-weblogic/refs/heads/main/openapi/oracle-weblogic-management-openapi.yml
- filename: oracle-weblogic-monitoring-openapi.yml
  format: yaml
  label: WebLogic Monitoring and Diagnostics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-weblogic/refs/heads/main/openapi/oracle-weblogic-monitoring-openapi.yml
- filename: oracle-weblogic-deployment-openapi.yml
  format: yaml
  label: WebLogic Deployment API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-weblogic/refs/heads/main/openapi/oracle-weblogic-deployment-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: BYOL + License-Included (OCI Compute)
description: 'FOCUS-aligned FinOps view for Oracle WebLogic Server: contractual Oracle Technology licenses (per-processor or NUP, by edition Standard / Enterprise / Suite) plus the underlying infrastructure cost (on-premises hardware, OCI compute with WebLogic Marketplace license-included or BYOL, block storage, egress). Management and application APIs are bundled with the license.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: License + Usage
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: Application Server / Middleware
  ServiceName: Oracle WebLogic Server
layout: finops
meters:
- aggregation: max
  description: Per-processor WebLogic licenses contracted with Oracle
  dimensions:
  - edition
  - environment
  name: weblogic_per_processor_license
  unit: processor
- aggregation: max
  description: Named User Plus WebLogic licenses contracted with Oracle
  dimensions:
  - edition
  - environment
  name: weblogic_named_user_plus_license
  unit: user
- aggregation: sum
  description: OCPU-hours consumed by WebLogic Marketplace stacks with included license
  dimensions:
  - edition
  - region
  - tag
  name: weblogic_oci_ocpu_hours_license_included
  unit: ocpu-hour
- aggregation: sum
  description: OCPU-hours consumed by BYOL WebLogic deployments on OCI compute
  dimensions:
  - region
  - shape
  - tag
  name: oci_compute_ocpu_hours
  unit: ocpu-hour
- aggregation: sum
  description: Block storage attached to WebLogic hosts
  dimensions:
  - region
  - tag
  name: oci_block_storage_gb_month
  unit: GB-month
- aggregation: sum
  description: Annual support and update license fee for on-premises WebLogic
  name: support_and_update_license
  unit: usd-annual
name: Oracle Weblogic Finops
provider_name: Oracle WebLogic Server
provider_slug: oracle-weblogic
publisher_name: Oracle America, Inc.
service_category: Application Server / Middleware
slug: oracle-weblogic-finops
source_filename: oracle-weblogic-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/java/weblogic/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle WebLogic Server\nproviderId: oracle-weblogic\npublisherName: Oracle America, Inc.\nserviceCategory: Application Server / Middleware\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Server\n  - Java EE\n  - Middleware\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle WebLogic Server: contractual Oracle\n  Technology licenses (per-processor or NUP, by edition Standard / Enterprise /\n  Suite) plus the underlying infrastructure cost (on-premises hardware, OCI\n  compute with WebLogic Marketplace license-included or BYOL, block storage,\n  egress). Management\
  \ and application APIs are bundled with the license.\nsources:\n  - https://www.oracle.com/java/weblogic/\n  - https://docs.oracle.com/en/middleware/standalone/weblogic-server/\n  - https://www.oracle.com/cloud/price-list/\nnotes: >-\n  No per-API meter exists. Track contractual license counts per edition and\n  metric, plus underlying OCI / on-premises infrastructure cost for the\n  WebLogic deployment; reconcile annually against the Oracle support and\n  update license invoice.\nbillingModel:\n  pricingCategory: BYOL + License-Included (OCI Compute)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle WebLogic Server\n  ServiceCategory: Application Server / Middleware\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: License + Usage\n  ChargeCategory: Purchase\n\
  meters:\n  - name: weblogic_per_processor_license\n    description: Per-processor WebLogic licenses contracted with Oracle\n    unit: processor\n    aggregation: max\n    dimensions:\n      - edition\n      - environment\n  - name: weblogic_named_user_plus_license\n    description: Named User Plus WebLogic licenses contracted with Oracle\n    unit: user\n    aggregation: max\n    dimensions:\n      - edition\n      - environment\n  - name: weblogic_oci_ocpu_hours_license_included\n    description: OCPU-hours consumed by WebLogic Marketplace stacks with included license\n    unit: ocpu-hour\n    aggregation: sum\n    dimensions:\n      - edition\n      - region\n      - tag\n  - name: oci_compute_ocpu_hours\n    description: OCPU-hours consumed by BYOL WebLogic deployments on OCI compute\n    unit: ocpu-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - shape\n      - tag\n  - name: oci_block_storage_gb_month\n    description: Block storage attached to WebLogic hosts\n\
  \    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - tag\n  - name: support_and_update_license\n    description: Annual support and update license fee for on-premises WebLogic\n    unit: usd-annual\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Use OCI Cost Analysis with cost-tracking tags applied to each\n      WebLogic Marketplace stack and BYOL compute instance; reconcile\n      annually against the Oracle Technology license count and support\n      renewal invoice.\n  - name: Allocation\n    description: >-\n      Tag each WebLogic environment (dev, test, prod, DR) and allocate\n      license + infrastructure cost to the consuming application or\n      product team.\n  - name: Optimization\n    description: >-\n      Right-size managed-server JVM heaps and OCPU shapes to actual\n      throughput, consolidate low-traffic applications onto shared domains\n      where licensing terms permit, prefer BYOL on OCI when existing\n\
  \      license entitlement is available, and schedule non-production\n      instances to stop outside business hours.\n  - name: Accountability\n    description: >-\n      Pair the WebLogic platform owner with the Java applications team and\n      a finance partner; review license utilization and OCI consumption\n      monthly, and the Oracle support and update renewal annually.\napis:\n  - name: WebLogic RESTful Management Services API\n    serviceName: WebLogic RESTful Management Services API\n    serviceCategory: Application Server / Middleware\n  - name: WebLogic Monitoring and Diagnostics API\n    serviceName: WebLogic Monitoring and Diagnostics API\n    serviceCategory: Application Server / Middleware\n  - name: WebLogic Deployment API\n    serviceName: WebLogic Deployment API\n    serviceCategory: Application Server / Middleware\n  - name: WebLogic WLST (WebLogic Scripting Tool) API\n    serviceName: WebLogic WLST (WebLogic Scripting Tool) API\n    serviceCategory: Application Server\
  \ / Middleware\n  - name: WebLogic JMX API\n    serviceName: WebLogic JMX API\n    serviceCategory: Application Server / Middleware\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-weblogic/refs/heads/main/finops/oracle-weblogic-finops.yml
sources:
- https://www.oracle.com/java/weblogic/
- https://docs.oracle.com/en/middleware/standalone/weblogic-server/
- https://www.oracle.com/cloud/price-list/
specification: FinOps Framework
tags:
- Application Server
- Java EE
- Middleware
- Oracle Cloud
- FinOps
- FOCUS
---
