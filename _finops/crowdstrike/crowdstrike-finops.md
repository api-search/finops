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
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for CrowdStrike Falcon: per-device subscription bundles (Go / Pro / Enterprise / Complete) billed monthly or annually, with module add-ons for Identity, Cloud, and SIEM.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CrowdStrike, Inc.
  PricingCategory: Subscription
  PricingUnit: device-month
  ProviderName: CrowdStrike
  PublisherName: CrowdStrike, Inc.
  ServiceCategory: Cybersecurity
  ServiceName: CrowdStrike Falcon
layout: finops
meters:
- aggregation: sum
  description: Count of licensed Falcon-protected devices
  dimensions:
  - bundle
  - billing_term
  - host_group
  - environment
  name: device_subscriptions
  unit: device-month
- aggregation: sum
  description: Add-on modules layered onto a base bundle (Identity, Cloud Workload, LogScale, Discover)
  dimensions:
  - module
  - bundle
  name: module_addons
  unit: module-month
- aggregation: sum
  description: Falcon Complete managed detection and response coverage
  dimensions:
  - host_group
  name: managed_service
  unit: device-month
- aggregation: sum
  description: API calls against the Falcon OAuth2 APIs (not separately billed; observed for capacity)
  dimensions:
  - api
  - endpoint
  - consumer
  name: api_requests
  unit: request
name: Crowdstrike Finops
provider_name: CrowdStrike
provider_slug: crowdstrike
publisher_name: CrowdStrike, Inc.
service_category: Cybersecurity
slug: crowdstrike-finops
source_filename: crowdstrike-finops.yml
source_heading: FinOps Profile
source_url: https://www.crowdstrike.com/en-us/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CrowdStrike\nproviderId: crowdstrike\npublisherName: CrowdStrike, Inc.\nserviceCategory: Cybersecurity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cybersecurity\n  - Endpoint Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for CrowdStrike Falcon: per-device subscription bundles (Go / Pro /\n  Enterprise / Complete) billed monthly or annually, with module add-ons for Identity, Cloud, and SIEM.'\nsources:\n  - https://www.crowdstrike.com/en-us/pricing/\nprinciples:\n  - name: Visibility\n    description: Use the Falcon console host inventory and Subscription Management API to\
  \ reconcile licensed\n      device counts against deployed sensors; export billing line items via the customer support portal.\n  - name: Allocation\n    description: Tag hosts with business unit / environment via Falcon host groups and sensor grouping\n      tags so per-device cost can be attributed to the consuming team.\n  - name: Optimization\n    description: Right-size bundles per device class (Go for SMB, Enterprise for high-risk endpoints);\n      retire dormant sensors promptly since billing is per provisioned device, and prefer annual billing\n      for the published discount.\n  - name: Accountability\n    description: Assign a security/IT budget owner who reviews monthly device counts, adds-on (Identity\n      Threat Protection, Cloud Workload Protection), and triggers true-up at renewal.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify\
  \ Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CrowdStrike Falcon\n  ServiceCategory: Cybersecurity\n  ProviderName: CrowdStrike\n  PublisherName: CrowdStrike, Inc.\n  InvoiceIssuerName: CrowdStrike, Inc.\n  PricingCategory: Subscription\n  PricingUnit: device-month\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name:\
  \ device_subscriptions\n    description: Count of licensed Falcon-protected devices\n    unit: device-month\n    aggregation: sum\n    dimensions:\n      - bundle\n      - billing_term\n      - host_group\n      - environment\n  - name: module_addons\n    description: Add-on modules layered onto a base bundle (Identity, Cloud Workload, LogScale, Discover)\n    unit: module-month\n    aggregation: sum\n    dimensions:\n      - module\n      - bundle\n  - name: managed_service\n    description: Falcon Complete managed detection and response coverage\n    unit: device-month\n    aggregation: sum\n    dimensions:\n      - host_group\n  - name: api_requests\n    description: API calls against the Falcon OAuth2 APIs (not separately billed; observed for capacity)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - consumer\napis:\n  - name: CrowdStrike API\n    baseURL: https://api.crowdstrike.com\n    tags:\n      - Cybersecurity\n      - Endpoint\
  \ Security\n    serviceName: CrowdStrike API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Protected Device\n    metric: billed_cost / device_subscriptions\n    target: TBD\n  - name: Cost per Detected Threat\n    metric: billed_cost / detections\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/crowdstrike/refs/heads/main/finops/crowdstrike-finops.yml
sources:
- https://www.crowdstrike.com/en-us/pricing/
specification: FinOps Framework
tags:
- Cybersecurity
- Endpoint Security
- FinOps
- Cost Management
- FOCUS
---
