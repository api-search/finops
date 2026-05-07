---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: score-openapi.yml
  format: yaml
  label: Score Workload Specification API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/application-research/refs/heads/main/openapi/score-openapi.yml
- filename: cloud-native-application-bundle-openapi.yml
  format: yaml
  label: Cloud Native Application Bundle API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/application-research/refs/heads/main/openapi/cloud-native-application-bundle-openapi.yml
- filename: open-component-model-openapi.yml
  format: yaml
  label: Open Component Model API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/application-research/refs/heads/main/openapi/open-component-model-openapi.yml
- filename: open-resource-discovery-openapi.yml
  format: yaml
  label: Open Resource Discovery API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/application-research/refs/heads/main/openapi/open-resource-discovery-openapi.yml
- filename: radius-openapi.yml
  format: yaml
  label: Radius Application Platform API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/application-research/refs/heads/main/openapi/radius-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Open Source (No Charge)
description: 'FOCUS-aligned FinOps view for Application Research: this is a research index of five free OSS specifications (Score, CNAB, OCM, ORD, Radius). There is no direct billing relationship; FinOps cost surfaces are downstream — the cloud, registry, and platform spend driven by applying these specifications in production.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (no invoice)
  ProviderName: Application Research (multi-vendor OSS)
  PublisherName: CNCF / SAP / Microsoft (per spec)
  ServiceCategory: Application Specifications / Cloud Native
  ServiceName: Application Research Specifications
layout: finops
meters:
- aggregation: sum
  description: Workload deployments produced from Score / CNAB / Radius specs (telemetry for downstream cost attribution)
  dimensions:
  - spec
  - target_platform
  - environment
  name: workload_deployments
  unit: deployment
- aggregation: sum
  description: OCM components/artifacts moved through the supply chain
  dimensions:
  - registry
  - environment
  name: component_artifacts
  unit: artifact
- aggregation: sum
  description: ORD discovery documents published or consumed
  dimensions:
  - publisher
  name: discovery_documents
  unit: document
name: Application Research Finops
provider_name: Application Research
provider_slug: application-research
publisher_name: Various Open Source Foundations
service_category: Application Specifications / Cloud Native
slug: application-research-finops
source_filename: application-research-finops.yml
source_heading: FinOps Profile
source_url: https://score.dev
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Application Research\nproviderId: application-research\npublisherName: Various Open Source Foundations\nserviceCategory: Application Specifications / Cloud Native\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Open Source\n  - Cloud Native\n  - Specifications\ndescription: 'FOCUS-aligned FinOps view for Application Research: this is a research index of five free\n  OSS specifications (Score, CNAB, OCM, ORD, Radius). There is no direct billing relationship; FinOps\n  cost surfaces are downstream — the cloud, registry, and platform spend driven by applying these specifications\n  in production.'\n\
  sources:\n  - https://score.dev\n  - https://cnab.io\n  - https://ocm.software\n  - https://sap.github.io/open-resource-discovery/\n  - https://radapp.io\nbillingModel:\n  pricingCategory: Open Source (No Charge)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Application Research Specifications\n  ServiceCategory: Application Specifications / Cloud Native\n  ProviderName: Application Research (multi-vendor OSS)\n  PublisherName: CNCF / SAP / Microsoft (per spec)\n  InvoiceIssuerName: N/A (no invoice)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: workload_deployments\n    description: Workload deployments produced from Score / CNAB / Radius specs (telemetry for downstream\n      cost attribution)\n    unit: deployment\n    aggregation: sum\n    dimensions:\n      - spec\n      - target_platform\n      - environment\n  - name: component_artifacts\n    description: OCM components/artifacts moved through\
  \ the supply chain\n    unit: artifact\n    aggregation: sum\n    dimensions:\n      - registry\n      - environment\n  - name: discovery_documents\n    description: ORD discovery documents published or consumed\n    unit: document\n    aggregation: sum\n    dimensions:\n      - publisher\nprinciples:\n  - name: Visibility\n    description: Use the underlying platform's billing exports (cloud, container registry, Backstage)\n      to attribute spend driven by applying these specifications; specs themselves emit no billing.\n  - name: Allocation\n    description: Tag specs and bundles with team / cost-center metadata so downstream cloud consumption\n      can be allocated back to the application owner.\n  - name: Optimization\n    description: Use Score / Radius portability to right-size targets per environment (smaller compute\n      for non-prod), share OCM components across applications, prefer ORD-driven service catalogs to reduce\n      duplicate API onboarding cost.\n  - name: Accountability\n\
  \    description: Platform Engineering owns the spec choice and toolchain; application teams accountable\n      for cloud/runtime cost attributed back via labels propagated from the specification.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/application-research/refs/heads/main/finops/application-research-finops.yml
sources:
- https://score.dev
- https://cnab.io
- https://ocm.software
- https://sap.github.io/open-resource-discovery/
- https://radapp.io
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Open Source
- Cloud Native
- Specifications
---
