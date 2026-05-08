---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-cloud-compute-openapi.yaml
  format: yaml
  label: Compute API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/openapi/oracle-cloud-compute-openapi.yaml
- filename: oracle-cloud-object-storage-openapi.yaml
  format: yaml
  label: Object Storage API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/openapi/oracle-cloud-object-storage-openapi.yaml
- filename: oracle-cloud-networking-openapi.yaml
  format: yaml
  label: Networking API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/openapi/oracle-cloud-networking-openapi.yaml
- filename: oracle-cloud-database-openapi.yaml
  format: yaml
  label: Database API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/openapi/oracle-cloud-database-openapi.yaml
- filename: oracle-cloud-iam-openapi.yaml
  format: yaml
  label: Identity and Access Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/openapi/oracle-cloud-iam-openapi.yaml
- filename: oracle-cloud-oke-openapi.yaml
  format: yaml
  label: Container Engine for Kubernetes API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/openapi/oracle-cloud-oke-openapi.yaml
- filename: oracle-cloud-functions-openapi.yaml
  format: yaml
  label: Functions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/openapi/oracle-cloud-functions-openapi.yaml
- filename: oracle-cloud-monitoring-openapi.yaml
  format: yaml
  label: Monitoring API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/openapi/oracle-cloud-monitoring-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use + BYOL
description: 'FOCUS-aligned FinOps for Oracle Cloud Infrastructure: per-service pay-as-you-go (compute OCPU/ECPU-hour, storage GB-month, network egress, autonomous DB) plus committed-use Universal Credits (1- or 3-year) and BYOL discounts. Always Free tier provides perpetual allocation. Cost data accessible via Cost Analysis, Usage Reports (CSV / Object Storage), and the FOCUS Cost and Usage exports.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Oracle America, Inc.
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  RegionId: e.g. us-ashburn-1, eu-frankfurt-1, ap-tokyo-1
  ServiceCategory: Cloud Infrastructure
  ServiceName: Oracle Cloud Infrastructure
layout: finops
meters:
- aggregation: sum
  dimensions:
  - shape
  - region
  - tenancy
  - compartment
  name: compute_ocpu_hours
  unit: OCPU-hour
- aggregation: sum
  dimensions:
  - service
  - region
  - autonomous_db
  name: ecpu_hours
  unit: ECPU-hour
- aggregation: sum
  dimensions:
  - region
  - performance_tier
  name: block_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - storage_tier
  name: object_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - destination
  name: data_egress
  unit: GB
- aggregation: sum
  dimensions:
  - shape
  - region
  name: load_balancer_hours
  unit: shape-hour
- aggregation: sum
  dimensions:
  - autonomous_db
  - region
  name: database_storage
  unit: GB-month
name: Oracle Cloud Finops
provider_name: Oracle Cloud Infrastructure
provider_slug: oracle-cloud
publisher_name: Oracle Corporation
service_category: Cloud Infrastructure
slug: oracle-cloud-finops
source_filename: oracle-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/cloud/price-list/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Oracle Cloud Infrastructure\nproviderId: oracle-cloud\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud Computing\n  - Infrastructure as a Service\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Oracle Cloud Infrastructure: per-service pay-as-you-go (compute\n  OCPU/ECPU-hour, storage GB-month, network egress, autonomous DB) plus committed-use Universal Credits\n  (1- or 3-year) and BYOL discounts. Always Free tier provides perpetual allocation. Cost data accessible\n  via Cost Analysis, Usage Reports (CSV / Object Storage), and the FOCUS Cost and Usage exports.'\nsources:\n  - https://www.oracle.com/cloud/price-list/\n  - https://www.oracle.com/cloud/free/\n  - https://docs.oracle.com/en-us/iaas/Content/Billing/Concepts/billingoverview.htm\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Oracle Corporation\nserviceCategory: Cloud Infrastructure\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use + BYOL\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle Cloud Infrastructure\n  ServiceCategory: Cloud Infrastructure\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  RegionId: e.g. us-ashburn-1, eu-frankfurt-1, ap-tokyo-1\nmeters:\n  - name: compute_ocpu_hours\n    unit: OCPU-hour\n    aggregation: sum\n    dimensions:\n      - shape\n      - region\n      - tenancy\n      - compartment\n  - name: ecpu_hours\n    unit: ECPU-hour\n    aggregation: sum\n    dimensions:\n      -\
  \ service\n      - region\n      - autonomous_db\n  - name: block_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - performance_tier\n  - name: object_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - storage_tier\n  - name: data_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - destination\n  - name: load_balancer_hours\n    unit: shape-hour\n    aggregation: sum\n    dimensions:\n      - shape\n      - region\n  - name: database_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - autonomous_db\n      - region\nprinciples:\n  - name: Visibility\n    description: Use OCI Cost Analysis, scheduled Usage Reports to Object Storage (CSV), and the FOCUS\n      Cost and Usage export to attribute spend to compartments and tags in near real-time.\n  - name: Allocation\n    description: Tag every resource with cost-center / environment / app metadata; use\
  \ OCI compartments\n      as the primary allocation boundary and tag-based budgets to alert per group.\n  - name: Optimization\n    description: Convert sustained workloads to Universal Credits (1y / 3y commitment); apply BYOL on\n      Oracle Database / WebLogic for ~70%+ savings; consolidate Autonomous Databases into Elastic Pools\n      (up to ~87% off); right-size to Arm Ampere A1 shapes where workloads permit; clean up unattached\n      block volumes and orphaned reserved IPs.\n  - name: Accountability\n    description: Cloud / platform team owns the OCI tenancy invoice; compartment owners review monthly\n      Cost Analysis reports and respond to budget alerts. Use OCI Quotas to enforce hard caps on optional\n      services.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-cloud/refs/heads/main/finops/oracle-cloud-finops.yml
sources:
- https://www.oracle.com/cloud/price-list/
- https://www.oracle.com/cloud/free/
- https://docs.oracle.com/en-us/iaas/Content/Billing/Concepts/billingoverview.htm
specification: FinOps Framework
tags:
- Cloud Computing
- Infrastructure as a Service
- FinOps
- Cost Management
- FOCUS
---
