---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: isg-rest-api.yml
  format: yaml
  label: Oracle EBS Integrated SOA Gateway REST API
  slug: oracle-ebs-integrated-soa-gateway-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/isg-rest-api.yml
- filename: financial-services-api.yml
  format: yaml
  label: Oracle EBS Financial Services API
  slug: oracle-ebs-financial-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/financial-services-api.yml
- filename: supply-chain-api.yml
  format: yaml
  label: Oracle EBS Supply Chain Management API
  slug: oracle-ebs-supply-chain-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/supply-chain-api.yml
- filename: human-resources-api.yml
  format: yaml
  label: Oracle EBS Human Resources API
  slug: oracle-ebs-human-resources-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/human-resources-api.yml
- filename: manufacturing-api.yml
  format: yaml
  label: Oracle EBS Manufacturing API
  slug: oracle-ebs-manufacturing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/manufacturing-api.yml
- filename: ecommerce-gateway-api.yml
  format: yaml
  label: Oracle EBS e-Commerce Gateway API
  slug: oracle-ebs-e-commerce-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/openapi/ecommerce-gateway-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (license/support); Monthly (cloud)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Perpetual License + Support + Pay-As-You-Go (cloud infra)
description: 'FOCUS-aligned FinOps for Oracle E-Business Suite: per-named-user (per module) or custom-suite perpetual licenses with 22% annual support, plus underlying Oracle Database, Application Server, and (for cloud-deployed estates) OCI compute / storage / network. Total contracts commonly span $100K–$1M+/year for mid-to-large enterprises.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Oracle America, Inc.
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  ServiceCategory: ERP / Business Applications
  ServiceName: Oracle E-Business Suite
layout: finops
meters:
- aggregation: max
  dimensions:
  - module
  - environment
  name: application_user_licenses
  unit: named_user
- aggregation: max
  dimensions:
  - bundle
  name: custom_suite_licenses
  unit: processor or named_user
- aggregation: sum
  dimensions:
  - contract
  - module
  name: annual_support
  unit: USD-year
- aggregation: sum
  dimensions:
  - tier
  - region
  name: oci_compute_for_ebs
  unit: OCPU-hour
- aggregation: sum
  dimensions:
  - tier
  name: database_for_ebs
  unit: OCPU-hour or processor-year
- aggregation: sum
  dimensions:
  - tier
  name: storage_for_ebs
  unit: GB-month
name: Oracle E Business Suite Finops
provider_name: Oracle E-Business Suite
provider_slug: oracle-e-business-suite
publisher_name: Oracle Corporation
service_category: ERP / Business Applications
slug: oracle-e-business-suite-finops
source_filename: oracle-e-business-suite-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/applications/ebusiness/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Oracle E-Business Suite\nproviderId: oracle-e-business-suite\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - ERP\n  - Business Applications\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Oracle E-Business Suite: per-named-user (per module) or custom-suite\n  perpetual licenses with 22% annual support, plus underlying Oracle Database, Application Server, and\n  (for cloud-deployed estates) OCI compute / storage / network. Total contracts commonly span $100K–$1M+/year\n  for mid-to-large enterprises.'\nsources:\n  - https://www.oracle.com/applications/ebusiness/\n  - https://www.oracle.com/nl/a/ocom/docs/corporate/pricing/applications-price-list-070574.pdf\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Oracle Corporation\nserviceCategory: ERP / Business Applications\nbillingModel:\n  pricingCategory: Perpetual License + Support + Pay-As-You-Go (cloud infra)\n  billingFrequency: Annual (license/support); Monthly (cloud)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Oracle E-Business Suite\n  ServiceCategory: ERP / Business Applications\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: application_user_licenses\n    unit: named_user\n    aggregation: max\n    dimensions:\n      - module\n      - environment\n  - name: custom_suite_licenses\n    unit: processor or named_user\n    aggregation: max\n    dimensions:\n      - bundle\n  - name: annual_support\n    unit: USD-year\n    aggregation: sum\n    dimensions:\n\
  \      - contract\n      - module\n  - name: oci_compute_for_ebs\n    unit: OCPU-hour\n    aggregation: sum\n    dimensions:\n      - tier\n      - region\n  - name: database_for_ebs\n    unit: OCPU-hour or processor-year\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: storage_for_ebs\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Maintain a per-module user count register; reconcile against Oracle LMS audits annually.\n      For cloud-deployed EBS, use OCI Cost Analysis to track infrastructure separately from license cost.\n  - name: Allocation\n    description: Allocate license cost by module to the consuming business unit (Finance, HR, Procurement,\n      etc.); allocate cloud infra by environment (Prod, Test, DR).\n  - name: Optimization\n    description: Reclaim inactive user accounts before each true-up; consolidate non-prod environments;\n      use BYOL on OCI for the EBS-supporting Database;\
  \ consider Oracle Fusion Cloud as a long-term replacement\n      where the modernization business case fits.\n  - name: Accountability\n    description: A named EBS license owner reconciles the user catalog; CFO / IT Finance own the annual\n      Oracle support renewal and license true-up.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-e-business-suite/refs/heads/main/finops/oracle-e-business-suite-finops.yml
sources:
- https://www.oracle.com/applications/ebusiness/
- https://www.oracle.com/nl/a/ocom/docs/corporate/pricing/applications-price-list-070574.pdf
specification: FinOps Framework
tags:
- ERP
- Business Applications
- FinOps
- Cost Management
- FOCUS
---
