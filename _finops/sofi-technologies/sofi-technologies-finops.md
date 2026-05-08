---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Product
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable (Consumer Banking)
description: FOCUS-aligned FinOps placeholder for SoFi Technologies. SoFi is a B2C banking, lending, and investing platform with no public developer billing surface; FOCUS columns describe the corporate publisher only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SoFi Bank, N.A.
  ProviderName: SoFi Technologies
  PublisherName: SoFi Technologies, Inc.
  ServiceCategory: Consumer Banking and Lending
  ServiceName: SoFi Member Banking and Lending
layout: finops
meters: []
name: Sofi Technologies Finops
provider_name: SoFi Technologies
provider_slug: sofi-technologies
publisher_name: SoFi Technologies, Inc.
service_category: Consumer Banking and Lending
slug: sofi-technologies-finops
source_filename: sofi-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.sofi.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SoFi Technologies\nproviderId: sofi-technologies\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Fintech\n  - Banking\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for SoFi Technologies. SoFi is a B2C banking, lending,\n  and investing platform with no public developer billing surface; FOCUS columns describe the corporate\n  publisher only.'\nsources:\n  - https://www.sofi.com\nnotes: SoFi Technologies does not expose a public developer API or usage-based billing surface. Meters,\n  unit prices, and ChargeCategory mappings cannot be reconciled because there are no published API consumption\n  units. Updated only if SoFi publishes a partner/developer pricing page.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SoFi Technologies, Inc.\nserviceCategory: Consumer Banking and Lending\nbillingModel:\n  pricingCategory: Not Applicable (Consumer Banking)\n  billingFrequency: Per-Product\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: SoFi Member Banking and Lending\n  ServiceCategory: Consumer Banking and Lending\n  ProviderName: SoFi Technologies\n  PublisherName: SoFi Technologies, Inc.\n  InvoiceIssuerName: SoFi Bank, N.A.\n  BillingCurrency: USD\nmeters: []\nprinciples:\n  - name: Visibility\n    description: SoFi member-facing consumption (interest, fees, investing activity) is surfaced through\n      the SoFi mobile/web app and member statements, not through a developer billing API.\n  - name: Allocation\n    description: Not applicable - SoFi is a direct-to-consumer bank without team/cost-center allocation\n      semantics on a developer surface.\n  - name: Optimization\n\
  \    description: Not applicable at the API/FinOps layer; product-level optimization (rate shopping, fee\n      avoidance) is the member's responsibility.\n  - name: Accountability\n    description: Member-level accountability is governed by the SoFi member agreement, not by a developer/tenant\n      contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sofi-technologies/refs/heads/main/finops/sofi-technologies-finops.yml
sources:
- https://www.sofi.com
specification: FinOps Framework
tags:
- Fintech
- Banking
- FinOps
- FOCUS
---
