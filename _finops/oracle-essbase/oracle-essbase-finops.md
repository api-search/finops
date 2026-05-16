---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-essbase-rest-api-openapi.yml
  format: yaml
  label: Oracle Essbase REST API
  slug: oracle-essbase-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-essbase/refs/heads/main/openapi/oracle-essbase-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: BYOL + Pay-As-You-Go (OCI Compute)
description: 'FOCUS-aligned FinOps view for Oracle Essbase: cost is composed of underlying OCI compute, block storage, and networking consumed by the Essbase host, plus a separately negotiated Oracle Technology license (BYOL or per-processor / named-user-plus on-premises).'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: BYOL + Usage
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: Analytics
  ServiceName: Oracle Essbase
layout: finops
meters:
- aggregation: sum
  description: OCPU-hours consumed by the OCI compute instance hosting Essbase
  dimensions:
  - region
  - shape
  - tag
  name: oci_compute_ocpu_hours
  unit: ocpu-hour
- aggregation: sum
  description: Block storage attached to the Essbase host
  dimensions:
  - region
  - tag
  name: oci_block_storage_gb_month
  unit: GB-month
- aggregation: sum
  description: Outbound data transfer from the Essbase host
  dimensions:
  - region
  name: oci_egress_gb
  unit: GB
- aggregation: max
  description: Contractual Oracle Technology license for Essbase (per-processor or NUP)
  dimensions:
  - license_type
  name: essbase_license
  unit: license
name: Oracle Essbase Finops
provider_name: Oracle Essbase
provider_slug: oracle-essbase
publisher_name: Oracle America, Inc.
service_category: Analytics
slug: oracle-essbase-finops
source_filename: oracle-essbase-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/business-analytics/essbase/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Essbase\nproviderId: oracle-essbase\npublisherName: Oracle America, Inc.\nserviceCategory: Analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Analytics\n  - OLAP\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle Essbase: cost is composed of underlying\n  OCI compute, block storage, and networking consumed by the Essbase host, plus\n  a separately negotiated Oracle Technology license (BYOL or per-processor /\n  named-user-plus on-premises).\nsources:\n  - https://www.oracle.com/business-analytics/essbase/\n  - https://cloudmarketplace.oracle.com/marketplace/en_US/listing/79529283\n\
  \  - https://www.oracle.com/cloud/price-list/\nnotes: >-\n  No public per-API meter exists. FinOps observation is performed against OCI\n  Cost Analysis (Cost-Tracking Tags) for the Essbase host plus the contractual\n  Oracle Technology license line.\nbillingModel:\n  pricingCategory: BYOL + Pay-As-You-Go (OCI Compute)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle Essbase\n  ServiceCategory: Analytics\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: BYOL + Usage\n  ChargeCategory: Usage\nmeters:\n  - name: oci_compute_ocpu_hours\n    description: OCPU-hours consumed by the OCI compute instance hosting Essbase\n    unit: ocpu-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - shape\n      - tag\n  - name: oci_block_storage_gb_month\n\
  \    description: Block storage attached to the Essbase host\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - tag\n  - name: oci_egress_gb\n    description: Outbound data transfer from the Essbase host\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n  - name: essbase_license\n    description: Contractual Oracle Technology license for Essbase (per-processor or NUP)\n    unit: license\n    aggregation: max\n    dimensions:\n      - license_type\nprinciples:\n  - name: Visibility\n    description: >-\n      Use OCI Cost Analysis with cost-tracking tags applied to the Essbase\n      compute, block volumes, and VCN to view consumption; reconcile against\n      the Oracle Technology license entitlement separately.\n  - name: Allocation\n    description: >-\n      Apply OCI cost-tracking tags (e.g. team, application, environment) to\n      every Essbase host and storage volume so spend can be attributed to\n      consuming products.\n \
  \ - name: Optimization\n    description: >-\n      Right-size the OCI compute shape to match actual calc and query\n      concurrency, schedule non-production instances to stop outside business\n      hours, and consolidate small Essbase applications onto shared hosts\n      where license terms permit.\n  - name: Accountability\n    description: >-\n      Assign an owner to each Essbase application; review OCI consumption and\n      Oracle support renewals quarterly.\napis:\n  - name: Oracle Essbase REST API\n    serviceName: Oracle Essbase REST API\n    serviceCategory: Analytics\n  - name: Essbase Java API\n    serviceName: Essbase Java API\n    serviceCategory: Analytics\n  - name: Essbase C API\n    serviceName: Essbase C API\n    serviceCategory: Analytics\n  - name: Essbase MaxL Scripting Interface\n    serviceName: Essbase MaxL Scripting Interface\n    serviceCategory: Analytics\n  - name: Essbase CLI (Command Line Interface)\n    serviceName: Essbase CLI (Command Line Interface)\n\
  \    serviceCategory: Analytics\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-essbase/refs/heads/main/finops/oracle-essbase-finops.yml
sources:
- https://www.oracle.com/business-analytics/essbase/
- https://cloudmarketplace.oracle.com/marketplace/en_US/listing/79529283
- https://www.oracle.com/cloud/price-list/
specification: FinOps Framework
tags:
- Analytics
- OLAP
- Oracle Cloud
- FinOps
- FOCUS
---
