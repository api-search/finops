---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Adobe Photoshop API
  slug: photoshop-api
  spec_type: OpenAPI
  url: https://developer.adobe.com/photoshop/api/openapi.json
- filename: openapi.json
  format: json
  label: Adobe Lightroom API
  slug: lightroom-api
  spec_type: OpenAPI
  url: https://developer.adobe.com/lightroom/api/openapi.json
- filename: openapi.json
  format: json
  label: Adobe Stock API
  slug: stock-api
  spec_type: OpenAPI
  url: https://developer.adobe.com/stock/docs/api/openapi.json
- filename: adobe-creative-suite-firefly-openapi.yml
  format: yaml
  label: Adobe Firefly API
  slug: firefly-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-suite/refs/heads/main/openapi/adobe-creative-suite-firefly-openapi.yml
- filename: adobe-creative-suite-pdf-services-openapi.yml
  format: yaml
  label: Adobe PDF Services API
  slug: pdf-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-suite/refs/heads/main/openapi/adobe-creative-suite-pdf-services-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: One-Time
  chargeCategories:
  - Purchase
  pricingCategory: Discontinued (Perpetual License)
description: Creative Suite is no longer commercially available. There is no active billing model. Customers should reference the adobe-creative-cloud FinOps artifact for the current Adobe creative-tools cost surface.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Creative SaaS (Discontinued)
  ServiceName: Adobe Creative Suite
layout: finops
meters:
- aggregation: sum
  description: Historical CS6 perpetual license (no longer sold)
  name: legacy_license
  unit: license
name: Adobe Creative Suite Finops
provider_name: Adobe Creative Suite
provider_slug: adobe-creative-suite
publisher_name: Adobe Inc.
service_category: Creative SaaS (Discontinued)
slug: adobe-creative-suite-finops
source_filename: adobe-creative-suite-finops.yml
source_heading: FinOps Profile
source_url: https://helpx.adobe.com/creative-suite/kb/creative-suite-end-support.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Creative Suite\nproviderId: adobe-creative-suite\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Creative Suite\n  - Legacy\nnotes: >-\n  Creative Suite is a discontinued perpetual-license product. No active\n  billing surface; no FinOps levers. This artifact is retained for catalog\n  completeness only and points consumers to the adobe-creative-cloud repo\n  for the active replacement.\ndescription: >-\n  Creative Suite is no longer commercially available. There is no active\n  billing model. Customers should reference the adobe-creative-cloud\n  FinOps artifact for the current Adobe creative-tools cost surface.\nsources:\n  - https://helpx.adobe.com/creative-suite/kb/creative-suite-end-support.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\nserviceCategory: Creative SaaS (Discontinued)\nbillingModel:\n  pricingCategory: Discontinued (Perpetual License)\n  billingFrequency: One-Time\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Adobe Creative Suite\n  ServiceCategory: Creative SaaS (Discontinued)\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: legacy_license\n    description: Historical CS6 perpetual license (no longer sold)\n    unit: license\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Inventory remaining CS6 installs in asset-management tooling;\n      reclassify any active spend as legacy / unsupported.\n  - name: Allocation\n    description: >-\n      Existing CS6 installs should be tracked\
  \ per device / user for\n      sunset-planning purposes only.\n  - name: Optimization\n    description: >-\n      Migrate users to Creative Cloud subscriptions; the security and\n      compatibility risk of running unsupported CS6 is no longer cost-justified.\n  - name: Accountability\n    description: >-\n      IT / security team owns the migration roadmap from CS6 to Creative Cloud.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-suite/refs/heads/main/finops/adobe-creative-suite-finops.yml
sources:
- https://helpx.adobe.com/creative-suite/kb/creative-suite-end-support.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Creative Suite
- Legacy
---
