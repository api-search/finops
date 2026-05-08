---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: porter-bundle-openapi.yml
  format: yaml
  label: Porter Bundle API
  slug: porter-bundle-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/porter/refs/heads/main/openapi/porter-bundle-openapi.yml
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A
  chargeCategories: []
  pricingCategory: Open Source (No Charge)
description: FOCUS-aligned FinOps placeholder for Porter. As a CNCF Sandbox open-source project, Porter has no direct billing surface; any FinOps treatment lives in the underlying Kubernetes cluster, container registry, and storage providers the bundles deploy onto. There are no Porter invoices, meters, or seat fees to allocate.
focus_columns:
  BillingCurrency: N/A
  InvoiceIssuerName: N/A
  ProviderName: The Porter Authors
  PublisherName: The Linux Foundation
  ServiceCategory: DevOps Tooling
  ServiceName: Porter
  ServiceSubcategory: Application Packaging (CNAB)
layout: finops
meters: []
name: Porter Finops
provider_name: Porter
provider_slug: porter
publisher_name: The Porter Authors / The Linux Foundation
service_category: DevOps Tooling
slug: porter-finops
source_filename: porter-finops.yml
source_heading: FinOps Profile
source_url: https://porter.sh/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Porter\nproviderId: porter\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud Native\n  - CNAB\n  - Kubernetes\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Porter. As a CNCF Sandbox open-source\n  project, Porter has no direct billing surface; any FinOps treatment lives in\n  the underlying Kubernetes cluster, container registry, and storage providers\n  the bundles deploy onto. There are no Porter invoices, meters, or seat fees\n  to allocate.\nsources:\n  - https://porter.sh/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Porter Authors / The Linux Foundation\nserviceCategory: DevOps Tooling\nbillingModel:\n\
  \  pricingCategory: Open Source (No Charge)\n  billingFrequency: N/A\n  billingCurrency: N/A\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Porter\n  ServiceCategory: DevOps Tooling\n  ServiceSubcategory: Application Packaging (CNAB)\n  ProviderName: The Porter Authors\n  PublisherName: The Linux Foundation\n  InvoiceIssuerName: N/A\n  BillingCurrency: N/A\nmeters: []\nprinciples:\n  - name: Visibility\n    description: Cost is realized in the underlying Kubernetes cluster, OCI registry, and storage that Porter bundles deploy onto; observe those provider invoices, not Porter itself.\n  - name: Allocation\n    description: Allocate by the target Kubernetes namespace and registry repo that bundle installs land in; tag bundles with team labels so downstream cluster cost-allocation tools can attribute spend.\n  - name: Optimization\n    description: Optimization happens at the bundle target (cluster sizing, registry storage classes, image layer reuse). Porter itself contributes no\
  \ recurring cost.\n  - name: Accountability\n    description: Bundle authors are accountable for what their bundles install; cluster and registry owners are accountable for the resulting consumption.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\nnotes: >-\n  Porter is a CNCF Sandbox project with no commercial billing surface.\n  Marked reconciled=false because there is no provider invoice, meter, or\n  pricing structure to align to FOCUS.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/porter/refs/heads/main/finops/porter-finops.yml
sources:
- https://porter.sh/
specification: FinOps Framework
tags:
- Cloud Native
- CNAB
- Kubernetes
- FinOps
- FOCUS
---
