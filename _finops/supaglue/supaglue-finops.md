---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: supaglue-management-api-openapi.yml
  format: yaml
  label: Supaglue Management API
  slug: management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/openapi/supaglue-management-api-openapi.yml
- filename: supaglue-crm-api-openapi.yml
  format: yaml
  label: Supaglue Unified CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/openapi/supaglue-crm-api-openapi.yml
- filename: supaglue-engagement-api-openapi.yml
  format: yaml
  label: Supaglue Unified Engagement API
  slug: engagement-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/openapi/supaglue-engagement-api-openapi.yml
- filename: supaglue-ticketing-api-openapi.yml
  format: yaml
  label: Supaglue Unified Ticketing API
  slug: ticketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/openapi/supaglue-ticketing-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Adjustment
  pricingCategory: Self-Hosted (Open Source)
description: Supaglue is an archived open-source project (MIT), no longer offered as a hosted service. There is no vendor invoice surface; deployment cost is entirely the self-hoster's infrastructure cost.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ''
  ProviderName: Supaglue Labs
  PublisherName: Supaglue Labs (archived)
  ServiceCategory: Unified CRM API
  ServiceName: Supaglue
layout: finops
meters:
- aggregation: sum
  description: The deployer's own compute, database, and egress; no vendor meter
  name: self_hosted_infrastructure
  unit: varies
name: Supaglue Finops
provider_name: Supaglue
provider_slug: supaglue
publisher_name: Supaglue Labs (archived)
service_category: Unified CRM API (Open Source)
slug: supaglue-finops
source_filename: supaglue-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/supaglue-labs/supaglue
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Supaglue\nproviderId: supaglue\npublisherName: Supaglue Labs (archived)\nserviceCategory: Unified CRM API (Open Source)\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Open Source\n  - Unified API\ndescription: Supaglue is an archived open-source project (MIT), no longer offered as a hosted service.\n  There is no vendor invoice surface; deployment cost is entirely the self-hoster's infrastructure cost.\nsources:\n  - https://github.com/supaglue-labs/supaglue\nnotes: 'Reconciliation marked false: project archived 2024-03-10; no hosted billing surface to reconcile.'\nbillingModel:\n  pricingCategory:\
  \ Self-Hosted (Open Source)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Supaglue\n  ServiceCategory: Unified CRM API\n  ProviderName: Supaglue Labs\n  PublisherName: Supaglue Labs (archived)\n  InvoiceIssuerName: ''\n  BillingCurrency: USD\nmeters:\n  - name: self_hosted_infrastructure\n    description: The deployer's own compute, database, and egress; no vendor meter\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the self-hoster's own observability stack on top of the deployment;\n      Supaglue itself emits no usage telemetry to a vendor.\n  - name: Allocation\n    description: Allocate the self-hosted footprint via the underlying cloud provider's tagging and\n      cost-allocation mechanisms.\n  - name: Optimization\n    description: Optimization levers are the standard self-hosted ones (right-size, autoscale, cache\n      upstream CRM responses)\
  \ plus migration to a maintained alternative since Supaglue is archived.\n  - name: Accountability\n    description: Ownership rests with the platform-engineering team running the deployment; budget alerts\n      via the underlying cloud account.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/supaglue/refs/heads/main/finops/supaglue-finops.yml
sources:
- https://github.com/supaglue-labs/supaglue
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Open Source
- Unified API
---
