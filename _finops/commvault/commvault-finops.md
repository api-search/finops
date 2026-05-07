---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: commvault-rest-openapi.yml
  format: yaml
  label: Commvault REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commvault/refs/heads/main/openapi/commvault-rest-openapi.yml
- filename: commvault-command-center-openapi.yml
  format: yaml
  label: Commvault Command Center API
  slug: command-center-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commvault/refs/heads/main/openapi/commvault-command-center-openapi.yml
- filename: commvault-automation-openapi.yml
  format: yaml
  label: Commvault Automation API
  slug: automation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commvault/refs/heads/main/openapi/commvault-automation-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Pay-As-You-Go + Subscription
description: 'FOCUS-aligned FinOps for Commvault: per-user/month and per-TB/month meters across SaaS workload protection, plus quote-based Operational/Autonomous/Cyber Recovery software bundles. Volume discounts apply at common thresholds (50+ units or 750+ users).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Commvault Systems, Inc.
  ProviderName: Commvault
  PublisherName: Commvault Systems, Inc.
  ServiceCategory: Data Protection
  ServiceName: Commvault Cloud
layout: finops
meters:
- aggregation: sum
  dimensions:
  - workload
  - tier
  name: protected_users
  unit: seat-month
- aggregation: sum
  dimensions:
  - workload
  - tier
  - region
  name: protected_capacity
  unit: TB-month
- aggregation: sum
  dimensions:
  - hypervisor
  name: protected_vms
  unit: vm-month
- aggregation: sum
  dimensions:
  - storage_class
  name: archive_capacity
  unit: TB-month
- aggregation: sum
  dimensions:
  - bundle
  - entitlement
  name: software_subscription
  unit: month
name: Commvault Finops
provider_name: Commvault
provider_slug: commvault
publisher_name: Commvault Systems, Inc.
service_category: Data Protection
slug: commvault-finops
source_filename: commvault-finops.yml
source_heading: FinOps Profile
source_url: https://www.commvault.com/saas-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Commvault\nproviderId: commvault\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Backup\n  - Data Protection\ndescription: 'FOCUS-aligned FinOps for Commvault: per-user/month and per-TB/month meters across SaaS workload\n  protection, plus quote-based Operational/Autonomous/Cyber Recovery software bundles. Volume discounts\n  apply at common thresholds (50+ units or 750+ users).'\nsources:\n  - https://www.commvault.com/saas-pricing\n  - https://www.commvault.com/packaging\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Commvault Systems, Inc.\nserviceCategory: Data Protection\nbillingModel:\n  pricingCategory: Pay-As-You-Go +\
  \ Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Commvault Cloud\n  ServiceCategory: Data Protection\n  ProviderName: Commvault\n  PublisherName: Commvault Systems, Inc.\n  InvoiceIssuerName: Commvault Systems, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: protected_users\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - workload\n      - tier\n  - name: protected_capacity\n    unit: TB-month\n    aggregation: sum\n    dimensions:\n      - workload\n      - tier\n      - region\n  - name: protected_vms\n    unit: vm-month\n    aggregation: sum\n    dimensions:\n      - hypervisor\n  - name: archive_capacity\n    unit: TB-month\n    aggregation: sum\n    dimensions:\n      - storage_class\n  - name: software_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - bundle\n      - entitlement\n\
  principles:\n  - name: Visibility\n    description: Use the Commvault Cloud usage / metering reports to track protected users and TBs by\n      workload; reconcile against the CommServe inventory.\n  - name: Allocation\n    description: Tag clients/subclients with business unit, application, and environment so backup spend\n      can be charged back.\n  - name: Optimization\n    description: Tier cold data into File & Object Archive ($900/100 TB/month vs $58.50/TB for active);\n      decommission unused VMs from 10-packs; consolidate users across M365 tiers; cross volume thresholds\n      (50+ units or 750+ users) to unlock volume discounts.\n  - name: Accountability\n    description: Backup admin owns retention policies; data owner approves protection scope; finance owns\n      annual subscription renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/commvault/refs/heads/main/finops/commvault-finops.yml
sources:
- https://www.commvault.com/saas-pricing
- https://www.commvault.com/packaging
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Backup
- Data Protection
---
