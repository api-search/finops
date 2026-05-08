---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: huntington-bank-treasury-management-api-openapi.yml
  format: yaml
  label: Huntington Bank Treasury Management API
  slug: treasury-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/huntington-bancshares/refs/heads/main/openapi/huntington-bank-treasury-management-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly account analysis
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Bundled (Commercial Banking Contract)
description: 'FOCUS-aligned FinOps for Huntington Bank treasury APIs: API access is bundled with the commercial banking treasury management contract. Cost surface is account-analysis fees, per-transaction fees (ACH, wire, RTP), and ERP-integration service charges rather than per-call API consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: The Huntington National Bank
  ProviderName: Huntington Bancshares
  PublisherName: The Huntington National Bank
  ServiceCategory: Banking & Treasury Management
  ServiceName: Huntington Treasury Management API
layout: finops
meters:
- aggregation: sum
  description: Monthly account-analysis charges from the treasury management agreement; the primary cost surface for API-enabled treasury workflows.
  dimensions:
  - account
  - service_code
  name: account_analysis_fees
  unit: month
- aggregation: sum
  description: ACH origination and receipt transaction count submitted via the API.
  dimensions:
  - direction
  - account
  name: ach_transactions
  unit: transaction
- aggregation: sum
  description: Wire-transfer count submitted via the API; typically priced per wire at the contracted rate.
  dimensions:
  - type
  - account
  name: wire_transactions
  unit: transaction
- aggregation: sum
  description: Real-Time Payments / FedNow transactions submitted via the API.
  dimensions:
  - account
  name: rtp_transactions
  unit: transaction
- aggregation: sum
  description: API call volume across the 500+ interfaces; not directly billed but useful for capacity and quota monitoring.
  dimensions:
  - api
  - consumer_key
  name: api_requests
  unit: request
name: Huntington Bancshares Finops
provider_name: Huntington Bancshares
provider_slug: huntington-bancshares
publisher_name: The Huntington National Bank
service_category: Banking & Treasury Management
slug: huntington-bancshares-finops
source_filename: huntington-bancshares-finops.yml
source_heading: FinOps Profile
source_url: https://hnbdevportal.huntington.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Huntington Bancshares\nproviderId: huntington-bancshares\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Treasury\n  - Payments\ndescription: 'FOCUS-aligned FinOps for Huntington Bank treasury APIs: API access is bundled with\n  the commercial banking treasury management contract. Cost surface is account-analysis fees, per-transaction\n  fees (ACH, wire, RTP), and ERP-integration service charges rather than per-call API consumption.'\nnotes: Per-call API pricing is not published; cost flows through the broader Huntington commercial\n  banking relationship.\nsources:\n  - https://hnbdevportal.huntington.com/\n  - https://www.huntington.com/Commercial/treasury-management\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n \
  \ dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Huntington National Bank\nserviceCategory: Banking & Treasury Management\nbillingModel:\n  pricingCategory: Bundled (Commercial Banking Contract)\n  billingFrequency: Monthly account analysis\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Huntington Treasury Management API\n  ServiceCategory: Banking & Treasury Management\n  ProviderName: Huntington Bancshares\n  PublisherName: The Huntington National Bank\n  InvoiceIssuerName: The Huntington National Bank\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: account_analysis_fees\n    description: Monthly account-analysis charges from the treasury management agreement; the primary\n      cost surface for API-enabled treasury workflows.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\n      - service_code\n  - name:\
  \ ach_transactions\n    description: ACH origination and receipt transaction count submitted via the API.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - direction\n      - account\n  - name: wire_transactions\n    description: Wire-transfer count submitted via the API; typically priced per wire at the contracted\n      rate.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - type\n      - account\n  - name: rtp_transactions\n    description: Real-Time Payments / FedNow transactions submitted via the API.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - account\n  - name: api_requests\n    description: API call volume across the 500+ interfaces; not directly billed but useful for capacity\n      and quota monitoring.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - consumer_key\nprinciples:\n  - name: Visibility\n    description: Reconcile monthly account-analysis statements against API transaction\
  \ logs. Use\n      the developer portal usage view (when surfaced) to track per-consumer-key call volume against\n      Apigee quotas.\n  - name: Allocation\n    description: Tag API consumer keys per ERP system / business unit. Map account-analysis service\n      codes back to the consuming team for chargeback.\n  - name: Optimization\n    description: Batch ACH origination where possible; minimize same-day wire usage in favor of standard\n      ACH or RTP for predictable lower fees; cache reference data (account balances, payee lists)\n      to reduce redundant API calls; review unused services on the account-analysis statement quarterly.\n  - name: Accountability\n    description: Designate a treasury-operations owner accountable for per-transaction fee variance.\n      Establish SLAs with Huntington partner enablement for quota raises and incident response.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/huntington-bancshares/refs/heads/main/finops/huntington-bancshares-finops.yml
sources:
- https://hnbdevportal.huntington.com/
- https://www.huntington.com/Commercial/treasury-management
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Treasury
- Payments
---
