---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: workday-studio-integration-openapi.yml
  format: yaml
  label: Workday Studio Integration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-studio/refs/heads/main/openapi/workday-studio-integration-openapi.yml
- filename: workday-studio-web-services-openapi.yml
  format: yaml
  label: Workday Web Services API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-studio/refs/heads/main/openapi/workday-studio-web-services-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps shape for Workday Studio is opaque. Studio is an IDE bundled with a Workday tenant subscription; runtime API consumption is part of the same tenant contract with no per-integration meter, FOCUS export, or public usage-billing API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: HR / Finance SaaS
  ServiceName: Workday Studio
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  name: tenant_subscription
  unit: month
name: Workday Studio Finops
provider_name: Workday Studio
provider_slug: workday-studio
publisher_name: Workday, Inc.
service_category: HR / Finance SaaS
slug: workday-studio-finops
source_filename: workday-studio-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/why-workday/about-us/contact-us.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Studio\nproviderId: workday-studio\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Integration\n  - Workday\ndescription: FinOps shape for Workday Studio is opaque. Studio is an IDE bundled with a Workday\n  tenant subscription; runtime API consumption is part of the same tenant contract with no\n  per-integration meter, FOCUS export, or public usage-billing API.\nsources:\n  - https://www.workday.com/en-us/why-workday/about-us/contact-us.html\n  - https://doc.workday.com/\nnotes: Workday does not expose a FOCUS-aligned cost export for Studio integrations. Meters and\n  charge categories cannot be reconciled without authenticated access to the customer's Workday\n  Community documentation and contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday, Inc.\nserviceCategory: HR / Finance SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Studio\n  ServiceCategory: HR / Finance SaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tenant_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: No public usage API; customers track Studio integration runs through the Workday\n      Integration Cloud monitor inside the tenant.\n  - name: Allocation\n    description: Costs allocate by Workday tenant and integration entitlement; per-integration\n      attribution depends on Studio's internal run history rather than\
  \ a billing export.\n  - name: Optimization\n    description: Levers are integration-design choices (batch sizing, schedule frequency, EIB use\n      where appropriate) rather than rate or commitment discounts.\n  - name: Accountability\n    description: Studio license is owned by Workday procurement; Studio integration design and\n      operation are owned by the integration engineering team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-studio/refs/heads/main/finops/workday-studio-finops.yml
sources:
- https://www.workday.com/en-us/why-workday/about-us/contact-us.html
- https://doc.workday.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Integration
- Workday
---
