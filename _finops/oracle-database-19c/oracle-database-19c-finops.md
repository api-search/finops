---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-database-19c-ords-openapi.yml
  format: yaml
  label: Oracle REST Data Services (ORDS)
  slug: oracle-rest-data-services-ords
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-database-19c/refs/heads/main/openapi/oracle-database-19c-ords-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (license/support); Monthly (cloud)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Perpetual License + Support + Pay-As-You-Go (cloud) + BYOL
description: 'FOCUS-aligned FinOps for Oracle Database 19c (long-term-release): perpetual per-Processor or per-NUP licenses with 22% annual support, separately-licensed Options (Partitioning, RAC, ADG, Multitenant) and Management Packs, plus per-OCPU/ECPU-hour cloud-managed variants on OCI (license-included or BYOL). 19c specifically is the long-term-supported release used for many large estates.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Oracle America, Inc.
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  ServiceCategory: Database
  ServiceName: Oracle Database 19c
layout: finops
meters:
- aggregation: max
  dimensions:
  - edition
  - environment
  name: processor_licenses_19c
  unit: processor
- aggregation: max
  dimensions:
  - edition
  - environment
  name: nup_licenses_19c
  unit: NUP
- aggregation: max
  dimensions:
  - option
  name: option_licenses_19c
  unit: processor or NUP
- aggregation: max
  dimensions:
  - pack
  name: management_pack_licenses_19c
  unit: processor or NUP
- aggregation: sum
  dimensions:
  - contract
  name: annual_support
  unit: USD-year
- aggregation: sum
  dimensions:
  - service
  - region
  - byol
  name: cloud_db_ocpu_hours
  unit: OCPU-hour
- aggregation: sum
  dimensions:
  - region
  name: cloud_db_storage
  unit: GB-month
name: Oracle Database 19C Finops
provider_name: Oracle Database 19c
provider_slug: oracle-database-19c
publisher_name: Oracle Corporation
service_category: Database
slug: oracle-database-19c-finops
source_filename: oracle-database-19c-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/database/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Oracle Database 19c\nproviderId: oracle-database-19c\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Database\n  - Enterprise\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Oracle Database 19c (long-term-release): perpetual per-Processor\n  or per-NUP licenses with 22% annual support, separately-licensed Options (Partitioning, RAC, ADG, Multitenant)\n  and Management Packs, plus per-OCPU/ECPU-hour cloud-managed variants on OCI (license-included or BYOL).\n  19c specifically is the long-term-supported release used for many large estates.'\nsources:\n  - https://www.oracle.com/database/pricing/\n  - https://www.oracle.com/cloud/price-list/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Oracle Corporation\nserviceCategory: Database\nbillingModel:\n  pricingCategory: Perpetual License + Support + Pay-As-You-Go (cloud) + BYOL\n  billingFrequency: Annual (license/support); Monthly (cloud)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Oracle Database 19c\n  ServiceCategory: Database\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: processor_licenses_19c\n    unit: processor\n    aggregation: max\n    dimensions:\n      - edition\n      - environment\n  - name: nup_licenses_19c\n    unit: NUP\n    aggregation: max\n    dimensions:\n      - edition\n      - environment\n  - name: option_licenses_19c\n    unit: processor or NUP\n    aggregation: max\n    dimensions:\n      - option\n  - name: management_pack_licenses_19c\n\
  \    unit: processor or NUP\n    aggregation: max\n    dimensions:\n      - pack\n  - name: annual_support\n    unit: USD-year\n    aggregation: sum\n    dimensions:\n      - contract\n  - name: cloud_db_ocpu_hours\n    unit: OCPU-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - byol\n  - name: cloud_db_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\nprinciples:\n  - name: Visibility\n    description: Maintain a CSI/contract-to-deployment register for 19c hosts and their EE Options; reconcile\n      with Oracle LMS data. For OCI, use Cost Analysis to track Database / Autonomous Database consumption.\n  - name: Allocation\n    description: Tag each 19c host and OCI Database Cloud instance with environment + business-unit metadata;\n      enforce via OCI compartments.\n  - name: Optimization\n    description: Use Multitenant to consolidate many PDBs onto fewer EE-licensed CDBs; convert under-utilized\n      perpetual\
  \ licenses to BYOL on OCI; eliminate unused Options and Management Packs (each carries\n      22% support).\n  - name: Accountability\n    description: License-management owner tracks 19c estate and Options counts; finance owns annual support\n      renewal. Cloud DB consumption reviewed monthly against forecast.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-database-19c/refs/heads/main/finops/oracle-database-19c-finops.yml
sources:
- https://www.oracle.com/database/pricing/
- https://www.oracle.com/cloud/price-list/
specification: FinOps Framework
tags:
- Database
- Enterprise
- FinOps
- Cost Management
- FOCUS
---
