---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: workday-tracking-system-time-tracking-openapi.yml
  format: yaml
  label: Workday Time Tracking API
  slug: workday-time-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-tracking-system/refs/heads/main/openapi/workday-tracking-system-time-tracking-openapi.yml
- filename: workday-tracking-system-absence-management-openapi.yml
  format: yaml
  label: Workday Absence Management API
  slug: workday-absence-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-tracking-system/refs/heads/main/openapi/workday-tracking-system-absence-management-openapi.yml
- filename: workday-tracking-system-scheduling-openapi.yml
  format: yaml
  label: Workday Scheduling API
  slug: workday-scheduling-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-tracking-system/refs/heads/main/openapi/workday-tracking-system-scheduling-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps shape for the Workday Tracking System is opaque. API consumption is bundled with a negotiated Workday tenant subscription; there is no per-request meter, FOCUS-aligned cost export, or public usage-billing API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: HR / Workforce SaaS
  ServiceName: Workday Tracking System
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  name: tenant_subscription
  unit: month
name: Workday Tracking System Finops
provider_name: Workday Tracking System
provider_slug: workday-tracking-system
publisher_name: Workday, Inc.
service_category: HR / Workforce SaaS
slug: workday-tracking-system-finops
source_filename: workday-tracking-system-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/products/human-capital-management/time-tracking.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Tracking System\nproviderId: workday-tracking-system\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Time Tracking\n  - Workforce Management\n  - Workday\ndescription: FinOps shape for the Workday Tracking System is opaque. API consumption is bundled\n  with a negotiated Workday tenant subscription; there is no per-request meter, FOCUS-aligned\n  cost export, or public usage-billing API.\nsources:\n  - https://www.workday.com/en-us/products/human-capital-management/time-tracking.html\n  - https://community.workday.com/api\nnotes: Workday does not expose a FOCUS-aligned cost export for time-tracking integrations. Meters\n  and charge categories cannot be reconciled without authenticated access to the customer's\n  Workday Community documentation and contract.\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday, Inc.\nserviceCategory: HR / Workforce SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Tracking System\n  ServiceCategory: HR / Workforce SaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tenant_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: No public usage API. Customers see time-tracking integration volume through the\n      Workday Integration Cloud monitor inside the tenant.\n  - name: Allocation\n    description: Costs allocate by Workday tenant and HCM/Time Tracking subscription\
  \ line; per-\n      integration attribution depends on internal Workday telemetry rather than a billing export.\n  - name: Optimization\n    description: Levers are integration-design choices (batch time-block submission, scheduled\n      pulls vs. event-driven webhooks where available, ISU reuse).\n  - name: Accountability\n    description: Workday subscription is owned by HR / Workforce procurement; Time Tracking\n      integration design and run-time costs are owned by the integration engineering team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-tracking-system/refs/heads/main/finops/workday-tracking-system-finops.yml
sources:
- https://www.workday.com/en-us/products/human-capital-management/time-tracking.html
- https://community.workday.com/api
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Time Tracking
- Workforce Management
- Workday
---
