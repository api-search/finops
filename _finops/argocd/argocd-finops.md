---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: argocd-server-openapi.json
  format: json
  label: Argo CD Applications API
  slug: argocd-applications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/argocd/refs/heads/main/openapi/argocd-server-openapi.json
billing_model:
  billingCurrency: Not Applicable
  billingFrequency: Not Applicable
  chargeCategories: []
  pricingCategory: Open Source — No Commercial Billing Surface
description: Argo CD is open-source software (Apache License 2.0). There is no commercial billing surface published by the Argo CD project itself — there are no invoices, no metered usage charges, and no subscription fees attributable to Argo CD. Operating costs flow entirely through the operator's own infrastructure providers (Kubernetes cluster compute, storage, networking, monitoring, and ingress). Commercial managed offerings exist (e.g., Akuity Platform, Codefresh/Octopus Deploy, Kubernetes distribution vendors) and have their own billing surfaces that should be profiled against the third-party vendor — not Argo CD.
focus_columns:
  BillingCurrency: Not Applicable
  ChargeCategory: Not Applicable
  InvoiceIssuerName: Not Applicable
  ProviderName: Argo CD (CNCF)
  PublisherName: Argo CD (CNCF)
  ServiceCategory: DevOps
  ServiceName: Argo CD
layout: finops
meters: []
name: Argocd Finops
provider_name: Argo CD
provider_slug: argocd
publisher_name: Argo CD (CNCF)
service_category: DevOps / GitOps
slug: argocd-finops
source_filename: argocd-finops.yml
source_heading: FinOps Profile
source_url: https://argo-cd.readthedocs.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Argo CD\nproviderId: argocd\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n  - DevOps\n  - GitOps\n  - Kubernetes\n  - CNCF\n  - Open Source\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: >-\n  Argo CD is open-source software (Apache License 2.0). There is no commercial billing surface published by the Argo CD project itself — there are no invoices, no metered usage charges, and no subscription fees attributable to Argo CD. Operating costs flow entirely through the operator's own infrastructure providers (Kubernetes cluster compute, storage, networking, monitoring, and ingress). Commercial managed offerings exist (e.g., Akuity Platform, Codefresh/Octopus Deploy, Kubernetes distribution vendors) and have their own billing surfaces that should be profiled against the third-party vendor — not Argo CD.\nnotes: >-\n  Open source\
  \ — no commercial billing surface; commercial offerings handled by 3rd parties (Akuity for Argo CD). reconciled=false explicitly indicates that no Argo CD-issued bill exists rather than incomplete data. The principles below describe how to FinOps-manage the underlying infrastructure cost of operating self-hosted Argo CD.\nsources:\n  - https://argo-cd.readthedocs.io/\n  - https://github.com/argoproj/argo-cd/blob/master/LICENSE\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Argo CD (CNCF)\nserviceCategory: DevOps / GitOps\nbillingModel:\n  pricingCategory: Open Source — No Commercial Billing Surface\n  billingFrequency: Not Applicable\n  billingCurrency: Not Applicable\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Argo CD\n  ServiceCategory:\
  \ DevOps\n  ProviderName: Argo CD (CNCF)\n  PublisherName: Argo CD (CNCF)\n  InvoiceIssuerName: Not Applicable\n  BillingCurrency: Not Applicable\n  ChargeCategory: Not Applicable\nmeters: []\nprinciples:\n  - name: Visibility\n    description: >-\n      No Argo CD invoice exists. Treat self-hosted Argo CD as a Kubernetes workload — its cost is the underlying compute (argocd-server, application-controller, repo-server, redis, ApplicationSet controller, notifications controller pods), persistent storage, ingress/load-balancer hours, and observability resources, all of which appear on the cloud provider's FOCUS-formatted bill.\n  - name: Allocation\n    description: >-\n      Tag Argo CD namespace resources by environment / cost-center via Kubernetes labels and propagate them to your cloud-provider tagging strategy. If running multiple Argo CD instances per tenant, allocate by namespace.\n  - name: Optimization\n    description: >-\n      Right-size argocd-server, repo-server, and application-controller\
  \ replicas; shard the application-controller for very large fleets; tune cache expiration; consider running Argo CD on Spot/Preemptible nodes; consolidate small instances into a single multi-tenant control-plane deployment.\n  - name: Accountability\n    description: >-\n      Assign a platform-engineering owner; review monthly Kubernetes-cluster cost attributable to argocd namespaces; if commercial managed Argo CD is being considered (e.g., Akuity), benchmark its monthly fee against the operational + opportunity cost of self-hosting.\ncommercialOfferings:\n  - name: Akuity Platform\n    type: managed-argocd\n    url: https://akuity.io/\n    note: SaaS offering of managed Argo CD founded by the project's creators; pricing on request.\n  - name: Codefresh (Octopus Deploy)\n    type: managed-argocd\n    url: https://codefresh.io/\n    note: GitOps platform built on Argo CD and Argo Workflows.\n  - name: Kubernetes Distribution Bundles\n    type: bundled-support\n    url: https://www.cncf.io/projects/argo/\n\
  \    note: Argo CD is bundled and supported by major Kubernetes distributions; pricing varies by vendor.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/argocd/refs/heads/main/finops/argocd-finops.yml
sources:
- https://argo-cd.readthedocs.io/
- https://github.com/argoproj/argo-cd/blob/master/LICENSE
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DevOps
- GitOps
- Kubernetes
- CNCF
- Open Source
- FinOps
- Cost Management
- FOCUS
---
