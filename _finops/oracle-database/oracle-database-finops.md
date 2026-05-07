---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Oracle REST Data Services (ORDS)
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/database/oracle/oracle-rest-data-services/
- filename: openapi.yaml
  format: yaml
  label: Oracle Cloud Infrastructure Database API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/iaas/api/#/en/database/
- filename: oracle-database-soda-openapi.yml
  format: yaml
  label: Oracle SODA (Simple Oracle Document Access)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-database/refs/heads/main/openapi/oracle-database-soda-openapi.yml
- filename: oracle-database-txeventq-asyncapi.yml
  format: yaml
  label: Oracle Transactional Event Queues (TxEventQ)
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-database/refs/heads/main/asyncapi/oracle-database-txeventq-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (license/support); Monthly (cloud)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Perpetual License + Support + Pay-As-You-Go (cloud) + BYOL
description: 'FOCUS-aligned FinOps for Oracle Database: perpetual per-Processor or per-Named-User-Plus licenses (with 22% annual support) for on-prem / self-hosted deployments, plus per-OCPU/ECPU-hour cloud-managed variants on OCI (license-included or BYOL). Options and Management Packs (Partitioning, Diagnostics Pack, Tuning Pack, etc.) are licensed separately and meaningfully drive total cost.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Oracle America, Inc.
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  ServiceCategory: Database
  ServiceName: Oracle Database
layout: finops
meters:
- aggregation: max
  dimensions:
  - edition
  - environment
  name: processor_licenses
  unit: processor
- aggregation: max
  dimensions:
  - edition
  - environment
  name: named_user_plus_licenses
  unit: NUP
- aggregation: max
  dimensions:
  - option
  - edition
  name: option_licenses
  unit: processor or NUP
- aggregation: max
  dimensions:
  - pack
  name: management_pack_licenses
  unit: processor or NUP
- aggregation: sum
  dimensions:
  - contract
  - edition
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
  - tier
  name: cloud_db_storage
  unit: GB-month
name: Oracle Database Finops
provider_name: Oracle Database
provider_slug: oracle-database
publisher_name: Oracle Corporation
service_category: Database
slug: oracle-database-finops
source_filename: oracle-database-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/database/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Oracle Database\nproviderId: oracle-database\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Database\n  - Enterprise\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Oracle Database: perpetual per-Processor or per-Named-User-Plus\n  licenses (with 22% annual support) for on-prem / self-hosted deployments, plus per-OCPU/ECPU-hour cloud-managed\n  variants on OCI (license-included or BYOL). Options and Management Packs (Partitioning, Diagnostics\n  Pack, Tuning Pack, etc.) are licensed separately and meaningfully drive total cost.'\nsources:\n  - https://www.oracle.com/database/pricing/\n  - https://www.oracle.com/cloud/price-list/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Oracle Corporation\nserviceCategory: Database\nbillingModel:\n  pricingCategory: Perpetual License + Support + Pay-As-You-Go (cloud) + BYOL\n  billingFrequency: Annual (license/support); Monthly (cloud)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Oracle Database\n  ServiceCategory: Database\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: processor_licenses\n    unit: processor\n    aggregation: max\n    dimensions:\n      - edition\n      - environment\n  - name: named_user_plus_licenses\n    unit: NUP\n    aggregation: max\n    dimensions:\n      - edition\n      - environment\n  - name: option_licenses\n    unit: processor or NUP\n    aggregation: max\n    dimensions:\n      - option\n      - edition\n  - name: management_pack_licenses\n    unit: processor or NUP\n    aggregation: max\n\
  \    dimensions:\n      - pack\n  - name: annual_support\n    unit: USD-year\n    aggregation: sum\n    dimensions:\n      - contract\n      - edition\n  - name: cloud_db_ocpu_hours\n    unit: OCPU-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - byol\n  - name: cloud_db_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - tier\nprinciples:\n  - name: Visibility\n    description: Reconcile Oracle CSI / contract numbers against actual deployed processor counts; for\n      cloud, use OCI Cost Analysis to track Database Cloud Service / Autonomous DB consumption per compartment.\n  - name: Allocation\n    description: Tag each licensed environment (prod, dr, test) and cloud DB instance with the consuming\n      business unit; use OCI compartments to enforce allocation boundaries.\n  - name: Optimization\n    description: Convert under-utilized perpetual licenses to BYOL on OCI for ~70%+ savings; consolidate\n     \
  \ with Multitenant pluggable databases; right-size cloud DB shapes; remove unused Options and Management\n      Packs (each one carries 22% support); for Autonomous DB, use Elastic Pools (up to ~87% off compute).\n  - name: Accountability\n    description: A named license-management owner reconciles Oracle audits and tracks LMS / certified\n      processor counts; finance owns the annual support renewal. Cloud DB consumption is reviewed monthly\n      against forecast.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-database/refs/heads/main/finops/oracle-database-finops.yml
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
