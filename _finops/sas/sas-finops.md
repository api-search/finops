---
aligned_with: {}
api_specs:
- filename: sas-viya-rest-api-openapi.yml
  format: yaml
  label: SAS Viya REST API
  slug: viya-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sas/refs/heads/main/openapi/sas-viya-rest-api-openapi.yml
billing_model: {}
description: SAS Viya is offered as an enterprise subscription rather than usage-metered pay-as-you-go. FinOps practitioners typically allocate Viya cost as fixed subscription with cloud-infrastructure overlay when deployed on AWS, Azure, or GCP.
focus_columns: {}
layout: finops
meters: []
name: Sas Finops
provider_name: SAS Institute
provider_slug: sas
publisher_name: ''
service_category: ''
slug: sas-finops
source_filename: sas-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "finopsFrameworkVersion: '2024'\nfocusSpecVersion: '1.0'\nprovider: sas\nname: SAS Viya FinOps Profile\ndescription: >-\n  SAS Viya is offered as an enterprise subscription rather than usage-metered\n  pay-as-you-go. FinOps practitioners typically allocate Viya cost as fixed\n  subscription with cloud-infrastructure overlay when deployed on AWS, Azure,\n  or GCP.\ncostModel:\n  primary: subscription\n  secondary: cloud-infrastructure-pass-through\nbillingDimensions:\n  - dimension: subscription-term\n    description: Annual or multi-year subscription fee\n  - dimension: cloud-infrastructure\n    description: Underlying compute, storage, and networking when self-managed on hyperscaler\n  - dimension: support-tier\n    description: Support and professional services subscriptions\nallocation:\n  - method: tag-based\n    description: Tag Kubernetes namespaces or cloud resources with SAS deployment identifiers\nreferences:\n  - https://www.sas.com/en_us/software/viya.html\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sas/refs/heads/main/finops/sas-finops.yml
sources: []
specification: ''
tags:
- Analytics
- Data Management
- Artificial Intelligence
- Machine Learning
- Software
---
