---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jfrog-artifactory-openapi.yml
  format: yaml
  label: JFrog Artifactory REST API
  slug: jfrog-artifactory-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-artifactory-openapi.yml
- filename: jfrog-artifactory-openapi.yml
  format: yaml
  label: JFrog Artifactory REST API V2
  slug: jfrog-artifactory-rest-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-artifactory-openapi.yml
- filename: jfrog-xray-openapi.yml
  format: yaml
  label: JFrog Xray REST API
  slug: jfrog-xray-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-xray-openapi.yml
- filename: jfrog-distribution-openapi.yml
  format: yaml
  label: JFrog Distribution REST API
  slug: jfrog-distribution-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-distribution-openapi.yml
- filename: jfrog-pipelines-openapi.yml
  format: yaml
  label: JFrog Pipelines REST API
  slug: jfrog-pipelines-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-pipelines-openapi.yml
- filename: jfrog-platform-openapi.yml
  format: yaml
  label: JFrog Platform REST API
  slug: jfrog-platform-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-platform-openapi.yml
- filename: jfrog-access-openapi.yml
  format: yaml
  label: JFrog Access REST API
  slug: jfrog-access-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-access-openapi.yml
- filename: jfrog-curation-openapi.yml
  format: yaml
  label: JFrog Curation REST API
  slug: jfrog-curation-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-curation-openapi.yml
- filename: jfrog-mission-control-openapi.yml
  format: yaml
  label: JFrog Mission Control REST API
  slug: jfrog-mission-control-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-mission-control-openapi.yml
- filename: jfrog-release-lifecycle-openapi.yml
  format: yaml
  label: JFrog Release Lifecycle Management REST API
  slug: jfrog-release-lifecycle-management-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-release-lifecycle-openapi.yml
- filename: jfrog-workers-openapi.yml
  format: yaml
  label: JFrog Workers REST API
  slug: jfrog-workers-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-workers-openapi.yml
- filename: jfrog-ml-openapi.yml
  format: yaml
  label: JFrog ML REST API
  slug: jfrog-ml-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-ml-openapi.yml
- filename: jfrog-connect-openapi.yml
  format: yaml
  label: JFrog Connect REST API
  slug: jfrog-connect-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-connect-openapi.yml
- filename: jfrog-catalog-openapi.yml
  format: yaml
  label: JFrog Catalog REST API
  slug: jfrog-catalog-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-catalog-openapi.yml
- filename: jfrog-evidence-openapi.yml
  format: yaml
  label: JFrog Evidence REST API
  slug: jfrog-evidence-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/openapi/jfrog-evidence-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Tiered Overage
description: 'FOCUS-aligned FinOps for JFrog: tiered Cloud subscriptions priced by monthly base + tiered storage / data-transfer overage, plus self-managed annual subscriptions and optional Security and MLOps bundles. The dominant cost driver in Cloud is consumption (GB stored, GB transferred) above the included tier allotment.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: JFrog Ltd.
  ProviderName: JFrog
  PublisherName: JFrog Ltd.
  ServiceCategory: DevOps / Software Supply Chain
  ServiceName: JFrog Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  - deployment
  name: subscription_base
  unit: month
- aggregation: sum
  dimensions:
  - repository
  - package_type
  - region
  name: storage_consumption
  unit: GB-month
- aggregation: sum
  dimensions:
  - direction
  - region
  name: data_transfer
  unit: GB
- aggregation: max
  dimensions:
  - tier
  name: server_subscription
  unit: server-year
- aggregation: sum
  dimensions:
  - bundle
  name: security_bundle
  unit: month
- aggregation: sum
  dimensions:
  - bundle
  name: mlops_bundle
  unit: month
name: Jfrog Finops
provider_name: JFrog
provider_slug: jfrog
publisher_name: JFrog Ltd.
service_category: DevOps / Software Supply Chain
slug: jfrog-finops
source_filename: jfrog-finops.yml
source_heading: FinOps Profile
source_url: https://jfrog.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: JFrog\nproviderId: jfrog\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - DevOps\n  - Software Supply Chain\n  - Container Registry\ndescription: 'FOCUS-aligned FinOps for JFrog: tiered Cloud subscriptions priced by monthly base + tiered\n  storage / data-transfer overage, plus self-managed annual subscriptions and optional Security and\n  MLOps bundles. The dominant cost driver in Cloud is consumption (GB stored, GB transferred) above\n  the included tier allotment.'\nsources:\n  - https://jfrog.com/pricing/\n  - https://jfrog.com/help/r/jfrog-platform-administration-documentation/jfrog-subscriptions\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: JFrog Ltd.\nserviceCategory: DevOps / Software Supply Chain\nbillingModel:\n  pricingCategory: Subscription + Tiered Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: JFrog Platform\n  ServiceCategory: DevOps / Software Supply Chain\n  ProviderName: JFrog\n  PublisherName: JFrog Ltd.\n  InvoiceIssuerName: JFrog Ltd.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_base\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - deployment\n  - name: storage_consumption\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - repository\n      - package_type\n      - region\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - direction\n      - region\n  - name: server_subscription\n    unit: server-year\n    aggregation: max\n    dimensions:\n      - tier\n  - name: security_bundle\n\
  \    unit: month\n    aggregation: sum\n    dimensions:\n      - bundle\n  - name: mlops_bundle\n    unit: month\n    aggregation: sum\n    dimensions:\n      - bundle\nprinciples:\n  - name: Visibility\n    description: Use the JFrog Platform Usage / Subscription dashboard and the Artifactory storage\n      summary REST endpoint to see GB consumption per repository and per package type; export to your\n      data warehouse for FOCUS reporting.\n  - name: Allocation\n    description: Tag repositories with team / product / environment metadata so storage and data-transfer\n      cost can be charged back; use Projects in JFrog Platform to bound consumption per tenant.\n  - name: Optimization\n    description: Apply automated cleanup policies (Enterprise X+) to expire snapshots and old images,\n      enable replication / federation only where business-critical, deduplicate base images, and choose\n      regions to minimize cross-region transfer; lock in 3-year commits for stable workloads.\n\
  \  - name: Accountability\n    description: DevOps platform team owns the JFrog tenancy and reconciles monthly base + overage\n      against forecast; per-team cost reviews quarterly via Projects-based showback.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jfrog/refs/heads/main/finops/jfrog-finops.yml
sources:
- https://jfrog.com/pricing/
- https://jfrog.com/help/r/jfrog-platform-administration-documentation/jfrog-subscriptions
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- DevOps
- Software Supply Chain
- Container Registry
---
