---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: gitlab-api-v4-groups-openapi-original.yml
  format: yaml
  label: GitLab Groups API
  slug: apiv4groups
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-groups-openapi-original.yml
- filename: gitlab-api-v4-projects-openapi-original.yml
  format: yaml
  label: GitLab Projects API
  slug: apiv4projects
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-projects-openapi-original.yml
- filename: gitlab-api-v4-admin-openapi-original.yml
  format: yaml
  label: GitLab Admin API
  slug: apiv4admin
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-admin-openapi-original.yml
- filename: gitlab-api-v4-applications-openapi-original.yml
  format: yaml
  label: GitLab Applications API
  slug: apiv4applications
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-applications-openapi-original.yml
- filename: gitlab-api-v4-avatar-openapi-original.yml
  format: yaml
  label: GitLab Avatar API
  slug: apiv4avatar
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-avatar-openapi-original.yml
- filename: gitlab-api-v4-broadcast-messages-openapi-original.yml
  format: yaml
  label: GitLab Broadcast Messages API
  slug: apiv4broadcast-messages
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-broadcast-messages-openapi-original.yml
- filename: gitlab-api-v4-bulk-imports-openapi-original.yml
  format: yaml
  label: GitLab Bulk Imports API
  slug: apiv4bulk-imports
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-bulk-imports-openapi-original.yml
- filename: gitlab-api-v4-application-openapi-original.yml
  format: yaml
  label: GitLab Application Settings API
  slug: apiv4application
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-application-openapi-original.yml
- filename: gitlab-api-v4-metadata-openapi-original.yml
  format: yaml
  label: GitLab Metadata API
  slug: apiv4metadata
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-metadata-openapi-original.yml
- filename: gitlab-api-v4-version-openapi-original.yml
  format: yaml
  label: GitLab Version API
  slug: apiv4version
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-version-openapi-original.yml
- filename: gitlab-openapi-original.yml
  format: yaml
  label: GitLab REST API
  slug: gitlab-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-openapi-original.yml
- filename: gitlab-oauth2-openapi.yml
  format: yaml
  label: GitLab OAuth 2.0 API
  slug: gitlab-oauth2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-oauth2-openapi.yml
- filename: gitlab-webhooks-openapi.yml
  format: yaml
  label: GitLab Webhooks
  slug: gitlab-webhooks
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-webhooks-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription + Compute Minutes
description: FOCUS-aligned FinOps for GitLab.
focus_columns:
  BillingCurrency: USD
  ProviderName: GitLab
  PublisherName: GitLab
  ServiceCategory: DevOps Platform
  ServiceName: GitLab
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_licenses
  unit: license-month
- aggregation: sum
  dimensions:
  - runner_type
  name: compute_minutes
  unit: minute
- aggregation: max
  name: storage
  unit: GiB-month
- aggregation: sum
  name: gitlab_credits_used
  unit: USD
name: Gitlab Finops
provider_name: GitLab
provider_slug: gitlab
publisher_name: GitLab
service_category: DevOps Platform
slug: gitlab-finops
source_filename: gitlab-finops.yml
source_heading: FinOps Profile
source_url: https://about.gitlab.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: GitLab\nproviderId: gitlab\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - DevOps Platform\ndescription: FOCUS-aligned FinOps for GitLab.\nsources:\n  - https://about.gitlab.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: GitLab\nserviceCategory: DevOps Platform\nbillingModel:\n  pricingCategory: Per-User Subscription + Compute Minutes\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: GitLab\n  ServiceCategory: DevOps Platform\n  ProviderName: GitLab\n  PublisherName: GitLab\n  BillingCurrency: USD\nmeters:\n  - name: user_licenses\n    unit: license-month\n    aggregation: max\n\
  \    dimensions:\n      - plan\n  - name: compute_minutes\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - runner_type\n  - name: storage\n    unit: GiB-month\n    aggregation: max\n  - name: gitlab_credits_used\n    unit: USD\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track GitLab consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/finops/gitlab-finops.yml
sources:
- https://about.gitlab.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- DevOps Platform
---
