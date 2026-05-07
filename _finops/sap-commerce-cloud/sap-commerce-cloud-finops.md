---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: overview
  format: yaml
  label: Commerce Web Services API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/commerce_web_services/overview
- filename: sap-commerce-cloud-assisted-service-openapi.yml
  format: yaml
  label: Assisted Service Module API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-commerce-cloud/refs/heads/main/openapi/sap-commerce-cloud-assisted-service-openapi.yml
- filename: sap-commerce-cloud-integration-openapi.yml
  format: yaml
  label: Integration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-commerce-cloud/refs/heads/main/openapi/sap-commerce-cloud-integration-openapi.yml
- filename: sap-commerce-cloud-admin-openapi.yml
  format: yaml
  label: Admin API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-commerce-cloud/refs/heads/main/openapi/sap-commerce-cloud-admin-openapi.yml
- filename: sap-commerce-cloud-product-content-management-openapi.yml
  format: yaml
  label: Product Content Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-commerce-cloud/refs/heads/main/openapi/sap-commerce-cloud-product-content-management-openapi.yml
billing_model:
  billingCurrency: USD/EUR/varies
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps placeholder for SAP Commerce Cloud. GMV-banded subscription with non-prod environment add-ons.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP Commerce Cloud
  PublisherName: SAP SE
  ServiceCategory: E-Commerce Platform
  ServiceName: SAP Commerce Cloud
layout: finops
meters:
- aggregation: sum
  description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual provider-published meters once available.
  dimensions:
  - service
  - region
  name: contracted_consumption
  unit: varies
name: Sap Commerce Cloud Finops
provider_name: SAP Commerce Cloud
provider_slug: sap-commerce-cloud
publisher_name: SAP SE
service_category: E-Commerce Platform
slug: sap-commerce-cloud-finops
source_filename: sap-commerce-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com/products/crm/commerce-cloud.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP Commerce Cloud\nproviderId: sap-commerce-cloud\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - B2B\n  - B2C\n  - Commerce\n  - Customer Experience\n  - Ecommerce\n  - Omnichannel\n  - Retail\ndescription: FOCUS-aligned FinOps placeholder for SAP Commerce Cloud. GMV-banded subscription with non-prod environment add-ons.\nsources:\n  - https://www.sap.com/products/crm/commerce-cloud.html\n  - https://help.sap.com/docs/SAP_COMMERCE_CLOUD_PUBLIC_CLOUD\nnotes: Provider does not publish a public, machine-readable rate card; meters and FOCUS columns below are placeholders to be reconciled once contract or partner-portal terms are available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: SAP SE\nserviceCategory: E-Commerce Platform\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/varies\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SAP Commerce Cloud\n  ServiceCategory: E-Commerce Platform\n  ProviderName: SAP Commerce Cloud\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n  - name: contracted_consumption\n    description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual\n      provider-published meters once available.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\nprinciples:\n  - name: Visibility\n    description: Use SAP for Me, the BTP Cockpit, or the SAP Concur admin console (as applicable) to\n      view consumption against entitlements; line items appear on the SAP / Concur invoice.\n  - name: Allocation\n\
  \    description: Allocate by SAP global account / subaccount or by Concur entity; map to internal cost\n      centers via the relevant cockpit before chargeback.\n  - name: Optimization\n    description: Track CPEA/BTPEA balance burn or per-employee subscription utilization; right-size service\n      plans and prune unused entitlements at renewal.\n  - name: Accountability\n    description: Designate a single billing owner and reconcile invoices monthly with usage reports from\n      the relevant SAP / Concur cockpit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-commerce-cloud/refs/heads/main/finops/sap-commerce-cloud-finops.yml
sources:
- https://www.sap.com/products/crm/commerce-cloud.html
- https://help.sap.com/docs/SAP_COMMERCE_CLOUD_PUBLIC_CLOUD
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- B2B
- B2C
- Commerce
- Customer Experience
- Ecommerce
- Omnichannel
- Retail
---
