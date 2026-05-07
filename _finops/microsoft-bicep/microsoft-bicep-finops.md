---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-bicep-deployments-openapi.yml
  format: yaml
  label: Bicep Deployments REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-bicep/refs/heads/main/openapi/microsoft-bicep-deployments-openapi.yml
- filename: microsoft-bicep-template-specs-openapi.yml
  format: yaml
  label: Bicep Template Specs REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-bicep/refs/heads/main/openapi/microsoft-bicep-template-specs-openapi.yml
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A — no direct billing
  chargeCategories:
  - Usage
  chargeFrequency: Recurring (only on deployed resources)
  pricingCategory: Free / Open Source (deployment cost flows through to deployed resources)
description: FOCUS-aligned FinOps for Microsoft Bicep — Bicep itself is free and open-source, so the FinOps focus is on the cost of resources Bicep deploys. Bicep's role in FinOps is to enforce tagging, cost-aware module patterns, and policy-as-code across all Azure deployments. No direct billing line items for Bicep; meters represent governance signals (deployment volume, tag coverage) rather than charges.
focus_columns:
  BillingCurrency: N/A
  ChargeCategory: Usage
  InvoiceIssuerName: N/A
  PricingCategory: Free
  PricingUnit: N/A
  ProviderName: Microsoft Corporation
  PublisherName: Microsoft Corporation
  ServiceCategory: Developer Tools
  ServiceName: Microsoft Bicep
layout: finops
meters:
- aggregation: count
  description: Count of Bicep / ARM deployments invoked (governance signal, not billable).
  dimensions:
  - subscription
  - resource_group
  - principal
  name: deployments_executed
  unit: deployment
- aggregation: count
  description: Resources created/updated by Bicep deployments — drives downstream Azure cost.
  dimensions:
  - resource_type
  - subscription
  - tags_completeness
  name: resources_deployed
  unit: resource
- aggregation: count
  description: Failed deployments (waste signal — points to mis-sized resources or quota blockers).
  dimensions:
  - error_code
  name: deployment_failures
  unit: failure
- aggregation: avg
  description: Percent of Bicep-deployed resources carrying required cost-allocation tags.
  dimensions:
  - subscription
  - required_tag
  name: tag_coverage
  unit: percent
name: Microsoft Bicep Finops
provider_name: Microsoft Bicep
provider_slug: microsoft-bicep
publisher_name: Microsoft Corporation
service_category: Developer Tools / Infrastructure as Code
slug: microsoft-bicep-finops
source_filename: microsoft-bicep-finops.yml
source_heading: FinOps Profile
source_url: https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Bicep\nproviderId: microsoft-bicep\npublisherName: Microsoft Corporation\nserviceCategory: Developer Tools / Infrastructure as Code\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - ARM Templates\n  - Azure\n  - Cloud\n  - Deployment\n  - DevOps\n  - Infrastructure as Code\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Microsoft Bicep — Bicep itself is free and open-source,\n  so the FinOps focus is on the cost of resources Bicep deploys. Bicep's role in FinOps is to\n  enforce tagging, cost-aware module patterns, and policy-as-code across all Azure deployments.\n  No direct billing line items for\
  \ Bicep; meters represent governance signals (deployment\n  volume, tag coverage) rather than charges.\nsources:\n  - https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Free / Open Source (deployment cost flows through to deployed resources)\n  billingFrequency: N/A — no direct billing\n  billingCurrency: N/A\n  chargeCategories:\n    - Usage\n  chargeFrequency: Recurring (only on deployed resources)\nfocusColumns:\n  ServiceName: Microsoft Bicep\n  ServiceCategory: Developer Tools\n  ProviderName: Microsoft Corporation\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: N/A\n  PricingCategory: Free\n  PricingUnit: N/A\n  BillingCurrency: N/A\n  ChargeCategory: Usage\nmeters:\n  - name: deployments_executed\n    description: Count of Bicep / ARM deployments invoked (governance signal, not billable).\n\
  \    unit: deployment\n    aggregation: count\n    dimensions:\n      - subscription\n      - resource_group\n      - principal\n  - name: resources_deployed\n    description: Resources created/updated by Bicep deployments — drives downstream Azure cost.\n    unit: resource\n    aggregation: count\n    dimensions:\n      - resource_type\n      - subscription\n      - tags_completeness\n  - name: deployment_failures\n    description: Failed deployments (waste signal — points to mis-sized resources or quota\n      blockers).\n    unit: failure\n    aggregation: count\n    dimensions:\n      - error_code\n  - name: tag_coverage\n    description: Percent of Bicep-deployed resources carrying required cost-allocation tags.\n    unit: percent\n    aggregation: avg\n    dimensions:\n      - subscription\n      - required_tag\nprinciples:\n  - name: Visibility\n    description: Use Azure Resource Graph to inventory all resources and trace each back to its\n      Bicep deployment. Combine with Cost\
  \ Management to attribute spend to the team that owns\n      the Bicep template (via tags). Pipeline logs (Azure Pipelines / GitHub Actions) reveal\n      who ran which deployment.\n  - name: Allocation\n    description: Codify required tags (CostCenter, Owner, Environment, App) directly in the\n      Bicep template. Use Bicep parameters with @allowed() to enforce environment values.\n      Bicep modules should always pass tag dictionaries to deployed resources.\n  - name: Optimization\n    description: Build cost-aware Bicep modules — default to lower-cost SKUs (Standard SSD,\n      B-series, basic LB) and require explicit override for premium. Use param objects with\n      cost-tier presets (dev / staging / prod). Enforce Azure Policy via Bicep deployments to\n      block disallowed expensive SKUs. Use what-if to preview deltas before committing\n      production changes.\n  - name: Accountability\n    description: Bicep templates live in version control with CODEOWNERS-style approval\
  \ gates.\n      Pipelines validate cost-policy compliance before deployment. FinOps team reviews new\n      Bicep modules quarterly to ensure cost guardrails remain current.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://github.com/Azure/bicep\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-bicep/refs/heads/main/finops/microsoft-bicep-finops.yml
sources:
- https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview
- https://learn.microsoft.com/en-us/azure/cost-management-billing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- ARM Templates
- Azure
- Cloud
- Deployment
- DevOps
- Infrastructure as Code
- FinOps
- FOCUS
---
