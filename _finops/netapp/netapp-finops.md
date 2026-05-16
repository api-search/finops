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
  label: NetApp Cloud Manager API
  slug: netapp-cloud-manager-api
  spec_type: OpenAPI
  url: https://docs.netapp.com/us-en/cloud-manager-automation/api/openapi.yaml
- filename: netapp-ontap-openapi.yml
  format: yaml
  label: NetApp ONTAP REST API
  slug: netapp-ontap-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/netapp/refs/heads/main/openapi/netapp-ontap-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Subscription + Enterprise Contract
description: 'FOCUS-aligned FinOps for NetApp: hybrid storage and data services billed via cloud marketplaces (CVO, FSx for ONTAP, Azure NetApp Files), SaaS subscriptions (BlueXP, Cloud Insights), savings-share (Spot by NetApp), and direct enterprise hardware/software contracts.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: NetApp, Inc.
  PricingCategory: Pay-As-You-Go
  ProviderName: NetApp
  PublisherName: NetApp, Inc.
  ServiceCategory: Storage
  ServiceName: NetApp
  ServiceSubcategory: Cloud Data Management
layout: finops
meters:
- aggregation: avg
  description: Cloud Volumes ONTAP licensed capacity (TB-month) or node-hours.
  dimensions:
  - cloud
  - region
  - tier
  name: cvo_capacity
  unit: TB-month
- aggregation: avg
  description: AWS FSx for NetApp ONTAP capacity and IOPS.
  dimensions:
  - region
  - storage_class
  name: fsx_ontap_capacity
  unit: GB-month
- aggregation: avg
  description: Azure NetApp Files capacity by service level (Standard/Premium/Ultra).
  dimensions:
  - region
  - service_level
  name: anf_capacity
  unit: TB-month
- aggregation: sum
  description: BlueXP service subscriptions (tiering, backup, replication, ransomware).
  dimensions:
  - service
  - tenant
  name: bluexp_subscription
  unit: month
- aggregation: sum
  description: Cloud Insights tier subscription (Basic / Standard / Premium).
  dimensions:
  - tier
  - tenant
  name: cloud_insights_subscription
  unit: month
- aggregation: sum
  description: Percentage-of-savings billed by Spot by NetApp.
  dimensions:
  - product
  - account
  name: spot_savings_share
  unit: USD
- aggregation: sum
  description: Hardware + ONTAP + support contracted purchases.
  dimensions:
  - sku
  - region
  name: enterprise_contract
  unit: month
name: Netapp Finops
provider_name: NetApp
provider_slug: netapp
publisher_name: NetApp, Inc.
service_category: Storage + Data Management
slug: netapp-finops
source_filename: netapp-finops.yml
source_heading: FinOps Profile
source_url: https://www.netapp.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: NetApp\nproviderId: netapp\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud\n  - Storage\n  - Data Management\nnotes: NetApp pricing is non-public; FinOps shape captured here is based on the documented product portfolio\n  and typical cloud-marketplace billing patterns rather than published per-SKU rates. Reconcile against\n  marketplace listings and the customer's NetApp Master License Agreement.\ndescription: 'FOCUS-aligned FinOps for NetApp: hybrid storage and data services billed via cloud marketplaces\n  (CVO, FSx for ONTAP, Azure NetApp Files), SaaS subscriptions (BlueXP, Cloud Insights), savings-share\n  (Spot by NetApp), and direct enterprise hardware/software contracts.'\nsources:\n  - https://www.netapp.com/pricing/\n  - https://docs.netapp.com/us-en/cloud-manager-automation/\nalignedWith:\n  framework:\
  \ FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: NetApp, Inc.\nserviceCategory: Storage + Data Management\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription + Enterprise Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: NetApp\n  ServiceCategory: Storage\n  ServiceSubcategory: Cloud Data Management\n  ProviderName: NetApp\n  PublisherName: NetApp, Inc.\n  InvoiceIssuerName: NetApp, Inc.\n  BillingCurrency: USD\n  PricingCategory: Pay-As-You-Go\nmeters:\n  - name: cvo_capacity\n    description: Cloud Volumes ONTAP licensed capacity (TB-month) or node-hours.\n    unit: TB-month\n    aggregation: avg\n    dimensions:\n      - cloud\n      - region\n      - tier\n  - name: fsx_ontap_capacity\n\
  \    description: AWS FSx for NetApp ONTAP capacity and IOPS.\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - storage_class\n  - name: anf_capacity\n    description: Azure NetApp Files capacity by service level (Standard/Premium/Ultra).\n    unit: TB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - service_level\n  - name: bluexp_subscription\n    description: BlueXP service subscriptions (tiering, backup, replication, ransomware).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - service\n      - tenant\n  - name: cloud_insights_subscription\n    description: Cloud Insights tier subscription (Basic / Standard / Premium).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - tenant\n  - name: spot_savings_share\n    description: Percentage-of-savings billed by Spot by NetApp.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product\n      - account\n  - name: enterprise_contract\n\
  \    description: Hardware + ONTAP + support contracted purchases.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - sku\n      - region\nprinciples:\n  - name: Visibility\n    description: Use BlueXP Digital Wallet for license inventory; Cloud Insights for telemetry; Spot\n      Eco for commitment visibility; cloud-marketplace billing exports for CVO / FSx / ANF charges.\n  - name: Allocation\n    description: Tag NetApp resources at the cloud layer (AWS/Azure/GCP tags) so cost attribution flows\n      through to FOCUS exports; use BlueXP Connector / project boundaries per business unit.\n  - name: Optimization\n    description: Use BlueXP tiering to move cold blocks to object storage; right-size ONTAP service levels\n      (Standard vs Premium vs Ultra); use Spot Ocean to optimize Kubernetes compute; review BYOL vs marketplace\n      tradeoffs per workload.\n  - name: Accountability\n    description: Assign per-workload license owners in BlueXP; review BlueXP Digital Wallet\
  \ quarterly\n      for unused capacity; reconcile cloud-marketplace bills against NetApp ELA commitments.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/netapp/refs/heads/main/finops/netapp-finops.yml
sources:
- https://www.netapp.com/pricing/
- https://docs.netapp.com/us-en/cloud-manager-automation/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud
- Storage
- Data Management
---
