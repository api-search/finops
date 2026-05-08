---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: supabase-management-api-openapi.yml
  format: yaml
  label: Supabase Management API
  slug: management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supabase/refs/heads/main/openapi/supabase-management-api-openapi.yml
- filename: supabase-auth-api-openapi.yml
  format: yaml
  label: Supabase Auth API
  slug: auth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supabase/refs/heads/main/openapi/supabase-auth-api-openapi.yml
- filename: supabase-storage-api-openapi.yml
  format: yaml
  label: Supabase Storage API
  slug: storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supabase/refs/heads/main/openapi/supabase-storage-api-openapi.yml
- filename: supabase-database-rest-api-openapi.yml
  format: yaml
  label: Supabase Database REST API
  slug: database-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supabase/refs/heads/main/openapi/supabase-database-rest-api-openapi.yml
- filename: supabase-edge-functions-api-openapi.yml
  format: yaml
  label: Supabase Edge Functions API
  slug: edge-functions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supabase/refs/heads/main/openapi/supabase-edge-functions-api-openapi.yml
- filename: supabase-realtime-api-asyncapi.yml
  format: yaml
  label: Supabase Realtime API
  slug: realtime-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/supabase/refs/heads/main/asyncapi/supabase-realtime-api-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Usage-Based
description: FOCUS-aligned FinOps for Supabase.
focus_columns:
  BillingCurrency: USD
  ProviderName: Supabase
  PublisherName: Supabase Inc.
  ServiceCategory: Backend Platform
  ServiceName: Supabase
layout: finops
meters:
- aggregation: max
  dimensions:
  - project
  name: database_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - project
  - type
  name: egress
  unit: GB
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: max
  name: file_storage
  unit: GB-month
- aggregation: sum
  name: edge_function_invocations
  unit: invocation
- aggregation: sum
  dimensions:
  - instance_type
  name: compute_size_hours
  unit: compute-hour
- aggregation: sum
  name: realtime_messages
  unit: message
name: Supabase Finops
provider_name: Supabase
provider_slug: supabase
publisher_name: Supabase Inc.
service_category: Backend Platform
slug: supabase-finops
source_filename: supabase-finops.yml
source_heading: FinOps Profile
source_url: https://supabase.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Supabase\nproviderId: supabase\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Database\ndescription: FOCUS-aligned FinOps for Supabase.\nsources:\n  - https://supabase.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Supabase Inc.\nserviceCategory: Backend Platform\nbillingModel:\n  pricingCategory: Subscription + Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Supabase\n  ServiceCategory: Backend Platform\n  ProviderName: Supabase\n  PublisherName: Supabase Inc.\n  BillingCurrency: USD\nmeters:\n  - name: database_storage\n    unit: GB-month\n    aggregation: max\n \
  \   dimensions:\n      - project\n  - name: egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - project\n      - type\n  - name: monthly_active_users\n    unit: MAU\n    aggregation: max\n  - name: file_storage\n    unit: GB-month\n    aggregation: max\n  - name: edge_function_invocations\n    unit: invocation\n    aggregation: sum\n  - name: compute_size_hours\n    unit: compute-hour\n    aggregation: sum\n    dimensions:\n      - instance_type\n  - name: realtime_messages\n    unit: message\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use Usage tab per project; export billing JSON via Management API.\n  - name: Allocation\n    description: One project per env (dev/stage/prod); orgs for team-level cost roll-up.\n  - name: Optimization\n    description: Drop unused indexes; archive cold tables; right-size compute add-ons.\n  - name: Accountability\n    description: Cap MAU growth via Auth provider gating; quarterly compute right-sizing.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/supabase/refs/heads/main/finops/supabase-finops.yml
sources:
- https://supabase.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Database
---
