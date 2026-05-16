---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-enterprise-manager-cloud-control-openapi.yml
  format: yaml
  label: Oracle Enterprise Manager Cloud Control REST API
  slug: oracle-enterprise-manager-cloud-control-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-enterprise-manager/refs/heads/main/openapi/oracle-enterprise-manager-cloud-control-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (license/support); Monthly (cloud)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Perpetual License + Support + Pay-As-You-Go (OCI O+M)
description: 'FOCUS-aligned FinOps for Oracle Enterprise Manager: the OEM framework itself is included with Oracle DB licenses, but each Management Pack (Diagnostics, Tuning, Database Lifecycle Management, Cloud Management, etc.) is a separately-licensed perpetual line item with 22% annual support, sized on the same metric (Processor or NUP) as the targets being managed. OCI Observability and Management is the cloud-native consumption-based alternative.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Oracle America, Inc.
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  ServiceCategory: IT Operations Management
  ServiceName: Oracle Enterprise Manager
layout: finops
meters:
- aggregation: max
  dimensions:
  - target_type
  - environment
  name: diagnostics_pack_licenses
  unit: processor or NUP
- aggregation: max
  dimensions:
  - target_type
  - environment
  name: tuning_pack_licenses
  unit: processor or NUP
- aggregation: max
  dimensions:
  - target_type
  name: db_lifecycle_management_pack_licenses
  unit: processor or NUP
- aggregation: max
  dimensions:
  - pack
  - target_type
  name: other_pack_licenses
  unit: processor or NUP
- aggregation: sum
  dimensions:
  - pack
  - contract
  name: annual_support
  unit: USD-year
- aggregation: sum
  dimensions:
  - service
  - region
  name: oci_observability_consumption
  unit: varies
name: Oracle Enterprise Manager Finops
provider_name: Oracle Enterprise Manager
provider_slug: oracle-enterprise-manager
publisher_name: Oracle Corporation
service_category: IT Operations Management
slug: oracle-enterprise-manager-finops
source_filename: oracle-enterprise-manager-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/manageability/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Oracle Enterprise Manager\nproviderId: oracle-enterprise-manager\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Enterprise Management\n  - Monitoring\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Oracle Enterprise Manager: the OEM framework itself is included\n  with Oracle DB licenses, but each Management Pack (Diagnostics, Tuning, Database Lifecycle Management,\n  Cloud Management, etc.) is a separately-licensed perpetual line item with 22% annual support, sized\n  on the same metric (Processor or NUP) as the targets being managed. OCI Observability and Management\n  is the cloud-native consumption-based alternative.'\nsources:\n  - https://www.oracle.com/manageability/\n  - https://docs.oracle.com/en/enterprise-manager/cloud-control/enterprise-manager-cloud-control/24.1/oemli/\nalignedWith:\n\
  \  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Oracle Corporation\nserviceCategory: IT Operations Management\nbillingModel:\n  pricingCategory: Perpetual License + Support + Pay-As-You-Go (OCI O+M)\n  billingFrequency: Annual (license/support); Monthly (cloud)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Oracle Enterprise Manager\n  ServiceCategory: IT Operations Management\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: diagnostics_pack_licenses\n    unit: processor or NUP\n    aggregation: max\n    dimensions:\n      - target_type\n      - environment\n  - name: tuning_pack_licenses\n    unit: processor or NUP\n    aggregation:\
  \ max\n    dimensions:\n      - target_type\n      - environment\n  - name: db_lifecycle_management_pack_licenses\n    unit: processor or NUP\n    aggregation: max\n    dimensions:\n      - target_type\n  - name: other_pack_licenses\n    unit: processor or NUP\n    aggregation: max\n    dimensions:\n      - pack\n      - target_type\n  - name: annual_support\n    unit: USD-year\n    aggregation: sum\n    dimensions:\n      - pack\n      - contract\n  - name: oci_observability_consumption\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\nprinciples:\n  - name: Visibility\n    description: Maintain a target-to-pack matrix — which databases, hosts, middleware are entitled to\n      Diagnostics, Tuning, DBLM, etc. Reconcile with Oracle LMS audit data; track OCI O+M consumption\n      separately.\n  - name: Allocation\n    description: Allocate Management Pack cost to the team that owns the target estate (DBA team for\n      Diagnostics/Tuning/DBLM;\
  \ platform team for Cloud Management Pack).\n  - name: Optimization\n    description: Eliminate Diagnostics/Tuning Pack on environments that don't need them (Dev, DR); migrate\n      lightweight monitoring needs to OCI O+M consumption-based services; ensure Tuning Pack always paired\n      with Diagnostics Pack (license rule). Each pack carries 22% annual support — every removed pack\n      saves the support stream too.\n  - name: Accountability\n    description: A named DBA or platform manager owns the OEM pack catalog and reconciles before each\n      annual true-up; finance owns annual support renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-enterprise-manager/refs/heads/main/finops/oracle-enterprise-manager-finops.yml
sources:
- https://www.oracle.com/manageability/
- https://docs.oracle.com/en/enterprise-manager/cloud-control/enterprise-manager-cloud-control/24.1/oemli/
specification: FinOps Framework
tags:
- Enterprise Management
- Monitoring
- FinOps
- Cost Management
- FOCUS
---
