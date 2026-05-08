---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (license) + Monthly (cloud infra)
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: License + Underlying Infra
description: FOCUS-aligned FinOps profile for QuestDB. The dominant cost surfaces are (a) the underlying infrastructure (your AWS/Azure/GCP compute, EBS/SSD, network egress) for OSS and BYOC deployments and (b) the QuestDB Enterprise / BYOC commercial license. There is no managed-service per-row, per-query or per-MAU charge.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: QuestDB / AWS Marketplace
  PricingUnit: license-year
  ProviderName: QuestDB
  PublisherName: QuestDB
  ServiceCategory: Database
  ServiceName: QuestDB Enterprise
layout: finops
meters:
- aggregation: sum
  description: Annual QuestDB Enterprise / BYOC license fee (negotiated).
  dimensions:
  - account
  name: enterprise_license
  unit: license-year
- aggregation: sum
  description: Underlying cloud VM hours running QuestDB.
  dimensions:
  - cloud_account
  - region
  - instance_type
  name: compute_instance_hours
  unit: vm-hour
- aggregation: avg
  description: Block / object storage attached to QuestDB instances.
  dimensions:
  - cloud_account
  - storage_class
  name: storage_gb_month
  unit: GB-month
- aggregation: sum
  description: Egress bytes out of the QuestDB cluster to consumers.
  dimensions:
  - cloud_account
  - region
  name: network_egress
  unit: GB
name: Questdb Finops
provider_name: QuestDB
provider_slug: questdb
publisher_name: QuestDB
service_category: Database (Time-Series)
slug: questdb-finops
source_filename: questdb-finops.yml
source_heading: FinOps Profile
source_url: https://questdb.com/enterprise/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: QuestDB\nproviderId: questdb\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Database\n- Time-Series\n- SQL\n- Open Source\n- Performance\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for QuestDB. The dominant cost surfaces are\n  (a) the underlying infrastructure (your AWS/Azure/GCP compute, EBS/SSD,\n  network egress) for OSS and BYOC deployments and (b) the QuestDB Enterprise\n  / BYOC commercial license. There is no managed-service per-row, per-query or\n  per-MAU charge.\nnotes: >-\n  In BYOC, the cloud invoice (AWS/Azure) carries the infra costs; QuestDB\n  Enterprise license/management is invoiced separately. Costs allocate\n  cleanly via cloud-account tags on the QuestDB instance(s).\nsources:\n- https://questdb.com/enterprise/\n- https://questdb.com/byoc/\n- https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: QuestDB\nserviceCategory: Database (Time-Series)\nbillingModel:\n  pricingCategory: License + Underlying Infra\n  billingFrequency: Annual (license) + Monthly (cloud infra)\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: QuestDB Enterprise\n  ServiceCategory: Database\n  ProviderName: QuestDB\n  PublisherName: QuestDB\n  InvoiceIssuerName: QuestDB / AWS Marketplace\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: license-year\nmeters:\n- name: enterprise_license\n  description: Annual QuestDB Enterprise / BYOC license fee (negotiated).\n  unit: license-year\n  aggregation: sum\n  dimensions:\n  - account\n- name: compute_instance_hours\n  description: Underlying cloud VM\
  \ hours running QuestDB.\n  unit: vm-hour\n  aggregation: sum\n  dimensions:\n  - cloud_account\n  - region\n  - instance_type\n- name: storage_gb_month\n  description: Block / object storage attached to QuestDB instances.\n  unit: GB-month\n  aggregation: avg\n  dimensions:\n  - cloud_account\n  - storage_class\n- name: network_egress\n  description: Egress bytes out of the QuestDB cluster to consumers.\n  unit: GB\n  aggregation: sum\n  dimensions:\n  - cloud_account\n  - region\nprinciples:\n- name: Visibility\n  description: Combine QuestDB invoice (license) with cloud cost-export (FOCUS) on the QuestDB-tagged resources.\n- name: Allocation\n  description: Tag QuestDB instances and storage with project / team / environment in AWS / Azure for downstream allocation.\n- name: Optimization\n  description: Use Hypercore-style tiered storage in Enterprise to push cold partitions to S3-class storage; right-size instance class to ingestion throughput.\n- name: Accountability\n  description:\
  \ Assign an Enterprise contract owner; assign cloud-account owner for infra spend.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/questdb/refs/heads/main/finops/questdb-finops.yml
sources:
- https://questdb.com/enterprise/
- https://questdb.com/byoc/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Database
- Time-Series
- SQL
- Open Source
- Performance
- FinOps
- Cost Management
- FOCUS
---
