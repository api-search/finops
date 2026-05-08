---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: symantec-sepm-api-openapi.yml
  format: yaml
  label: Symantec Endpoint Protection Manager API
  slug: sepm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/symantec/refs/heads/main/openapi/symantec-sepm-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Enterprise License
description: Symantec API access is bundled with Broadcom-issued enterprise security licenses (SEPM, SES, EDR, DLP); there is no published usage-based pricing or FOCUS-aligned export, so FinOps shape is approximated from license-bundle invoices.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Broadcom Inc.
  ProviderName: Symantec (Broadcom)
  PublisherName: Broadcom Inc.
  ServiceCategory: Cybersecurity / Endpoint Security
  ServiceName: Symantec Enterprise Cloud
layout: finops
meters:
- aggregation: max
  description: Per-endpoint license counts for SEPM/SES (the primary commercial unit for endpoint protection).
  name: endpoint_licenses
  unit: endpoint
- aggregation: max
  description: Data volume protected by DLP / monitored channels - typical commercial unit for the DLP product line.
  name: protected_data_volume
  unit: GB
- aggregation: max
  description: Endpoints under EDR coverage; commercial unit for the EDR product line.
  name: edr_licensed_endpoints
  unit: endpoint
name: Symantec Finops
provider_name: Symantec
provider_slug: symantec
publisher_name: Broadcom Inc. (Symantec Enterprise Cloud)
service_category: Cybersecurity / Endpoint Security
slug: symantec-finops
source_filename: symantec-finops.yml
source_heading: FinOps Profile
source_url: https://www.broadcom.com/products/cybersecurity/endpoint
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Symantec\nproviderId: symantec\npublisherName: Broadcom Inc. (Symantec Enterprise Cloud)\nserviceCategory: Cybersecurity / Endpoint Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cybersecurity\n  - Endpoint Security\n  - FinOps\n  - FOCUS\ndescription: Symantec API access is bundled with Broadcom-issued enterprise security licenses (SEPM, SES, EDR, DLP); there is no published usage-based pricing or FOCUS-aligned export, so FinOps shape is approximated from license-bundle invoices.\nsources:\n  - https://www.broadcom.com/products/cybersecurity/endpoint\n  - https://apidocs.symantec.com/\n  - https://apidocs.securitycloud.symantec.com/\n\
  notes: Broadcom does not publish a usage-metered API pricing surface for Symantec products. Cost data must be reconciled from negotiated enterprise license invoices issued by Broadcom Inc.\nbillingModel:\n  pricingCategory: Enterprise License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Symantec Enterprise Cloud\n  ServiceCategory: Cybersecurity / Endpoint Security\n  ProviderName: Symantec (Broadcom)\n  PublisherName: Broadcom Inc.\n  InvoiceIssuerName: Broadcom Inc.\n  BillingCurrency: USD\nmeters:\n  - name: endpoint_licenses\n    description: Per-endpoint license counts for SEPM/SES (the primary commercial unit for endpoint protection).\n    unit: endpoint\n    aggregation: max\n  - name: protected_data_volume\n    description: Data volume protected by DLP / monitored channels - typical commercial unit for the DLP product line.\n    unit: GB\n    aggregation: max\n  - name: edr_licensed_endpoints\n\
  \    description: Endpoints under EDR coverage; commercial unit for the EDR product line.\n    unit: endpoint\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Cost visibility is on a per-license basis from Broadcom's commercial portal; the API surface itself is not separately metered or invoiced.\n  - name: Allocation\n    description: Allocate by product (SEPM/SES/EDR/DLP) and by managed endpoint count - the same units used on the Broadcom invoice.\n  - name: Optimization\n    description: Optimization levers are commercial - right-size endpoint counts, consolidate to the unified Symantec Enterprise Cloud bundle, and renegotiate at term boundaries.\n  - name: Accountability\n    description: Security/IT operations owns endpoint counts; procurement/legal owns the Broadcom contract; together they reconcile against the Broadcom invoice.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/symantec/refs/heads/main/finops/symantec-finops.yml
sources:
- https://www.broadcom.com/products/cybersecurity/endpoint
- https://apidocs.symantec.com/
- https://apidocs.securitycloud.symantec.com/
specification: FinOps Framework
tags:
- Cybersecurity
- Endpoint Security
- FinOps
- FOCUS
---
