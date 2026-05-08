---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nuget-server-api-openapi.yml
  format: yaml
  label: NuGet Server API
  slug: nuget-server-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nuget/refs/heads/main/openapi/nuget-server-api-openapi.yml
- filename: nuget-catalog-api-openapi.yml
  format: yaml
  label: NuGet Catalog API
  slug: nuget-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nuget/refs/heads/main/openapi/nuget-catalog-api-openapi.yml
- filename: nuget-search-api-openapi.yml
  format: yaml
  label: NuGet Search API
  slug: nuget-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nuget/refs/heads/main/openapi/nuget-search-api-openapi.yml
- filename: nuget-package-metadata-api-openapi.yml
  format: yaml
  label: NuGet Package Metadata API
  slug: nuget-package-metadata-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nuget/refs/heads/main/openapi/nuget-package-metadata-api-openapi.yml
- filename: nuget-package-content-api-openapi.yml
  format: yaml
  label: NuGet Package Content API
  slug: nuget-package-content-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nuget/refs/heads/main/openapi/nuget-package-content-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories:
  - Usage
  chargeFrequency: None
  pricingCategory: Free / Public Service
description: 'FOCUS-aligned FinOps for nuget.org: the public registry is free of charge. Commercial spend for private NuGet feeds is on Azure Artifacts (per-user) or GitHub Packages (per-org), not nuget.org itself.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (free service for public feed)
  PricingCategory: Free
  PricingUnit: request
  ProviderName: NuGet
  PublisherName: .NET Foundation / Microsoft Corporation
  ServiceCategory: Developer Tools / Package Registry
  ServiceName: NuGet
layout: finops
meters:
- aggregation: sum
  description: Total .nupkg downloads from nuget.org
  dimensions:
  - package_id
  - version
  name: package_downloads
  unit: download
- aggregation: sum
  description: Bytes egressed by .nupkg downloads
  dimensions:
  - package_id
  name: package_egress_bytes
  unit: GB
- aggregation: sum
  description: Search and metadata requests
  dimensions:
  - api
  name: search_requests
  unit: request
- aggregation: sum
  description: Catalog API pages consumed by mirroring/ingestion clients
  name: catalog_pages_processed
  unit: page
name: Nuget Finops
provider_name: NuGet
provider_slug: nuget
publisher_name: .NET Foundation / Microsoft Corporation
service_category: Developer Tools / Package Registry
slug: nuget-finops
source_filename: nuget-finops.yml
source_heading: FinOps Profile
source_url: https://learn.microsoft.com/en-us/nuget/api/overview
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: NuGet\nproviderId: nuget\npublisherName: .NET Foundation / Microsoft Corporation\nserviceCategory: Developer Tools / Package Registry\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Package Management\n  - .NET\n  - Packages\n  - Registry\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for nuget.org: the public registry is free of charge. Commercial spend\n  for private NuGet feeds is on Azure Artifacts (per-user) or GitHub Packages (per-org), not nuget.org\n  itself.'\nsources:\n  - https://learn.microsoft.com/en-us/nuget/api/overview\n  - https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/\n\
  \  - https://github.com/pricing\nprinciples:\n  - name: Visibility\n    description: nuget.org does not invoice consumers; visibility is about restore cost and time. Track\n      package download bytes, restore duration, and CI cache hit rate. For Azure Artifacts or GitHub Packages,\n      use the respective billing dashboards.\n  - name: Allocation\n    description: Allocate package storage and Actions/Pipelines minutes to the publishing org/team. Tag\n      private feeds by repo or product so each owner sees their share.\n  - name: Optimization\n    description: Cache restored packages in CI (e.g. actions/cache, NuGet.config globalPackagesFolder).\n      Use a proxy feed (Azure Artifacts upstream, JFrog, Sonatype) for high-volume monorepos to reduce\n      egress from nuget.org and avoid throttling.\n  - name: Accountability\n    description: Even though nuget.org is free, runaway CI restores cost time and money downstream. Assign\n      an owner for the package cache, restore performance,\
  \ and any private feed billing.\nbillingModel:\n  pricingCategory: Free / Public Service\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  chargeFrequency: None\nfocusColumns:\n  ServiceName: NuGet\n  ServiceCategory: Developer Tools / Package Registry\n  ProviderName: NuGet\n  PublisherName: .NET Foundation / Microsoft Corporation\n  InvoiceIssuerName: N/A (free service for public feed)\n  PricingCategory: Free\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: package_downloads\n    description: Total .nupkg downloads from nuget.org\n    unit: download\n    aggregation: sum\n    dimensions:\n      - package_id\n      - version\n  - name: package_egress_bytes\n    description: Bytes egressed by .nupkg downloads\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - package_id\n  - name: search_requests\n    description: Search and metadata requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n  - name: catalog_pages_processed\n    description: Catalog API pages consumed by mirroring/ingestion clients\n    unit: page\n    aggregation: sum\napis:\n  - name: NuGet Server API\n    baseURL: https://api.nuget.org/v3/index.json\n    tags:\n      - Package Management\n      - .NET\n      - Registry\n    serviceName: NuGet Server API\n    serviceCategory: Package Registry\n  - name: NuGet Catalog API\n    baseURL: https://api.nuget.org/v3/catalog0/index.json\n    tags:\n      - Catalog\n      - Event Log\n    serviceName: NuGet Catalog API\n    serviceCategory: Package Registry\n  - name: NuGet Search API\n    baseURL: https://azuresearch-usnc.nuget.org/query\n    tags:\n      - Search\n      - Discovery\n    serviceName: NuGet Search API\n    serviceCategory: Package Registry\n  - name: NuGet Package Metadata API\n    baseURL: https://api.nuget.org/v3/registration5-gz-semver2\n    tags:\n      - Metadata\n      - Versions\n    serviceName: NuGet Package Metadata API\n\
  \    serviceCategory: Package Registry\n  - name: NuGet Package Content API\n    baseURL: https://api.nuget.org/v3-flatcontainer\n    tags:\n      - Package Download\n      - NuPkg\n    serviceName: NuGet Package Content API\n    serviceCategory: Package Registry\nunitEconomics:\n  - name: Restore time per CI build\n    metric: ci_restore_seconds / ci_build_count\n    target: minimize via package cache\n  - name: Egress per build\n    metric: package_egress_bytes / ci_build_count\n    target: '< 100MB sustained via cache'\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nuget/refs/heads/main/finops/nuget-finops.yml
sources:
- https://learn.microsoft.com/en-us/nuget/api/overview
- https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/
- https://github.com/pricing
specification: FinOps Framework
tags:
- Package Management
- .NET
- Packages
- Registry
- FinOps
- Cost Management
- FOCUS
---
