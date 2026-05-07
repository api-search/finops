---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: motorola-solutions-motorola-api-openapi.yml
  format: yaml
  label: Motorola Solutions API
  slug: motorola-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/motorola-solutions/refs/heads/main/openapi/motorola-solutions-motorola-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Term License + Project Services
description: 'FOCUS-aligned FinOps for Motorola Solutions: API access is gated through the Application Partner Developer Program. MOTOTRBO API licenses are free for 3-year terms; ASTRO 25 carries a project-quoted license fee. There is no metered consumption surface — costs are fixed-term licenses plus the underlying radio-system contract.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Motorola Solutions, Inc.
  ProviderName: Motorola Solutions
  PublisherName: Motorola Solutions, Inc.
  ServiceCategory: Public Safety Communications
  ServiceName: Motorola Solutions ADP APIs
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - partner
  name: api_license_term
  unit: year
- aggregation: sum
  dimensions:
  - product
  - phase
  name: implementation_services
  unit: project
- aggregation: sum
  dimensions:
  - product
  name: support_maintenance
  unit: year
name: Motorola Solutions Finops
provider_name: Motorola Solutions
provider_slug: motorola-solutions
publisher_name: Motorola Solutions, Inc.
service_category: Public Safety / Communications
slug: motorola-solutions-finops
source_filename: motorola-solutions-finops.yml
source_heading: FinOps Profile
source_url: https://www.motorolasolutions.com/en_us/partners/become-partner/application-partner-developer-program.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Motorola Solutions\nproviderId: motorola-solutions\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Public Safety\n  - Land Mobile Radio\n  - Mission Critical\ndescription: 'FOCUS-aligned FinOps for Motorola Solutions: API access is gated through the Application\n  Partner Developer Program. MOTOTRBO API licenses are free for 3-year terms; ASTRO 25 carries a project-quoted\n  license fee. There is no metered consumption surface — costs are fixed-term licenses plus the underlying\n  radio-system contract.'\nsources:\n  - https://www.motorolasolutions.com/en_us/partners/become-partner/application-partner-developer-program.html\n  - https://www.motorolasolutions.com/en_xa/developers/application-partner-developer-program/faqs.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Motorola Solutions, Inc.\nserviceCategory: Public Safety / Communications\nbillingModel:\n  pricingCategory: Term License + Project Services\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Motorola Solutions ADP APIs\n  ServiceCategory: Public Safety Communications\n  ProviderName: Motorola Solutions\n  PublisherName: Motorola Solutions, Inc.\n  InvoiceIssuerName: Motorola Solutions, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_license_term\n    unit: year\n    aggregation: max\n    dimensions:\n      - product\n      - partner\n  - name: implementation_services\n    unit: project\n    aggregation: sum\n    dimensions:\n      - product\n      - phase\n  - name: support_maintenance\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n\
  \  - name: Visibility\n    description: Track ADP license status (renewal date, scope) and project-services invoices in the financial\n      system; the platform itself emits no per-call billing telemetry.\n  - name: Allocation\n    description: Allocate ADP license cost to the partner product line that ships against MOTOTRBO, ASTRO\n      25, TETRA / DIMETRA, IMW, or broadband Push-to-X.\n  - name: Optimization\n    description: Optimization is realized by choosing the minimum required API surface (MOTOTRBO is free\n      for a 3-year term; ASTRO 25 carries a fee) and by aligning renewal cycles across partner products.\n  - name: Accountability\n    description: The partner program PM owns ADP license renewal; the integration engineering lead monitors\n      operational health inside the deployed radio system; procurement owns the renewal calendar.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/motorola-solutions/refs/heads/main/finops/motorola-solutions-finops.yml
sources:
- https://www.motorolasolutions.com/en_us/partners/become-partner/application-partner-developer-program.html
- https://www.motorolasolutions.com/en_xa/developers/application-partner-developer-program/faqs.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Public Safety
- Land Mobile Radio
- Mission Critical
---
