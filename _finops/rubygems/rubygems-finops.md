---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rubygems-gems-api-openapi.yml
  format: yaml
  label: RubyGems Gems API
  slug: gems-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rubygems/refs/heads/main/openapi/rubygems-gems-api-openapi.yml
- filename: rubygems-api-v2-openapi.yml
  format: yaml
  label: RubyGems API V2
  slug: api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rubygems/refs/heads/main/openapi/rubygems-api-v2-openapi.yml
- filename: rubygems-downloads-api-openapi.yml
  format: yaml
  label: RubyGems Downloads API
  slug: downloads-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rubygems/refs/heads/main/openapi/rubygems-downloads-api-openapi.yml
- filename: rubygems-search-api-openapi.yml
  format: yaml
  label: RubyGems Search API
  slug: search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rubygems/refs/heads/main/openapi/rubygems-search-api-openapi.yml
- filename: rubygems-activity-api-openapi.yml
  format: yaml
  label: RubyGems Activity API
  slug: activity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rubygems/refs/heads/main/openapi/rubygems-activity-api-openapi.yml
- filename: rubygems-webhooks-api-openapi.yml
  format: yaml
  label: RubyGems Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rubygems/refs/heads/main/openapi/rubygems-webhooks-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories: []
  pricingCategory: Free / Community-Funded
description: 'FOCUS-aligned FinOps shape for RubyGems.org: a free, community-funded public registry with no direct billing. FinOps relevance is indirect — internal cost of CI bandwidth and storage when consuming the registry — rather than vendor invoice reconciliation.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Ruby Central, Inc.
  ProviderName: RubyGems
  PublisherName: Ruby Central, Inc.
  ServiceCategory: Developer Tools / Package Registry
  ServiceName: RubyGems.org
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - source_ip
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - account
  name: gem_publishes
  unit: request
- aggregation: sum
  dimensions:
  - source_ip
  name: dependency_index_fetches
  unit: request
- aggregation: sum
  dimensions:
  - gem
  name: download_bytes
  unit: GB
name: Rubygems Finops
provider_name: RubyGems
provider_slug: rubygems
publisher_name: Ruby Central, Inc.
service_category: Developer Tools / Package Registry
slug: rubygems-finops
source_filename: rubygems-finops.yml
source_heading: FinOps Profile
source_url: https://guides.rubygems.org/rubygems-org-rate-limits/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: RubyGems\nproviderId: rubygems\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Ruby\n  - Package Manager\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for RubyGems.org: a free, community-funded public registry with\n  no direct billing. FinOps relevance is indirect — internal cost of CI bandwidth and storage when consuming\n  the registry — rather than vendor invoice reconciliation.'\nsources:\n  - https://guides.rubygems.org/rubygems-org-rate-limits/\n  - https://rubygems.org/pages/sponsors\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ruby Central, Inc.\n\
  serviceCategory: Developer Tools / Package Registry\nbillingModel:\n  pricingCategory: Free / Community-Funded\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: RubyGems.org\n  ServiceCategory: Developer Tools / Package Registry\n  ProviderName: RubyGems\n  PublisherName: Ruby Central, Inc.\n  InvoiceIssuerName: Ruby Central, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - source_ip\n  - name: gem_publishes\n    unit: request\n    aggregation: sum\n    dimensions:\n      - account\n  - name: dependency_index_fetches\n    unit: request\n    aggregation: sum\n    dimensions:\n      - source_ip\n  - name: download_bytes\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - gem\nprinciples:\n  - name: Visibility\n    description: There is no per-consumer billing telemetry from RubyGems.org. Visibility comes from the\n  \
  \    consumer side (CI logs, mirror access logs, Bundler resolution traces) rather than provider-issued\n      invoices.\n  - name: Allocation\n    description: Allocate the indirect costs (CI minutes, internal mirror storage/egress) by tagging Bundler\n      / gem fetches with the project, environment, and pipeline that triggered them.\n  - name: Optimization\n    description: Use the compact index endpoints, run an internal gem mirror, cache aggressively in CI,\n      and avoid hitting POST /api/v1/gems retry loops to stay well below load-balancer and rack-attack\n      thresholds.\n  - name: Accountability\n    description: Engineering teams own their CI consumption and dependency hygiene. Sustained abusive traffic\n      is escalated through support@rubygems.org.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rubygems/refs/heads/main/finops/rubygems-finops.yml
sources:
- https://guides.rubygems.org/rubygems-org-rate-limits/
- https://rubygems.org/pages/sponsors
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Ruby
- Package Manager
- Open Source
- FinOps
- FOCUS
---
