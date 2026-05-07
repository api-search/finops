---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: synopsys-polaris-openapi.yml
  format: yaml
  label: Synopsys Polaris API
  slug: polaris
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/synopsys/refs/heads/main/openapi/synopsys-polaris-openapi.yml
- filename: synopsys-cloud-openlink-openapi.yml
  format: yaml
  label: Synopsys Cloud OpenLink API
  slug: cloud-openlink
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/synopsys/refs/heads/main/openapi/synopsys-cloud-openlink-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Enterprise License
description: Synopsys's APIs are bundled with paid product licenses (Polaris, Coverity, Seeker for AppSec; Synopsys Cloud / OpenLink for EDA). There is no usage-metered API billing surface; FinOps shape is approximated against the underlying license invoice.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Synopsys, Inc. / Black Duck Software, Inc.
  ProviderName: Synopsys
  PublisherName: Synopsys, Inc.
  ServiceCategory: Application Security / EDA
  ServiceName: Synopsys APIs (Polaris, Coverity, Seeker, Cloud OpenLink)
layout: finops
meters:
- aggregation: max
  description: Developer / contributor licenses on Polaris, Coverity, and Seeker (the typical commercial unit for AppSec).
  name: appsec_developer_licenses
  unit: developer
- aggregation: max
  description: Applications under scan / SCA - alternate commercial unit on some Polaris and Black Duck SKUs.
  name: scanned_applications
  unit: application
- aggregation: sum
  description: Synopsys Cloud / EDA tool license-months; the dominant commercial unit on the EDA side.
  name: eda_license_months
  unit: license-month
- aggregation: count
  description: License entitlements distributed through the Cloud OpenLink API.
  name: openlink_entitlements
  unit: entitlement
name: Synopsys Finops
provider_name: Synopsys
provider_slug: synopsys
publisher_name: Synopsys, Inc. (Software Integrity products billed via Black Duck Software, Inc.)
service_category: Application Security / EDA
slug: synopsys-finops
source_filename: synopsys-finops.yml
source_heading: FinOps Profile
source_url: https://www.synopsys.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Synopsys\nproviderId: synopsys\npublisherName: Synopsys, Inc. (Software Integrity products billed via Black Duck Software, Inc.)\nserviceCategory: Application Security / EDA\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Security\n  - EDA\n  - Semiconductor\n  - FinOps\n  - FOCUS\ndescription: Synopsys's APIs are bundled with paid product licenses (Polaris, Coverity, Seeker for AppSec; Synopsys Cloud / OpenLink for EDA). There is no usage-metered API billing surface; FinOps shape is approximated against the underlying license invoice.\nsources:\n  - https://www.synopsys.com\n  - https://polaris.synopsys.com/developer/default/documentation\n\
  \  - https://www.synopsys.com/cloud/openlink/api.html\nnotes: No FOCUS-aligned per-call billing surface. Cost data is reconciled from license invoices issued by Synopsys, Inc. (EDA / Synopsys Cloud) and Black Duck Software, Inc. (former Synopsys Software Integrity Group products).\nbillingModel:\n  pricingCategory: Enterprise License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Synopsys APIs (Polaris, Coverity, Seeker, Cloud OpenLink)\n  ServiceCategory: Application Security / EDA\n  ProviderName: Synopsys\n  PublisherName: Synopsys, Inc.\n  InvoiceIssuerName: Synopsys, Inc. / Black Duck Software, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: appsec_developer_licenses\n    description: Developer / contributor licenses on Polaris, Coverity, and Seeker (the typical commercial unit for AppSec).\n    unit: developer\n    aggregation: max\n  - name: scanned_applications\n    description: Applications\
  \ under scan / SCA - alternate commercial unit on some Polaris and Black Duck SKUs.\n    unit: application\n    aggregation: max\n  - name: eda_license_months\n    description: Synopsys Cloud / EDA tool license-months; the dominant commercial unit on the EDA side.\n    unit: license-month\n    aggregation: sum\n  - name: openlink_entitlements\n    description: License entitlements distributed through the Cloud OpenLink API.\n    unit: entitlement\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Visibility is on a per-license basis from Synopsys / Black Duck commercial portals; the API surface itself is not separately metered or invoiced.\n  - name: Allocation\n    description: Allocate by product (Polaris/Coverity/Seeker/Cloud) and by developer or application count - the same units Synopsys and Black Duck use on their invoices.\n  - name: Optimization\n    description: Optimization is commercial - right-size developer counts, consolidate AppSec tools onto a\
  \ single platform, schedule EDA jobs to reduce concurrent license-month consumption, and renegotiate at term boundaries.\n  - name: Accountability\n    description: AppSec / DevSecOps team owns developer counts and scan policies; semiconductor design team owns EDA license consumption; procurement owns the Synopsys/Black Duck contracts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/synopsys/refs/heads/main/finops/synopsys-finops.yml
sources:
- https://www.synopsys.com
- https://polaris.synopsys.com/developer/default/documentation
- https://www.synopsys.com/cloud/openlink/api.html
specification: FinOps Framework
tags:
- Application Security
- EDA
- Semiconductor
- FinOps
- FOCUS
---
