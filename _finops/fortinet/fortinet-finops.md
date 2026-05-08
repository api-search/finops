---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Perpetual + Subscription
description: FOCUS-aligned FinOps mapping for Fortinet — appliance + FortiCare entitlement model with FortiCloud SaaS subscriptions layered on top. APIs are bundled with the underlying product license rather than sold as separate API plans.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Fortinet, Inc. (or reseller of record)
  ProviderName: Fortinet, Inc.
  PublisherName: Fortinet, Inc.
  ServiceCategory: Cybersecurity / Networking
  ServiceName: Fortinet
layout: finops
meters:
- aggregation: max
  description: Hardware/VM appliances under active license (FortiGate, FortiSwitch, FortiAP, etc.)
  dimensions:
  - product
  - model
  - site
  name: appliances
  unit: appliance-year
- aggregation: max
  description: FortiCare support and entitlement renewal per appliance
  dimensions:
  - tier
  - appliance
  name: forticare_renewal
  unit: appliance-year
- aggregation: max
  description: User-based FortiCloud subscriptions (FortiSASE, FortiAuthenticator Cloud, etc.)
  dimensions:
  - service
  - region
  name: forticloud_users
  unit: seat-year
- aggregation: max
  description: Bandwidth-based FortiCloud subscriptions (FortiSASE secure web gateway, etc.)
  dimensions:
  - service
  name: forticloud_bandwidth
  unit: Gbps-month
- aggregation: sum
  description: Log/event volume ingested into FortiAnalyzer Cloud
  dimensions:
  - service
  - device
  name: forticloud_log_volume
  unit: GB
name: Fortinet Finops
provider_name: Fortinet
provider_slug: fortinet
publisher_name: Fortinet, Inc.
service_category: Cybersecurity / Networking
slug: fortinet-finops
source_filename: fortinet-finops.yml
source_heading: FinOps Profile
source_url: https://www.fortinet.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Fortinet\nproviderId: fortinet\npublisherName: Fortinet, Inc.\nserviceCategory: Cybersecurity / Networking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cybersecurity\n  - Networking\n  - Firewall\n  - SASE\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps mapping for Fortinet — appliance + FortiCare entitlement model with FortiCloud SaaS subscriptions layered on top. APIs are bundled with the underlying product license rather than sold as separate API plans.\nnotes: No public list pricing. Meters reflect typical Fortinet invoice patterns (per-appliance license, per-user / per-bandwidth FortiCloud, FortiCare\
  \ renewal).\nsources:\n  - https://www.fortinet.com/products\n  - https://www.fortinet.com/products/management/forticloud\nbillingModel:\n  pricingCategory: Perpetual + Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Fortinet\n  ServiceCategory: Cybersecurity / Networking\n  ProviderName: Fortinet, Inc.\n  PublisherName: Fortinet, Inc.\n  InvoiceIssuerName: Fortinet, Inc. (or reseller of record)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: appliances\n    description: Hardware/VM appliances under active license (FortiGate, FortiSwitch, FortiAP, etc.)\n    unit: appliance-year\n    aggregation: max\n    dimensions:\n      - product\n      - model\n      - site\n  - name: forticare_renewal\n    description: FortiCare support and entitlement renewal per appliance\n    unit: appliance-year\n    aggregation: max\n    dimensions:\n\
  \      - tier\n      - appliance\n  - name: forticloud_users\n    description: User-based FortiCloud subscriptions (FortiSASE, FortiAuthenticator Cloud, etc.)\n    unit: seat-year\n    aggregation: max\n    dimensions:\n      - service\n      - region\n  - name: forticloud_bandwidth\n    description: Bandwidth-based FortiCloud subscriptions (FortiSASE secure web gateway, etc.)\n    unit: Gbps-month\n    aggregation: max\n    dimensions:\n      - service\n  - name: forticloud_log_volume\n    description: Log/event volume ingested into FortiAnalyzer Cloud\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - service\n      - device\nprinciples:\n  - name: Visibility\n    description: Pull FortiCloud admin reports and FortiManager inventory; reconcile active-appliance counts against the FortiCare renewal invoice to surface decommissioned hardware still on the bill.\n  - name: Allocation\n    description: Tag appliances and FortiCloud tenants by site/business-unit for chargeback; FortiAnalyzer's\
  \ logs can be partitioned by ADOM for finer attribution.\n  - name: Optimization\n    description: Right-size FortiCare tiers (8x5 vs 24x7 vs 360); decommission unused appliances; consolidate FortiCloud subscriptions onto an enterprise agreement; archive old FortiAnalyzer logs to cheaper tiers.\n  - name: Accountability\n    description: Network/security operations owns the appliance fleet; finance audits FortiCare renewal lists annually against the asset inventory.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fortinet/refs/heads/main/finops/fortinet-finops.yml
sources:
- https://www.fortinet.com/products
- https://www.fortinet.com/products/management/forticloud
specification: FinOps Framework
tags:
- Cybersecurity
- Networking
- Firewall
- SASE
- FinOps
- FOCUS
---
