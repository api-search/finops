---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (license) + Monthly (cloud / infra)
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: License + Underlying Infra OR Managed Subscription
description: FOCUS-aligned FinOps profile for VictoriaMetrics. The dominant cost surfaces are (a) the underlying infrastructure for self-hosted Community/Enterprise (cloud VMs, attached SSD/EBS, network egress) and (b) VictoriaMetrics Enterprise license or VictoriaMetrics Cloud subscription metered by ingestion rate / active series. There is no per-query or per-MAU charge.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: VictoriaMetrics
  PricingUnit: ingestion-rate / active-series
  ProviderName: VictoriaMetrics
  PublisherName: VictoriaMetrics
  ServiceCategory: Observability
  ServiceName: VictoriaMetrics
layout: finops
meters:
- aggregation: sum
  description: Annual VictoriaMetrics Enterprise license fee.
  dimensions:
  - account
  name: enterprise_license
  unit: license-year
- aggregation: avg
  description: Datapoints ingested per second on VictoriaMetrics Cloud (managed).
  dimensions:
  - cluster_id
  name: cloud_ingestion_rate
  unit: samples_per_second
- aggregation: avg
  description: Active time series stored on VictoriaMetrics Cloud.
  dimensions:
  - cluster_id
  name: cloud_active_series
  unit: series
- aggregation: sum
  description: Underlying cloud VM hours running vminsert / vmselect / vmstorage / vmagent.
  dimensions:
  - component
  - region
  name: compute_instance_hours
  unit: vm-hour
- aggregation: avg
  description: Block storage attached to vmstorage.
  dimensions:
  - cluster_id
  name: storage_gb_month
  unit: GB-month
- aggregation: sum
  description: Egress bytes from VictoriaMetrics to consumers (Grafana, alerts, federation).
  dimensions:
  - region
  name: network_egress
  unit: GB
name: Victoriametrics Finops
provider_name: VictoriaMetrics
provider_slug: victoriametrics
publisher_name: VictoriaMetrics
service_category: Observability / Time-Series
slug: victoriametrics-finops
source_filename: victoriametrics-finops.yml
source_heading: FinOps Profile
source_url: https://victoriametrics.com/products/enterprise/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: VictoriaMetrics\nproviderId: victoriametrics\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Database\n- Time-Series\n- Monitoring\n- Open Source\n- Prometheus\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for VictoriaMetrics. The dominant cost surfaces\n  are (a) the underlying infrastructure for self-hosted Community/Enterprise\n  (cloud VMs, attached SSD/EBS, network egress) and (b) VictoriaMetrics\n  Enterprise license or VictoriaMetrics Cloud subscription metered by\n  ingestion rate / active series. There is no per-query or per-MAU charge.\nnotes: >-\n  VictoriaMetrics exposes per-tenant statistics that map cleanly to FOCUS\n  ResourceTag for chargeback by tenant. Cloud invoices are denominated in\n  ingestion-rate / active-series tiers.\nsources:\n- https://victoriametrics.com/products/enterprise/\n\
  - https://victoriametrics.com/products/cloud/\n- https://docs.victoriametrics.com/PerTenantStatistic.html\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: VictoriaMetrics\nserviceCategory: Observability / Time-Series\nbillingModel:\n  pricingCategory: License + Underlying Infra OR Managed Subscription\n  billingFrequency: Annual (license) + Monthly (cloud / infra)\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: VictoriaMetrics\n  ServiceCategory: Observability\n  ProviderName: VictoriaMetrics\n  PublisherName: VictoriaMetrics\n  InvoiceIssuerName: VictoriaMetrics\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: ingestion-rate / active-series\nmeters:\n- name: enterprise_license\n\
  \  description: Annual VictoriaMetrics Enterprise license fee.\n  unit: license-year\n  aggregation: sum\n  dimensions:\n  - account\n- name: cloud_ingestion_rate\n  description: Datapoints ingested per second on VictoriaMetrics Cloud (managed).\n  unit: samples_per_second\n  aggregation: avg\n  dimensions:\n  - cluster_id\n- name: cloud_active_series\n  description: Active time series stored on VictoriaMetrics Cloud.\n  unit: series\n  aggregation: avg\n  dimensions:\n  - cluster_id\n- name: compute_instance_hours\n  description: Underlying cloud VM hours running vminsert / vmselect / vmstorage / vmagent.\n  unit: vm-hour\n  aggregation: sum\n  dimensions:\n  - component\n  - region\n- name: storage_gb_month\n  description: Block storage attached to vmstorage.\n  unit: GB-month\n  aggregation: avg\n  dimensions:\n  - cluster_id\n- name: network_egress\n  description: Egress bytes from VictoriaMetrics to consumers (Grafana, alerts, federation).\n  unit: GB\n  aggregation: sum\n  dimensions:\n\
  \  - region\nprinciples:\n- name: Visibility\n  description: Use vmstats / per-tenant stats for chargeback; combine with cloud cost-export.\n- name: Allocation\n  description: Multi-tenant clusters allocate via vmselect/vminsert tenantID; otherwise tag clusters by team/env.\n- name: Optimization\n  description: Apply Enterprise downsampling and retention rules; reduce label cardinality; right-size vminsert/vmselect.\n- name: Accountability\n  description: Assign cluster owners; set per-tenant active-series budgets in Enterprise.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/victoriametrics/refs/heads/main/finops/victoriametrics-finops.yml
sources:
- https://victoriametrics.com/products/enterprise/
- https://victoriametrics.com/products/cloud/
- https://docs.victoriametrics.com/PerTenantStatistic.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Database
- Time-Series
- Monitoring
- Open Source
- Prometheus
- FinOps
- Cost Management
- FOCUS
---
