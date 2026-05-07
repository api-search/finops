---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: artifactory-rest-api-openapi.yml
  format: yaml
  label: Artifactory REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/artifactory/refs/heads/main/openapi/artifactory-rest-api-openapi.yml
- filename: artifactory-aql-api-openapi.yml
  format: yaml
  label: Artifactory Query Language (AQL) API
  slug: aql-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/artifactory/refs/heads/main/openapi/artifactory-aql-api-openapi.yml
- filename: artifactory-docker-registry-api-openapi.yml
  format: yaml
  label: Artifactory Docker Registry API
  slug: docker-registry-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/artifactory/refs/heads/main/openapi/artifactory-docker-registry-api-openapi.yml
- filename: artifactory-build-integration-api-openapi.yml
  format: yaml
  label: Artifactory Build Integration API
  slug: build-integration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/artifactory/refs/heads/main/openapi/artifactory-build-integration-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (SaaS) / Annual (Self-Managed)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Usage Overage
description: FOCUS-aligned FinOps for JFrog Artifactory — tiered SaaS subscription with included storage consumption plus a per-GB overage meter on a tiered overage schedule, alongside annual self-managed per-server subscriptions.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: JFrog Ltd.
  PricingCategory: Tiered Subscription + Usage Overage
  PricingUnit: GB-month
  ProviderName: JFrog
  PublisherName: JFrog Ltd.
  ServiceCategory: Developer Tools
  ServiceName: JFrog Artifactory
  ServiceSubcategory: Artifact Repository
layout: finops
meters:
- aggregation: sum
  description: Monthly or annual subscription fee for the selected Artifactory plan
  dimensions:
  - plan
  - deployment_model
  name: subscription_fee
  unit: month
- aggregation: max
  description: GB of artifact storage consumed (counts toward included base before overage)
  dimensions:
  - plan
  - region
  name: storage_consumption
  unit: GB-month
- aggregation: sum
  description: GB of storage above the plan's included base, billed on the tiered overage schedule
  dimensions:
  - plan
  - region
  - tier_band
  name: storage_overage
  unit: GB
- aggregation: sum
  description: Network data transfer associated with artifact downloads where charged
  dimensions:
  - direction
  - region
  name: data_transfer
  unit: GB
- aggregation: max
  description: Number of self-managed servers under license
  dimensions:
  - plan
  name: server_count
  unit: server
name: Artifactory Finops
provider_name: JFrog Artifactory
provider_slug: artifactory
publisher_name: JFrog Ltd.
service_category: Developer Tools / Artifact Management
slug: artifactory-finops
source_filename: artifactory-finops.yml
source_heading: FinOps Profile
source_url: https://jfrog.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: JFrog Artifactory\nproviderId: artifactory\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Artifacts\n  - DevOps\n  - CI/CD\n  - Docker Registry\n  - Package Management\n  - Repository\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for JFrog Artifactory — tiered SaaS subscription with included storage\n  consumption plus a per-GB overage meter on a tiered overage schedule, alongside annual self-managed\n  per-server subscriptions.\nsources:\n  - https://jfrog.com/pricing/\n  - https://jfrog.com/help/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: JFrog Ltd.\nserviceCategory: Developer\
  \ Tools / Artifact Management\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage Overage\n  billingFrequency: Monthly (SaaS) / Annual (Self-Managed)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: JFrog Artifactory\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: Artifact Repository\n  ProviderName: JFrog\n  PublisherName: JFrog Ltd.\n  InvoiceIssuerName: JFrog Ltd.\n  BillingCurrency: USD\n  PricingCategory: Tiered Subscription + Usage Overage\n  PricingUnit: GB-month\n  ChargeCategory: Usage\nmeters:\n  - name: subscription_fee\n    description: Monthly or annual subscription fee for the selected Artifactory plan\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - deployment_model\n  - name: storage_consumption\n    description: GB of artifact storage consumed (counts toward included base before overage)\n    unit: GB-month\n    aggregation:\
  \ max\n    dimensions:\n      - plan\n      - region\n  - name: storage_overage\n    description: GB of storage above the plan's included base, billed on the tiered overage schedule\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - plan\n      - region\n      - tier_band\n  - name: data_transfer\n    description: Network data transfer associated with artifact downloads where charged\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - direction\n      - region\n  - name: server_count\n    description: Number of self-managed servers under license\n    unit: server\n    aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Use the JFrog Platform Admin console (Reports → Storage Summary, Usage by Repository)\n      and the System REST API (api/storageinfo, api/repositories/{key}/usage) to surface monthly storage\n      consumption and projected overage before invoice close.\n  - name: Allocation\n    description: Tag spend\
  \ by repository and project using Artifactory's repository-level metadata\n      and properties; map repositories to cost centers in the consuming team's CMDB or via JFrog\n      labels.\n  - name: Optimization\n    description: Reduce storage overage through repository cleanup policies (max-unique-snapshots,\n      retention rules), generic-repo deduplication, and binary cleanup with JFrog's automated cleanup\n      features (Enterprise X+). Use Tiered Storage to push cold artifacts to cheaper backends.\n  - name: Accountability\n    description: Assign repository ownership and surface monthly storage charts to repo owners; use\n      JFrog Insight or exported CSV reports to feed showback. Trigger alerts when projected storage\n      crosses 80% of the included plan base.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/artifactory/refs/heads/main/finops/artifactory-finops.yml
sources:
- https://jfrog.com/pricing/
- https://jfrog.com/help/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Artifacts
- DevOps
- CI/CD
- Docker Registry
- Package Management
- Repository
- FinOps
- FOCUS
---
