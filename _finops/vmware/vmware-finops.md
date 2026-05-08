---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vmware-vsphere-api-openapi.yml
  format: yaml
  label: vSphere API
  slug: vsphere-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vmware/refs/heads/main/openapi/vmware-vsphere-api-openapi.yml
- filename: openapi.yaml
  format: yaml
  label: vCloud Director API
  slug: vcloud-director-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/vmware-cloud-director/latest/openapi/
- filename: openapi.yaml
  format: yaml
  label: NSX-T Data Center API
  slug: nsx-t-data-center-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/nsx-t/latest/openapi/
- filename: openapi.yaml
  format: yaml
  label: vRealize Automation API
  slug: vrealize-automation-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/vrealize-automation/latest/openapi/
- filename: openapi.yaml
  format: yaml
  label: VMware Cloud on AWS API
  slug: vmware-cloud-on-aws-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/vmc/latest/openapi/
- filename: openapi.yaml
  format: yaml
  label: vRealize Operations API
  slug: vrealize-operations-api
  spec_type: OpenAPI
  url: https://developer.vmware.com/apis/vrealize-operations/latest/openapi/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: FinOps view of the VMware (Broadcom) portfolio. Licensing is sold as subscription bundles (VMware Cloud Foundation, vSphere Foundation) priced per core / VM, negotiated through Broadcom direct sales or authorized partners. No public pricing surface; FOCUS mapping is limited to invoice-side fields until customer-specific contract terms are observed.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Broadcom Inc.
  ProviderName: VMware
  PublisherName: Broadcom Inc.
  ServiceCategory: Cloud Infrastructure / Virtualization
  ServiceName: VMware
layout: finops
meters:
- aggregation: sum
  description: Subscription license entitlement covering the negotiated VMware portfolio bundle for a contract term.
  dimensions:
  - product
  - edition
  - core_count
  - term
  name: subscription_term
  unit: varies
name: Vmware Finops
provider_name: VMware
provider_slug: vmware
publisher_name: Broadcom Inc.
service_category: Cloud Infrastructure / Virtualization
slug: vmware-finops
source_filename: vmware-finops.yml
source_heading: FinOps Profile
source_url: https://www.broadcom.com/products/vmware-cloud-foundation
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: VMware\nproviderId: vmware\npublisherName: Broadcom Inc.\nserviceCategory: Cloud Infrastructure / Virtualization\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud Computing\n  - Virtualization\n  - Hybrid Cloud\n  - FinOps\n  - FOCUS\ndescription: FinOps view of the VMware (Broadcom) portfolio. Licensing is sold as\n  subscription bundles (VMware Cloud Foundation, vSphere Foundation) priced per\n  core / VM, negotiated through Broadcom direct sales or authorized partners.\n  No public pricing surface; FOCUS mapping is limited to invoice-side fields\n  until customer-specific contract terms are observed.\nsources:\n  - https://www.broadcom.com/products/vmware-cloud-foundation\n\
  \  - https://www.vmware.com/products/cloud-infrastructure/vsphere-foundation\nnotes: VMware/Broadcom does not expose a vendor-wide usage or billing API; FinOps\n  observability depends on contract entitlements, customer-side telemetry (vCenter,\n  Aria Operations, Tanzu CloudHealth), and Broadcom-issued invoices.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: VMware\n  ServiceCategory: Cloud Infrastructure / Virtualization\n  ProviderName: VMware\n  PublisherName: Broadcom Inc.\n  InvoiceIssuerName: Broadcom Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_term\n    description: Subscription license entitlement covering the negotiated VMware\n      portfolio bundle for a contract term.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\n      - edition\n      - core_count\n \
  \     - term\nprinciples:\n  - name: Visibility\n    description: VMware does not expose a vendor-side usage API. Use Aria Operations\n      / VMware CloudHealth and SDDC Manager telemetry to observe consumption against\n      the licensed entitlement; reconcile against the Broadcom invoice line items.\n  - name: Allocation\n    description: Allocate VMware spend by cluster, datacenter, and business unit\n      using vCenter tags and Aria Operations cost views; map to Broadcom contract\n      line items at the bundle / edition level.\n  - name: Optimization\n    description: Right-size VM core counts against the licensed core entitlement,\n      consolidate workloads onto fewer hosts, and review bundle edition (VCF vs\n      vSphere Foundation) at renewal.\n  - name: Accountability\n    description: Procurement and infrastructure-platform teams jointly own the\n      Broadcom contract; per-cluster owners are accountable for staying within the\n      negotiated entitlement.\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vmware/refs/heads/main/finops/vmware-finops.yml
sources:
- https://www.broadcom.com/products/vmware-cloud-foundation
- https://www.vmware.com/products/cloud-infrastructure/vsphere-foundation
specification: FinOps Framework
tags:
- Cloud Computing
- Virtualization
- Hybrid Cloud
- FinOps
- FOCUS
---
