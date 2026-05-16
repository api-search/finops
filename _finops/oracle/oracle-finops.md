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
  label: Oracle Cloud Infrastructure REST API
  slug: oracle-cloud-infrastructure-rest-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en-us/iaas/api/
- filename: oci-compute-api-openapi.yml
  format: yaml
  label: OCI Compute API
  slug: oci-compute-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle/refs/heads/main/openapi/oci-compute-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Oracle (OCI + Database + Apps).
focus_columns:
  BillingCurrency: USD
  ProviderName: Oracle (OCI + Database + Apps)
  PublisherName: Oracle (OCI + Database + Apps)
  ServiceCategory: Cloud + Database + ERP
  ServiceName: Oracle (OCI + Database + Apps)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - region
  - instance_type
  - tenant
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - service
  - tier
  name: storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - egress_type
  - region_pair
  name: data_transfer
  unit: GB
- aggregation: sum
  dimensions:
  - service
  - operation
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - service
  name: managed_services
  unit: varies
name: Oracle Finops
provider_name: Oracle
provider_slug: oracle
publisher_name: Oracle (OCI + Database + Apps)
service_category: Cloud + Database + ERP
slug: oracle-finops
source_filename: oracle-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/cloud/price-list/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Oracle (OCI + Database + Apps)\nproviderId: oracle\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud + Database + ERP\ndescription: FOCUS-aligned FinOps for Oracle (OCI + Database + Apps).\nsources:\n  - https://www.oracle.com/cloud/price-list/\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Oracle (OCI + Database + Apps)\nserviceCategory: Cloud + Database + ERP\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Oracle (OCI + Database + Apps)\n  ServiceCategory: Cloud + Database + ERP\n  ProviderName:\
  \ Oracle (OCI + Database + Apps)\n  PublisherName: Oracle (OCI + Database + Apps)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Oracle (OCI + Database + Apps) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n\
  \  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle/refs/heads/main/finops/oracle-finops.yml
sources:
- https://www.oracle.com/cloud/price-list/
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud + Database + ERP
---
