---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tekton-pipeline-openapi.json
  format: json
  label: Tekton Task CRD
  slug: tekton-task-crd
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tekton/refs/heads/main/openapi/tekton-pipeline-openapi.json
billing_model:
  billingCurrency: Not Applicable
  billingFrequency: Not Applicable
  chargeCategories: []
  pricingCategory: Open Source — No Commercial Billing Surface
description: Tekton is open-source software (Apache License 2.0). There is no commercial billing surface published by the Tekton project itself — there are no invoices, no metered usage charges, and no subscription fees attributable to Tekton. Operating costs flow entirely through the operator's own Kubernetes infrastructure providers (worker-node compute consumed by TaskRun/PipelineRun pods, persistent volumes for workspaces, image-registry storage, ingress, observability, and any cloud-side OCI registries used by Chains). Commercial managed offerings exist (Red Hat OpenShift Pipelines, IBM Cloud Continuous Delivery, Tekton via various cloud platforms) and have their own billing surfaces that should be profiled against the third-party vendor — not Tekton.
focus_columns:
  BillingCurrency: Not Applicable
  ChargeCategory: Not Applicable
  InvoiceIssuerName: Not Applicable
  ProviderName: Tekton (CNCF)
  PublisherName: Tekton (CNCF)
  ServiceCategory: DevOps
  ServiceName: Tekton
layout: finops
meters: []
name: Tekton Finops
provider_name: Tekton
provider_slug: tekton
publisher_name: Tekton (CNCF)
service_category: DevOps / CI/CD
slug: tekton-finops
source_filename: tekton-finops.yml
source_heading: FinOps Profile
source_url: https://tekton.dev/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tekton\nproviderId: tekton\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n  - DevOps\n  - CI/CD\n  - Kubernetes\n  - CNCF\n  - Open Source\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: >-\n  Tekton is open-source software (Apache License 2.0). There is no commercial billing surface published by the Tekton project itself — there are no invoices, no metered usage charges, and no subscription fees attributable to Tekton. Operating costs flow entirely through the operator's own Kubernetes infrastructure providers (worker-node compute consumed by TaskRun/PipelineRun pods, persistent volumes for workspaces, image-registry storage, ingress, observability, and any cloud-side OCI registries used by Chains). Commercial managed offerings exist (Red Hat OpenShift Pipelines, IBM Cloud Continuous Delivery, Tekton via various cloud platforms)\
  \ and have their own billing surfaces that should be profiled against the third-party vendor — not Tekton.\nnotes: >-\n  Open source — no commercial billing surface; commercial offerings handled by 3rd parties (Red Hat OpenShift Pipelines, IBM Cloud Continuous Delivery, Tekton via cloud platforms). reconciled=false explicitly indicates that no Tekton-issued bill exists rather than incomplete data. The principles below describe how to FinOps-manage the underlying infrastructure cost of operating self-hosted Tekton.\nsources:\n  - https://tekton.dev/\n  - https://github.com/tektoncd/pipeline/blob/main/LICENSE\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tekton (CNCF)\nserviceCategory: DevOps / CI/CD\nbillingModel:\n  pricingCategory: Open Source\
  \ — No Commercial Billing Surface\n  billingFrequency: Not Applicable\n  billingCurrency: Not Applicable\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Tekton\n  ServiceCategory: DevOps\n  ProviderName: Tekton (CNCF)\n  PublisherName: Tekton (CNCF)\n  InvoiceIssuerName: Not Applicable\n  BillingCurrency: Not Applicable\n  ChargeCategory: Not Applicable\nmeters: []\nprinciples:\n  - name: Visibility\n    description: >-\n      No Tekton invoice exists. Treat self-hosted Tekton as a Kubernetes workload — the cost is the underlying compute consumed by TaskRun/PipelineRun pods (often bursty), persistent storage for workspaces, image pulls, OCI artifact pushes, ingress for EventListeners, and the database backing Tekton Results. All of these appear on the cloud provider's FOCUS-formatted bill.\n  - name: Allocation\n    description: >-\n      Tag PipelineRun and TaskRun pods by team / repository / commit-author via Tekton's labels and annotations and propagate them to your cloud-provider\
  \ tagging strategy. Tekton Results storage costs can be allocated by namespace.\n  - name: Optimization\n    description: >-\n      Use spot/preemptible nodes for short-lived TaskRun pods; right-size step container resource requests; cache image layers via local registry mirrors; use the Hub/Bundles resolver to avoid re-bundling Tasks; expire old Results data; consolidate small Tekton installations onto a shared cluster with namespace-level RBAC and ResourceQuotas.\n  - name: Accountability\n    description: >-\n      Assign a platform-engineering owner; review monthly Kubernetes-cluster cost attributable to tekton-pipelines and PipelineRun namespaces; benchmark managed Tekton (e.g., OpenShift Pipelines) versus self-hosting before signing a vendor contract.\ncommercialOfferings:\n  - name: Red Hat OpenShift Pipelines\n    type: distribution\n    url: https://www.redhat.com/en/technologies/cloud-computing/openshift/pipelines\n    note: Bundled and supported as part of OpenShift subscription.\n\
  \  - name: IBM Cloud Continuous Delivery\n    type: managed-service\n    url: https://www.ibm.com/cloud/continuous-delivery\n    note: Cloud-hosted CI/CD using Tekton; pricing per IBM Cloud catalog.\n  - name: Pipelines-as-Code on Cloud Platforms\n    type: managed-service\n    url: https://pipelinesascode.com/\n    note: Several cloud platforms expose hosted Tekton Pipelines-as-Code; pricing per platform.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tekton/refs/heads/main/finops/tekton-finops.yml
sources:
- https://tekton.dev/
- https://github.com/tektoncd/pipeline/blob/main/LICENSE
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DevOps
- CI/CD
- Kubernetes
- CNCF
- Open Source
- FinOps
- Cost Management
- FOCUS
---
