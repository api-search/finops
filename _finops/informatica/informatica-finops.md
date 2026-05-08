---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: informatica-platform-rest-api-openapi.yml
  format: yaml
  label: Informatica Platform REST API
  slug: informatica
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/informatica/refs/heads/main/openapi/informatica-platform-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps shape for Informatica IDMC. Billing is consumption-based via Informatica Processing Units (IPUs) drawn from a pre-purchased pool, with MDM additionally metered per-domain records. The single fungible meter (IPU) maps cleanly to FOCUS Usage charges and supports per-service attribution.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Informatica LLC
  PricingCategory: Pay-As-You-Go
  PricingUnit: IPU
  ProviderName: Informatica
  PublisherName: Informatica LLC
  ServiceCategory: Data Integration + Management
  ServiceName: Informatica IDMC
layout: finops
meters:
- aggregation: sum
  description: Informatica Processing Units consumed across IDMC services
  dimensions:
  - service
  - org
  - project
  - runtime_environment
  name: ipu_consumption
  unit: IPU
- aggregation: max
  description: Mastered records under management per MDM domain
  dimensions:
  - domain
  - environment
  name: mdm_records
  unit: record-month
- aggregation: max
  description: Secure Agents in operation
  dimensions:
  - runtime_environment
  - region
  name: secure_agents
  unit: agent-month
name: Informatica Finops
provider_name: Informatica
provider_slug: informatica
publisher_name: Informatica LLC
service_category: Data Integration + Management
slug: informatica-finops
source_filename: informatica-finops.yml
source_heading: FinOps Profile
source_url: https://www.informatica.com/products/cloud-integration/pricing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Informatica\nproviderId: informatica\npublisherName: Informatica LLC\nserviceCategory: Data Integration + Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Data Integration\n  - iPaaS\n  - IDMC\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Informatica IDMC. Billing is consumption-based via Informatica\n  Processing Units (IPUs) drawn from a pre-purchased pool, with MDM additionally metered per-domain\n  records. The single fungible meter (IPU) maps cleanly to FOCUS Usage charges and supports per-service\n  attribution.\nnotes: Per-IPU dollar amount not publicly disclosed; the IPU itself\
  \ is the canonical meter. Reconcile\n  against the customer's Cloud and Product Description Schedule and IDMC Consumption dashboard.\nsources:\n  - https://www.informatica.com/products/cloud-integration/pricing.html\nprinciples:\n  - name: Visibility\n    description: Use the IDMC Consumption Dashboard and the Audit Log API to see per-service IPU consumption\n      and project burn-rate against the pre-purchased pool.\n  - name: Allocation\n    description: Tag projects, folders, and runtime environments by team / business unit so IPU consumption\n      can be attributed; export consumption to FinOps tooling via the Cloud Audit Log API.\n  - name: Optimization\n    description: Tune CDI-e job parallelism, prefer push-down compute, retire low-value scheduled jobs,\n      and right-size Secure Agents to lower IPU burn-rate per job.\n  - name: Accountability\n    description: Designate a data-engineering FinOps owner with monthly IPU-burn review; set IPU consumption\n      thresholds and\
  \ alerts in the admin UI to flag anomalies before pool exhaustion.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName:\
  \ Informatica IDMC\n  ServiceCategory: Data Integration + Management\n  ProviderName: Informatica\n  PublisherName: Informatica LLC\n  InvoiceIssuerName: Informatica LLC\n  PricingCategory: Pay-As-You-Go\n  PricingUnit: IPU\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: ipu_consumption\n    description: Informatica Processing Units consumed across IDMC services\n    unit: IPU\n    aggregation: sum\n    dimensions:\n      - service\n      - org\n      - project\n      - runtime_environment\n  - name: mdm_records\n    description: Mastered records under management per MDM domain\n    unit: record-month\n    aggregation: max\n    dimensions:\n      - domain\n      - environment\n  - name: secure_agents\n    description: Secure Agents in operation\n    unit: agent-month\n    aggregation: max\n    dimensions:\n      - runtime_environment\n      - region\napis:\n  - name: Informatica IDMC REST API\n    baseURL: https://{pod}.informaticacloud.com\n    serviceCategory: API\n\
  \  - name: Informatica API & App Integration\n    baseURL: https://{pod}.informaticacloud.com\n    serviceCategory: API\n  - name: Informatica Cloud Data Integration\n    baseURL: https://{pod}.informaticacloud.com\n    serviceCategory: API\nunitEconomics:\n  - name: IPU Cost per Job-Minute\n    metric: billed_cost / job_minutes\n    target: TBD\n  - name: IPU Cost per Mastered Record\n    metric: billed_cost / mdm_records\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/informatica/refs/heads/main/finops/informatica-finops.yml
sources:
- https://www.informatica.com/products/cloud-integration/pricing.html
specification: FinOps Framework
tags:
- Data Integration
- iPaaS
- IDMC
- FinOps
- FOCUS
---
