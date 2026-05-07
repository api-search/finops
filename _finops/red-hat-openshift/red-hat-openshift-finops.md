---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: red-hat-openshift-api-openapi.yml
  format: yaml
  label: Red Hat OpenShift Container Platform API
  slug: openshift-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-openshift/refs/heads/main/openapi/red-hat-openshift-api-openapi.yml
- filename: openapi
  format: yaml
  label: Red Hat OpenShift Cluster Manager API
  slug: openshift-cluster-manager-api
  spec_type: OpenAPI
  url: https://api.openshift.com/openapi
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps shape for Red Hat OpenShift. Two billing surfaces coexist — managed cloud services billed hourly through the cloud provider's invoice (AWS, Azure, IBM, GCP) with reserved-instance / committed-use discount, and self-managed annual subscriptions billed by Red Hat. Reserved-instance ROSA at 4vCPU/3yr starts at $0.076/hour.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Red Hat, Inc. (self-managed); cloud provider (managed services)
  ProviderName: Red Hat
  PublisherName: Red Hat, Inc.
  ServiceCategory: Container Platform
  ServiceName: Red Hat OpenShift
layout: finops
meters:
- aggregation: sum
  description: Hourly billed Red Hat OpenShift Service on AWS instance hours; on-demand or reserved (1yr / 3yr).
  dimensions:
  - aws_region
  - instance_type
  - commitment_term
  name: rosa_instance_hours
  unit: instance-hour
- aggregation: sum
  description: Hourly billed Microsoft Azure Red Hat OpenShift instance hours.
  dimensions:
  - azure_region
  - instance_type
  name: aro_instance_hours
  unit: instance-hour
- aggregation: sum
  description: Annual Red Hat OpenShift Dedicated subscription on AWS or Google Cloud.
  dimensions:
  - underlying_cloud
  - support_level
  name: dedicated_subscription
  unit: contract
- aggregation: sum
  description: Hourly billed Red Hat OpenShift on IBM Cloud instance hours.
  dimensions:
  - ibm_region
  - instance_type
  name: ibm_instance_hours
  unit: instance-hour
- aggregation: sum
  description: Annual self-managed OpenShift subscription (Platform Plus, Container Platform, Kubernetes Engine, Virtualization Engine).
  dimensions:
  - edition
  - core_count
  - support_level
  name: self_managed_subscription
  unit: contract
name: Red Hat Openshift Finops
provider_name: Red Hat OpenShift
provider_slug: red-hat-openshift
publisher_name: Red Hat, Inc.
service_category: Container Platform
slug: red-hat-openshift-finops
source_filename: red-hat-openshift-finops.yml
source_heading: FinOps Profile
source_url: https://www.redhat.com/en/technologies/cloud-computing/openshift/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat OpenShift\nproviderId: red-hat-openshift\npublisherName: Red Hat, Inc.\nserviceCategory: Container Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Kubernetes\n  - Containers\n  - Cloud\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Red Hat OpenShift. Two billing surfaces coexist —\n  managed cloud services billed hourly through the cloud provider's invoice (AWS, Azure, IBM,\n  GCP) with reserved-instance / committed-use discount, and self-managed annual subscriptions\n  billed by Red Hat. Reserved-instance ROSA at 4vCPU/3yr starts at $0.076/hour.\nsources:\n  - https://www.redhat.com/en/technologies/cloud-computing/openshift/pricing\n\
  billingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Red Hat OpenShift\n  ServiceCategory: Container Platform\n  ProviderName: Red Hat\n  PublisherName: Red Hat, Inc.\n  InvoiceIssuerName: 'Red Hat, Inc. (self-managed); cloud provider (managed services)'\n  BillingCurrency: USD\nmeters:\n  - name: rosa_instance_hours\n    description: Hourly billed Red Hat OpenShift Service on AWS instance hours; on-demand or\n      reserved (1yr / 3yr).\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - aws_region\n      - instance_type\n      - commitment_term\n  - name: aro_instance_hours\n    description: Hourly billed Microsoft Azure Red Hat OpenShift instance hours.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - azure_region\n      - instance_type\n  - name: dedicated_subscription\n    description: Annual Red\
  \ Hat OpenShift Dedicated subscription on AWS or Google Cloud.\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - underlying_cloud\n      - support_level\n  - name: ibm_instance_hours\n    description: Hourly billed Red Hat OpenShift on IBM Cloud instance hours.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - ibm_region\n      - instance_type\n  - name: self_managed_subscription\n    description: Annual self-managed OpenShift subscription (Platform Plus, Container Platform,\n      Kubernetes Engine, Virtualization Engine).\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - edition\n      - core_count\n      - support_level\nprinciples:\n  - name: Visibility\n    description: For managed services, ingest the cloud provider's CUR/billing export (AWS CUR,\n      Azure Cost Mgmt, IBM Cloud billing) filtered to the OpenShift line items. For self-managed,\n      use Red Hat Subscription Watch and OpenShift Cost Management Operator to\
  \ attribute cluster\n      spend to namespaces.\n  - name: Allocation\n    description: Tag clusters and namespaces; use the OpenShift Cost Management Operator to\n      attribute compute, memory, and storage to teams and projects.\n  - name: Optimization\n    description: Move steady-state ROSA workloads to reserved instances ($0.076/hr at 4vCPU\n      3yr starting rate); consolidate self-managed editions onto Platform Plus where ACM/ACS\n      are needed; right-size cluster autoscaler aggressively in non-prod.\n  - name: Accountability\n    description: Platform team owns cluster-level spend; product teams own namespace-level\n      consumption attributed via Cost Management Operator.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat-openshift/refs/heads/main/finops/red-hat-openshift-finops.yml
sources:
- https://www.redhat.com/en/technologies/cloud-computing/openshift/pricing
specification: FinOps Framework
tags:
- Kubernetes
- Containers
- Cloud
- FinOps
- FOCUS
---
