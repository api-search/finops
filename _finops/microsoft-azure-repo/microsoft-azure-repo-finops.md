---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: git.json
  format: json
  label: Azure DevOps Services REST API - Git
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/MicrosoftDocs/vsts-rest-api-specs/blob/master/specification/git/7.1/git.json
- filename: tfvc.json
  format: json
  label: Azure DevOps Services REST API - TFVC
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/MicrosoftDocs/vsts-rest-api-specs/blob/master/specification/tfvc/7.1/tfvc.json
- filename: policy.json
  format: json
  label: Azure DevOps Services REST API - Policy
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/MicrosoftDocs/vsts-rest-api-specs/blob/master/specification/policy/7.1/policy.json
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription (per Seat)
description: FOCUS-aligned FinOps for Azure Repos — billed per Basic-access user per month ($6) above the free 5-user grant, plus optional GitHub Advanced Security for Azure DevOps per-active-committer add-on. Largest waste pattern is paying for inactive Basic users.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Subscription
  PricingUnit: user-month
  ProviderName: Microsoft Azure DevOps
  PublisherName: Microsoft Corporation
  ServiceCategory: Developer Tools
  ServiceName: Azure Repos
layout: finops
meters:
- aggregation: max
  description: Users with Basic access level (paid above the first 5).
  dimensions:
  - organization
  - team
  - cost_center
  name: basic_users
  unit: user-month
- aggregation: max
  description: Free Stakeholder users (informational; not billed).
  dimensions:
  - organization
  name: stakeholder_users
  unit: user-month
- aggregation: max
  description: Active committers triggering GitHub Advanced Security charges.
  dimensions:
  - repository
  - organization
  name: ghas_committers
  unit: committer-month
- aggregation: max
  description: Repository storage consumed (informational; not directly billed under Basic).
  dimensions:
  - repository
  name: storage_gb
  unit: GB
name: Microsoft Azure Repo Finops
provider_name: Azure Repos
provider_slug: microsoft-azure-repo
publisher_name: Microsoft Corporation
service_category: Developer Tools / Source Control
slug: microsoft-azure-repo-finops
source_filename: microsoft-azure-repo-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/pricing/details/devops/azure-devops-services/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Repos\nproviderId: microsoft-azure-repo\npublisherName: Microsoft Corporation\nserviceCategory: Developer Tools / Source Control\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - DevOps\n  - Git\n  - Repositories\n  - Source Control\n  - Version Control\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Azure Repos — billed per Basic-access user per month\n  ($6) above the free 5-user grant, plus optional GitHub Advanced Security for Azure DevOps\n  per-active-committer add-on. Largest waste pattern is paying for inactive Basic users.\nsources:\n  - https://azure.microsoft.com/pricing/details/devops/azure-devops-services/\n\
  \  - https://learn.microsoft.com/en-us/azure/devops/organizations/billing/buy-basic-access-add-users\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/\nbillingModel:\n  pricingCategory: Subscription (per Seat)\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Repos\n  ServiceCategory: Developer Tools\n  ProviderName: Microsoft Azure DevOps\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Subscription\n  PricingUnit: user-month\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: basic_users\n    description: Users with Basic access level (paid above the first 5).\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - organization\n      - team\n      - cost_center\n  - name: stakeholder_users\n    description:\
  \ Free Stakeholder users (informational; not billed).\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - organization\n  - name: ghas_committers\n    description: Active committers triggering GitHub Advanced Security charges.\n    unit: committer-month\n    aggregation: max\n    dimensions:\n      - repository\n      - organization\n  - name: storage_gb\n    description: Repository storage consumed (informational; not directly billed under Basic).\n    unit: GB\n    aggregation: max\n    dimensions:\n      - repository\nprinciples:\n  - name: Visibility\n    description: Use Organization Settings > Users + Last Access to find inactive Basic users.\n      Pull data via the Member Entitlement Management REST API to drive a periodic audit. Cost\n      Management line items appear as 'Azure DevOps - Basic Users' on the Azure invoice.\n  - name: Allocation\n    description: Tag users by team via Azure DevOps groups; multi-org billing centralizes\n      spend across orgs to\
  \ one Azure subscription. Use group rules to assign access by\n      Entra ID group membership.\n  - name: Optimization\n    description: Audit Last Access date — users not signed in for 30+ days should be downgraded\n      to Stakeholder (free). Avoid double-paying VS subscribers (auto-detected). Use multi-org\n      billing so contractors with multi-org access pay once. Disable GHAS on archived/abandoned\n      repos.\n  - name: Accountability\n    description: Project Collection Administrators set the default access level. Establish a\n      monthly inactive-user review and a budget alert at the Azure subscription level.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://azure.microsoft.com/services/devops/repos/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-repo/refs/heads/main/finops/microsoft-azure-repo-finops.yml
sources:
- https://azure.microsoft.com/pricing/details/devops/azure-devops-services/
- https://learn.microsoft.com/en-us/azure/devops/organizations/billing/buy-basic-access-add-users
- https://learn.microsoft.com/en-us/azure/cost-management-billing/
specification: FinOps Framework
tags:
- DevOps
- Git
- Repositories
- Source Control
- Version Control
- FinOps
- FOCUS
---
