---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jupyter-notebook-rest-api-openapi.yml
  format: yaml
  label: Jupyter Notebook REST API
  slug: jupyter-notebook-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/openapi/jupyter-notebook-rest-api-openapi.yml
- filename: jupyter-kernel-gateway-api-openapi.yml
  format: yaml
  label: Jupyter Kernel Gateway API
  slug: jupyter-kernel-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/openapi/jupyter-kernel-gateway-api-openapi.yml
- filename: jupyterhub-rest-api-openapi.yml
  format: yaml
  label: JupyterHub REST API
  slug: jupyterhub-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/openapi/jupyterhub-rest-api-openapi.yml
- filename: jupyter-kernel-messaging-asyncapi.yml
  format: yaml
  label: Jupyter Kernel Messaging Protocol
  slug: jupyter-kernel-messaging
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/asyncapi/jupyter-kernel-messaging-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Usage
  pricingCategory: Open Source (no project fees)
description: FOCUS-aligned FinOps scaffold for Project Jupyter. The software itself has no license cost; the FinOps surface is the underlying compute / storage the operator pays for to run kernels, servers, and JupyterHub.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Not Applicable (open source)
  ProviderName: Project Jupyter
  PublisherName: Project Jupyter
  ServiceCategory: Open-Source Data Science / Notebooks
  ServiceName: Jupyter Notebook
layout: finops
meters:
- aggregation: sum
  dimensions:
  - kernel_type
  - user
  - hub
  name: kernel_runtime_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - user
  - hub
  name: notebook_storage
  unit: GB-month
- aggregation: max
  dimensions:
  - hub
  name: hub_active_users
  unit: user
name: Jupyter Notebook Finops
provider_name: Jupyter Notebook
provider_slug: jupyter-notebook
publisher_name: Project Jupyter
service_category: Open-Source Data Science / Notebooks
slug: jupyter-notebook-finops
source_filename: jupyter-notebook-finops.yml
source_heading: FinOps Profile
source_url: https://jupyter.org/about
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Jupyter Notebook\nproviderId: jupyter-notebook\npublisherName: Project Jupyter\nserviceCategory: Open-Source Data Science / Notebooks\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Data Science\n  - Interactive Computing\n  - Jupyter\n  - Notebooks\n  - FinOps\n  - FOCUS\n  - Open Source\ndescription: FOCUS-aligned FinOps scaffold for Project Jupyter. The software itself has no\n  license cost; the FinOps surface is the underlying compute / storage the operator pays\n  for to run kernels, servers, and JupyterHub.\nsources:\n  - https://jupyter.org/about\n  - https://jupyterhub.readthedocs.io/\n  - https://www.finops.org/framework/\n\
  \  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Open Source (no project fees)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Jupyter Notebook\n  ServiceCategory: Open-Source Data Science / Notebooks\n  ProviderName: Project Jupyter\n  PublisherName: Project Jupyter\n  InvoiceIssuerName: Not Applicable (open source)\n  BillingCurrency: USD\nmeters:\n  - name: kernel_runtime_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - kernel_type\n      - user\n      - hub\n  - name: notebook_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - user\n      - hub\n  - name: hub_active_users\n    unit: user\n    aggregation: max\n    dimensions:\n      - hub\nprinciples:\n  - name: Visibility\n    description: Project Jupyter has no first-party billing; visibility comes from the\n      underlying cloud / on-prem cost data and JupyterHub\
  \ usage logs (PrometheusMetrics\n      exporter, named-server / named-user telemetry).\n  - name: Allocation\n    description: Allocate the underlying cost by JupyterHub username, named-server, or\n      Kubernetes namespace; tag cloud resources with hub and tenant labels.\n  - name: Optimization\n    description: Idle-server culling (jupyterhub-idle-culler), right-sized kernel images,\n      shared CPU/GPU pools, and sleep-on-idle drastically reduce notebook compute spend.\n  - name: Accountability\n    description: A platform / data-platform team typically owns the JupyterHub deployment;\n      pair with departmental owners who fund the underlying compute.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jupyter-notebook/refs/heads/main/finops/jupyter-notebook-finops.yml
sources:
- https://jupyter.org/about
- https://jupyterhub.readthedocs.io/
- https://www.finops.org/framework/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Data Science
- Interactive Computing
- Jupyter
- Notebooks
- FinOps
- FOCUS
- Open Source
---
