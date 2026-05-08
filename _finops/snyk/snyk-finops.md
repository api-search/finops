---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Groups
  slug: rest-groups
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Organizations
  slug: rest-organizations
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Projects
  slug: rest-projects
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Issues
  slug: rest-issues
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Targets
  slug: rest-targets
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Integrations
  slug: rest-integrations
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Audit Logs
  slug: rest-audit-logs
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - SBOMs
  slug: rest-sboms
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Container Images
  slug: rest-container-images
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Custom Base Images
  slug: rest-custom-base-images
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Webhooks
  slug: rest-webhooks
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Export
  slug: rest-export
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Subscription (Per Contributing Developer)
description: FOCUS-aligned FinOps for Snyk. Snyk's commercial model is per-contributing-developer subscription, where a contributing developer is one who has committed to a Snyk-monitored private repo in the last 90 days. Self-serve Team is $25/dev/month with a 5-developer floor and 10-developer cap. Ignite is $1,260/dev/year for up to 50 developers. Enterprise is custom-quoted with optional add-ons (Snyk Learning, Snyk API & Web). Test counts on the Free tier are hard-capped, providing the lever to size up. The API itself is not separately metered - it is included with the tier.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Snyk Limited
  ProviderName: Snyk
  PublisherName: Snyk Limited
  ServiceCategory: Application Security
  ServiceName: Snyk
layout: finops
meters:
- aggregation: sum
  description: Recurring monthly or annual platform subscription fee for the active tier (Team, Ignite, or Enterprise).
  dimensions:
  - plan_tier
  - billing_cycle
  name: subscription_fee
  unit: month
- aggregation: max
  description: Count of contributing developers in the billing period - developers who have committed to a Snyk-monitored private repo in the last 90 days. Drives per-developer subscription totals.
  dimensions:
  - organization_id
  - group_id
  name: contributing_developers
  unit: developer
- aggregation: max
  description: Number of DAST web-application targets registered (10 included on Ignite, custom on Enterprise).
  dimensions:
  - organization_id
  name: dast_targets
  unit: target
- aggregation: sum
  description: Free-tier-only meter; tracks consumed monthly tests against the per-product cap (e.g. open-source, code, container, IaC). Drives upgrade trigger.
  dimensions:
  - organization_id
  - product
  name: tests_per_product
  unit: test
- aggregation: sum
  description: Subscription line for Enterprise add-ons such as Snyk Learning Management and Snyk API & Web (DAST).
  dimensions:
  - addon_name
  name: addon_subscription
  unit: month
name: Snyk Finops
provider_name: Snyk
provider_slug: snyk
publisher_name: Snyk Limited
service_category: Application Security
slug: snyk-finops
source_filename: snyk-finops.yml
source_heading: FinOps Profile
source_url: https://snyk.io/plans/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Snyk\nproviderId: snyk\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Security\n  - DevSecOps\n  - Vulnerability Management\n  - Application Security\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Snyk. Snyk's commercial model is per-contributing-developer\n  subscription, where a contributing developer is one who has committed to a\n  Snyk-monitored private repo in the last 90 days. Self-serve Team is $25/dev/month\n  with a 5-developer floor and 10-developer cap. Ignite is $1,260/dev/year for up to 50\n  developers. Enterprise is custom-quoted with optional add-ons (Snyk Learning,\n  Snyk API & Web). Test counts on the Free tier are hard-capped, providing the lever\n  to size up. The API itself is not separately metered - it is included with the tier.\nsources:\n  - https://snyk.io/plans/\n  - https://docs.snyk.io/snyk-api/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Snyk Limited\nserviceCategory: Application Security\nbillingModel:\n  pricingCategory: Subscription (Per Contributing Developer)\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Snyk\n  ServiceCategory: Application Security\n  ProviderName: Snyk\n  PublisherName: Snyk Limited\n  InvoiceIssuerName: Snyk Limited\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_fee\n    description: >-\n      Recurring monthly or annual platform subscription fee for the active tier (Team,\n      Ignite, or Enterprise).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n      - billing_cycle\n\
  \  - name: contributing_developers\n    description: >-\n      Count of contributing developers in the billing period - developers who have\n      committed to a Snyk-monitored private repo in the last 90 days. Drives\n      per-developer subscription totals.\n    unit: developer\n    aggregation: max\n    dimensions:\n      - organization_id\n      - group_id\n  - name: dast_targets\n    description: >-\n      Number of DAST web-application targets registered (10 included on Ignite, custom\n      on Enterprise).\n    unit: target\n    aggregation: max\n    dimensions:\n      - organization_id\n  - name: tests_per_product\n    description: >-\n      Free-tier-only meter; tracks consumed monthly tests against the per-product cap\n      (e.g. open-source, code, container, IaC). Drives upgrade trigger.\n    unit: test\n    aggregation: sum\n    dimensions:\n      - organization_id\n      - product\n  - name: addon_subscription\n    description: >-\n      Subscription line for Enterprise add-ons\
  \ such as Snyk Learning Management and\n      Snyk API & Web (DAST).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - addon_name\nprinciples:\n  - name: Visibility\n    description: >-\n      Use Snyk Group reporting to track contributing developer counts per organization\n      and project counts per product. The REST Audit Logs and Issues APIs feed\n      attribution into a finops store.\n  - name: Allocation\n    description: >-\n      Map organizations to business units; use group-level governance to enforce the\n      mapping. Tag projects with consuming-team metadata so license and DAST-target\n      consumption can be split.\n  - name: Optimization\n    description: >-\n      Right-size on contributing developers - exclude bot/CI accounts and offboarded\n      developers promptly, cap mono-repo committer sprawl, and consolidate redundant\n      organizations to avoid duplicate fixed costs. Move automation off personal tokens\n      to service accounts to keep tier\
  \ upgrades predictable.\n  - name: Accountability\n    description: >-\n      Assign a security or platform owner per Snyk group. Review contributing-developer\n      counts each cycle and renegotiate add-on inclusion (Learning, API & Web) at\n      renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/finops/snyk-finops.yml
sources:
- https://snyk.io/plans/
- https://docs.snyk.io/snyk-api/
specification: FinOps Framework
tags:
- Security
- DevSecOps
- Vulnerability Management
- Application Security
- FinOps
- FOCUS
---
