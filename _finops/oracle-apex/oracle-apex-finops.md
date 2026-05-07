---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Included with Database + Pay-As-You-Go (cloud)
description: 'FOCUS-aligned FinOps for Oracle APEX: APEX is free-with-database, so the meters that matter are the Oracle Database / Autonomous Database compute (ECPU or OCPU) and storage that host the APEX workspaces.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Oracle America, Inc.
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  ServiceCategory: Application Development / Low-Code
  ServiceName: Oracle APEX
layout: finops
meters:
- aggregation: sum
  dimensions:
  - autonomous_db
  - workload_type
  - region
  name: ecpu_hours
  unit: ECPU-hour
- aggregation: sum
  dimensions:
  - autonomous_db
  - region
  name: database_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - autonomous_db
  name: backup_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  name: data_egress
  unit: GB
name: Oracle Apex Finops
provider_name: Oracle APEX
provider_slug: oracle-apex
publisher_name: Oracle Corporation
service_category: Application Development / Low-Code
slug: oracle-apex-finops
source_filename: oracle-apex-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/application-development/apex/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Oracle APEX\nproviderId: oracle-apex\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Low-Code\n  - Database\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Oracle APEX: APEX is free-with-database, so the meters that matter\n  are the Oracle Database / Autonomous Database compute (ECPU or OCPU) and storage that host the APEX\n  workspaces.'\nsources:\n  - https://www.oracle.com/application-development/apex/pricing/\n  - https://www.oracle.com/autonomous-database/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Oracle Corporation\nserviceCategory: Application Development / Low-Code\nbillingModel:\n  pricingCategory:\
  \ Included with Database + Pay-As-You-Go (cloud)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Oracle APEX\n  ServiceCategory: Application Development / Low-Code\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: ecpu_hours\n    unit: ECPU-hour\n    aggregation: sum\n    dimensions:\n      - autonomous_db\n      - workload_type\n      - region\n  - name: database_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - autonomous_db\n      - region\n  - name: backup_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - autonomous_db\n  - name: data_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\nprinciples:\n  - name: Visibility\n    description: Use OCI Cost Analysis and Usage Reports to track ECPU and storage consumption\
  \ per Autonomous\n      Database / APEX Service instance; tag instances with workspace/team metadata.\n  - name: Allocation\n    description: Map APEX workspaces to OCI compartments and tags so each business unit's database consumption\n      is allocated cleanly; use OCI tag-based budgets.\n  - name: Optimization\n    description: Use Always-Free instances for dev/test; consolidate workspaces into Elastic Pools (up\n      to ~87% compute discount); enable auto-scaling to pay only for peak ECPUs; bring your own Database\n      license (BYOL) where applicable.\n  - name: Accountability\n    description: Platform team owns the Autonomous Database subscription and monitors monthly OCI invoice\n      lines for APEX-hosting instances; line-of-business teams own workspace storage growth.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-apex/refs/heads/main/finops/oracle-apex-finops.yml
sources:
- https://www.oracle.com/application-development/apex/pricing/
- https://www.oracle.com/autonomous-database/pricing/
specification: FinOps Framework
tags:
- Low-Code
- Database
- FinOps
- Cost Management
- FOCUS
---
