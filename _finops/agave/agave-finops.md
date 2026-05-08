---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: agave-unified-api-openapi.yml
  format: yaml
  label: Agave Unified Construction API
  slug: unified-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/agave/refs/heads/main/openapi/agave-unified-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Custom Contract
description: FOCUS-aligned FinOps shape for Agave's Unified Construction API. Agave is sold as a custom contract scoped by systems integrated, companies, modules, and customizations; there is no public rate card.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Agave
  ProviderName: Agave
  PublisherName: Agave
  ServiceCategory: Construction Tech / Integration
  ServiceName: Agave Unified Construction API
layout: finops
meters:
- aggregation: sum
  description: Annual or multi-year custom contract fee
  dimensions:
  - module
  - source_system
  - company_count
  name: contract_subscription
  unit: contract
- aggregation: count
  description: Distinct ERP / construction-platform integrations covered by the contract
  dimensions:
  - source_system
  - deployment_type
  name: source_system_connections
  unit: connection
- aggregation: sum
  description: API requests Agave makes downstream to integrated source systems on the customer's behalf
  dimensions:
  - source_system
  - module
  name: integration_requests
  unit: request
name: Agave Finops
provider_name: Agave
provider_slug: agave
publisher_name: Agave
service_category: Construction Tech / Integration
slug: agave-finops
source_filename: agave-finops.yml
source_heading: FinOps Profile
source_url: https://useagave.com/contractors/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Agave\nproviderId: agave\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Agave\nserviceCategory: Construction Tech / Integration\ntags:\n  - Accounting\n  - Construction\n  - Integration\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Agave's Unified Construction API. Agave is sold as a custom\n  contract scoped by systems integrated, companies, modules, and customizations; there is no public\n  rate card.\nnotes: No public pricing; meters reflect the contract dimensions Agave uses to scope quotes (modules,\n  companies, source systems) plus integration request volume that customers should track\
  \ for unit\n  economics.\nsources:\n  - https://useagave.com/contractors/pricing\n  - https://docs.agaveapi.com/\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Agave Unified Construction API\n  ServiceCategory: Construction Tech / Integration\n  ProviderName: Agave\n  PublisherName: Agave\n  InvoiceIssuerName: Agave\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_subscription\n    description: Annual or multi-year custom contract fee\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - module\n      - source_system\n      - company_count\n  - name: source_system_connections\n    description: Distinct ERP / construction-platform integrations covered by the contract\n    unit: connection\n    aggregation: count\n    dimensions:\n      - source_system\n      - deployment_type\n  - name: integration_requests\n\
  \    description: API requests Agave makes downstream to integrated source systems on the customer's behalf\n    unit: request\n    aggregation: sum\n    dimensions:\n      - source_system\n      - module\nprinciples:\n  - name: Visibility\n    description: Track Agave costs at contract-renewal granularity since pricing is annual and custom;\n      pair with Agave's webhook/event logs to monitor sync volume per source system.\n  - name: Allocation\n    description: Allocate cost by module (Core / AP / AR / Workforce / Forecast) and by company entity\n      since both factor directly into Agave's scoping formula.\n  - name: Optimization\n    description: Optimize by consolidating which source ERPs are connected, deferring optional modules\n      until they're justified, and minimizing customizations against Agave defaults to keep quotes lean.\n  - name: Accountability\n    description: Construction operations or IT integration owners typically hold the Agave budget; align\n      renewal\
  \ review with the underlying ERP contracts whose data Agave is syncing.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/agave/refs/heads/main/finops/agave-finops.yml
sources:
- https://useagave.com/contractors/pricing
- https://docs.agaveapi.com/
specification: FinOps Framework
tags:
- Accounting
- Construction
- Integration
- FinOps
- FOCUS
---
