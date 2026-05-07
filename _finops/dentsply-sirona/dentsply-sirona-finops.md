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
  - Purchase
  - Usage
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: SaaS Subscription + Hardware Bundle
description: 'FOCUS-aligned FinOps for Dentsply Sirona DS Core and intraoral imaging APIs: SaaS subscription for the DS Core cloud platform plus modality-bundled API access on hardware. No per-call API charges.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Dentsply Sirona, Inc.
  PricingCategory: Subscription + Hardware
  PricingUnit: practice
  ProviderName: Dentsply Sirona
  PublisherName: Dentsply Sirona, Inc.
  ServiceCategory: Dental Technology / Practice Management
  ServiceName: DS Core API
layout: finops
meters:
- aggregation: sum
  description: DS Core subscription seats / practices
  dimensions:
  - practice
  - region
  name: ds_core_subscription
  unit: month
- aggregation: max
  description: Imaging storage consumed in DS Core
  dimensions:
  - practice
  name: imaging_storage
  unit: GB-month
- aggregation: max
  description: Connected intraoral imaging modalities (Schick, Primescan, CEREC)
  dimensions:
  - practice
  - modality_type
  name: modality_devices
  unit: device
- aggregation: max
  description: Partner / ISV apps installed in a DS Core practice
  dimensions:
  - practice
  - app
  name: partner_app_installs
  unit: install
name: Dentsply Sirona Finops
provider_name: Dentsply Sirona
provider_slug: dentsply-sirona
publisher_name: Dentsply Sirona, Inc.
service_category: Dental Technology / Practice Management
slug: dentsply-sirona-finops
source_filename: dentsply-sirona-finops.yml
source_heading: FinOps Profile
source_url: https://www.dentsplysirona.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dentsply Sirona\nproviderId: dentsply-sirona\npublisherName: Dentsply Sirona, Inc.\nserviceCategory: Dental Technology / Practice Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Dentsply Sirona does not publish API pricing. DS Core is sold as a per-practice subscription, with\n  imaging-modality APIs included with hardware purchase. FinOps shape is SaaS subscription plus hardware\n  CapEx; API consumption is not directly billed. Reconcile against DS Core subscription invoices when available.\ntags:\n  - Dental\n  - DS Core\n  - Practice Management\n  - Imaging\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Dentsply Sirona DS Core and intraoral\
  \ imaging APIs: SaaS subscription\n  for the DS Core cloud platform plus modality-bundled API access on hardware. No per-call API charges.'\nsources:\n  - https://www.dentsplysirona.com/\n  - https://developer.dscore.com/\nprinciples:\n  - name: Visibility\n    description: Track DS Core seat and practice counts via the practice admin console; reconcile imaging\n      storage and partner-app entitlements against the DS Core subscription terms.\n  - name: Allocation\n    description: Allocate DS Core spend by practice location and modality (CEREC, Primescan, Schick) for\n      multi-site dental groups; tag partner-app installs to the practice that activated them.\n  - name: Optimization\n    description: Right-size DS Core seat counts during quarterly reviews, archive old imaging studies\n      to manage storage, and consolidate partner-app subscriptions to avoid double-paying for overlapping\n      capabilities.\n  - name: Accountability\n    description: Practice owner / DSO operations\
  \ leader owns DS Core renewal and seat hygiene; integration\n      partners own usage of their respective DS Core APIs.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: SaaS Subscription + Hardware Bundle\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName:\
  \ DS Core API\n  ServiceCategory: Dental Technology / Practice Management\n  ProviderName: Dentsply Sirona\n  PublisherName: Dentsply Sirona, Inc.\n  InvoiceIssuerName: Dentsply Sirona, Inc.\n  PricingCategory: Subscription + Hardware\n  PricingUnit: practice\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: ds_core_subscription\n    description: DS Core subscription seats / practices\n    unit: month\n    aggregation: sum\n    dimensions:\n      - practice\n      - region\n  - name: imaging_storage\n    description: Imaging storage consumed in DS Core\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - practice\n  - name: modality_devices\n    description: Connected intraoral imaging modalities (Schick, Primescan, CEREC)\n    unit: device\n    aggregation: max\n    dimensions:\n      - practice\n      - modality_type\n  - name: partner_app_installs\n    description: Partner / ISV apps installed in a DS Core practice\n    unit: install\n    aggregation:\
  \ max\n    dimensions:\n      - practice\n      - app\napis:\n  - name: DS Core API\n    baseURL: https://api.dscore.com\n    tags:\n      - DS Core\n      - Imaging\n      - Lab Management\n      - Patient Data\n      - Practice Management\n      - SSO\n    serviceName: DS Core API\n    serviceCategory: API\n  - name: Dentsply Sirona Intraoral Imaging Modality API\n    baseURL: https://api.dscore.com\n    tags:\n      - Imaging\n      - Intraoral\n      - Modality\n      - Sensors\n    serviceName: Dentsply Sirona Intraoral Imaging Modality API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Practice\n    metric: ds_core_subscription_cost / practices\n    target: TBD\n  - name: Cost per Modality Device\n    metric: ds_core_subscription_cost / modality_devices\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dentsply-sirona/refs/heads/main/finops/dentsply-sirona-finops.yml
sources:
- https://www.dentsplysirona.com/
- https://developer.dscore.com/
specification: FinOps Framework
tags:
- Dental
- DS Core
- Practice Management
- Imaging
- FinOps
- FOCUS
---
