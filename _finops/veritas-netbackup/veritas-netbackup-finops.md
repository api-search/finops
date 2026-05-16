---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veritas-netbackup-rest-api-openapi.yml
  format: yaml
  label: Veritas NetBackup REST API
  slug: veritas-netbackup-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veritas-netbackup/refs/heads/main/openapi/veritas-netbackup-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Veritas NetBackup: enterprise software license (typically front-end-TB sized) with no public pricing or usage/billing API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Veritas Technologies LLC
  ProviderName: Veritas
  PublisherName: Veritas Technologies LLC
  ServiceCategory: Backup / Data Protection
  ServiceName: Veritas NetBackup
layout: finops
meters:
- aggregation: sum
  description: Annual NetBackup license line; sizing dimensions (front-end TB, sockets, appliance count) negotiated in the order form.
  name: software_license
  unit: varies
name: Veritas Netbackup Finops
provider_name: Veritas NetBackup
provider_slug: veritas-netbackup
publisher_name: Veritas Technologies LLC
service_category: Backup / Data Protection
slug: veritas-netbackup-finops
source_filename: veritas-netbackup-finops.yml
source_heading: FinOps Profile
source_url: https://www.veritas.com/protection/netbackup
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veritas NetBackup\nproviderId: veritas-netbackup\npublisherName: Veritas Technologies LLC\nserviceCategory: Backup / Data Protection\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Backup\n  - Data Protection\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Veritas NetBackup: enterprise software license (typically front-end-TB\n  sized) with no public pricing or usage/billing API.'\nsources:\n  - https://www.veritas.com/protection/netbackup\nnotes: No public pricing or billing API; product page returned 403 to crawlers. Meters are not invented;\n  reconciliation deferred.\nbillingModel:\n  pricingCategory:\
  \ Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Veritas NetBackup\n  ServiceCategory: Backup / Data Protection\n  ProviderName: Veritas\n  PublisherName: Veritas Technologies LLC\n  InvoiceIssuerName: Veritas Technologies LLC\n  BillingCurrency: USD\nmeters:\n  - name: software_license\n    description: Annual NetBackup license line; sizing dimensions (front-end TB, sockets, appliance count)\n      negotiated in the order form.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into protected data and job activity is local to the customer's NetBackup\n      primary server (NetBackup IT Analytics, OpsCenter, REST API); there is no public cost API.\n  - name: Allocation\n    description: Allocation is per protected workload / business unit, mapped via NetBackup policies\n      and consumed against the front-end-TB entitlement.\n  - name: Optimization\n\
  \    description: 'Optimization levers are deduplication and retention tuning, decommissioning unneeded\n      policies, and right-sizing front-end-TB at renewal.'\n  - name: Accountability\n    description: Accountability sits with the backup / data-protection team that operates the NetBackup\n      primary server; finance owns the annual subscription line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veritas-netbackup/refs/heads/main/finops/veritas-netbackup-finops.yml
sources:
- https://www.veritas.com/protection/netbackup
specification: FinOps Framework
tags:
- Backup
- Data Protection
- FinOps
- FOCUS
---
