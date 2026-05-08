---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-goldengate-rest-api-openapi.yml
  format: yaml
  label: Oracle GoldenGate REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-goldengate/refs/heads/main/openapi/oracle-goldengate-rest-api-openapi.yml
- filename: oracle-goldengate-big-data-rest-api-openapi.yml
  format: yaml
  label: Oracle GoldenGate for Big Data REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-goldengate/refs/heads/main/openapi/oracle-goldengate-big-data-rest-api-openapi.yml
- filename: oracle-goldengate-veridata-rest-api-openapi.yml
  format: yaml
  label: Oracle GoldenGate Veridata REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-goldengate/refs/heads/main/openapi/oracle-goldengate-veridata-rest-api-openapi.yml
- filename: oracle-goldengate-cloud-service-api-openapi.yml
  format: yaml
  label: Oracle GoldenGate Cloud Service API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-goldengate/refs/heads/main/openapi/oracle-goldengate-cloud-service-api-openapi.yml
- filename: oracle-goldengate-stream-analytics-rest-api-openapi.yml
  format: yaml
  label: Oracle GoldenGate Stream Analytics REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-goldengate/refs/heads/main/openapi/oracle-goldengate-stream-analytics-rest-api-openapi.yml
- filename: oracle-goldengate-data-streams-rest-api-openapi.yml
  format: yaml
  label: Oracle GoldenGate Data Streams REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-goldengate/refs/heads/main/openapi/oracle-goldengate-data-streams-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go (OCI) + BYOL (On-Premises)
description: 'FOCUS-aligned FinOps view for Oracle GoldenGate: OCI managed service billing per OCPU-hour by edition, plus separate OCI block storage and egress meters for trail files and replicated data; on-premises deployments are billed against the contractual Oracle Technology license. FinOps observation focuses on edition-OCPU utilization and replication egress.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: Pay-As-You-Go
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: Data Integration
  ServiceName: Oracle GoldenGate
layout: finops
meters:
- aggregation: sum
  description: OCPU-hours consumed by OCI GoldenGate deployments
  dimensions:
  - edition
  - region
  - deployment
  - tag
  name: goldengate_ocpu_hours
  unit: ocpu-hour
- aggregation: sum
  description: Block storage attached to GoldenGate deployments for trail files
  dimensions:
  - region
  - deployment
  name: goldengate_trail_storage_gb_month
  unit: GB-month
- aggregation: sum
  description: Outbound data transfer from GoldenGate deployments to remote targets
  dimensions:
  - region
  - target_type
  name: goldengate_egress_gb
  unit: GB
- aggregation: max
  description: Contractual Oracle Technology license for on-premises GoldenGate
  dimensions:
  - license_type
  name: goldengate_on_prem_license
  unit: license
name: Oracle Goldengate Finops
provider_name: Oracle GoldenGate
provider_slug: oracle-goldengate
publisher_name: Oracle America, Inc.
service_category: Data Integration
slug: oracle-goldengate-finops
source_filename: oracle-goldengate-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/integration/goldengate/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle GoldenGate\nproviderId: oracle-goldengate\npublisherName: Oracle America, Inc.\nserviceCategory: Data Integration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - CDC\n  - Data Integration\n  - Real-Time Replication\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle GoldenGate: OCI managed service\n  billing per OCPU-hour by edition, plus separate OCI block storage and\n  egress meters for trail files and replicated data; on-premises deployments\n  are billed against the contractual Oracle Technology license. FinOps\n  observation focuses on edition-OCPU utilization\
  \ and replication egress.\nsources:\n  - https://www.oracle.com/integration/goldengate/\n  - https://docs.oracle.com/en/cloud/paas/goldengate-service/\n  - https://www.oracle.com/cloud/price-list/\nnotes: >-\n  No public per-API meter exists. Track OCPU-hour consumption per GoldenGate\n  edition through OCI Cost Analysis, plus block storage and egress for trail\n  files and outbound replication.\nbillingModel:\n  pricingCategory: Pay-As-You-Go (OCI) + BYOL (On-Premises)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle GoldenGate\n  ServiceCategory: Data Integration\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: Pay-As-You-Go\n  ChargeCategory: Usage\nmeters:\n  - name: goldengate_ocpu_hours\n    description: OCPU-hours consumed by OCI GoldenGate deployments\n\
  \    unit: ocpu-hour\n    aggregation: sum\n    dimensions:\n      - edition\n      - region\n      - deployment\n      - tag\n  - name: goldengate_trail_storage_gb_month\n    description: Block storage attached to GoldenGate deployments for trail files\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - deployment\n  - name: goldengate_egress_gb\n    description: Outbound data transfer from GoldenGate deployments to remote targets\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - target_type\n  - name: goldengate_on_prem_license\n    description: Contractual Oracle Technology license for on-premises GoldenGate\n    unit: license\n    aggregation: max\n    dimensions:\n      - license_type\nprinciples:\n  - name: Visibility\n    description: >-\n      Use OCI Cost Analysis with cost-tracking tags applied to each\n      GoldenGate deployment, attached block storage, and the deployment's\n      VCN to see OCPU and egress consumption\
  \ by edition and region.\n  - name: Allocation\n    description: >-\n      Apply cost-tracking tags (e.g. team, source_db, target_system) to each\n      deployment so replication cost can be attributed to the consuming data\n      pipeline.\n  - name: Optimization\n    description: >-\n      Right-size deployment OCPU to match peak replication lag tolerance,\n      consolidate low-volume sources onto shared deployments, and prefer\n      cross-region replication only where data-residency requirements\n      mandate it (egress is metered).\n  - name: Accountability\n    description: >-\n      Assign a data-platform owner to each GoldenGate deployment; review OCI\n      consumption monthly and on-premises support renewals annually.\napis:\n  - name: Oracle GoldenGate REST API\n    serviceName: Oracle GoldenGate REST API\n    serviceCategory: Data Integration\n  - name: Oracle GoldenGate for Big Data REST API\n    serviceName: Oracle GoldenGate for Big Data REST API\n    serviceCategory:\
  \ Data Integration\n  - name: Oracle GoldenGate Veridata REST API\n    serviceName: Oracle GoldenGate Veridata REST API\n    serviceCategory: Data Integration\n  - name: Oracle GoldenGate Cloud Service API\n    serviceName: Oracle GoldenGate Cloud Service API\n    serviceCategory: Data Integration\n  - name: Oracle GoldenGate Stream Analytics REST API\n    serviceName: Oracle GoldenGate Stream Analytics REST API\n    serviceCategory: Data Integration\n  - name: Oracle GoldenGate Data Streams REST API\n    serviceName: Oracle GoldenGate Data Streams REST API\n    serviceCategory: Data Integration\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-goldengate/refs/heads/main/finops/oracle-goldengate-finops.yml
sources:
- https://www.oracle.com/integration/goldengate/
- https://docs.oracle.com/en/cloud/paas/goldengate-service/
- https://www.oracle.com/cloud/price-list/
specification: FinOps Framework
tags:
- CDC
- Data Integration
- Real-Time Replication
- Oracle Cloud
- FinOps
- FOCUS
---
