---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: Authentication_OpenAPI.json
  format: json
  label: Workday Authentication API
  slug: workday-authentication-api
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Security/v44.0/Authentication_OpenAPI.json
- filename: Identity_Management_OpenAPI.json
  format: json
  label: Workday Identity Management API
  slug: workday-identity-management-api
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Security/v44.0/Identity_Management_OpenAPI.json
- filename: Security_Groups_OpenAPI.json
  format: json
  label: Workday Security Groups API
  slug: workday-security-groups-api
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Security/v44.0/Security_Groups_OpenAPI.json
- filename: Audit_OpenAPI.json
  format: json
  label: Workday Audit and Compliance API
  slug: workday-audit-and-compliance-api
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Security/v44.0/Audit_OpenAPI.json
- filename: Privacy_OpenAPI.json
  format: json
  label: Workday Privacy API
  slug: workday-privacy-api
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Security/v44.0/Privacy_OpenAPI.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps shape for Workday Security is opaque. API consumption is bundled with a negotiated Workday tenant subscription; there is no per-request meter, FOCUS-aligned cost export, or public usage-billing API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Workday, Inc.
  ProviderName: Workday
  PublisherName: Workday, Inc.
  ServiceCategory: HR / Finance SaaS
  ServiceName: Workday Security
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  name: tenant_subscription
  unit: month
name: Workday Security Finops
provider_name: Workday Security
provider_slug: workday-security
publisher_name: Workday, Inc.
service_category: HR / Finance SaaS
slug: workday-security-finops
source_filename: workday-security-finops.yml
source_heading: FinOps Profile
source_url: https://www.workday.com/en-us/why-workday/about-us/contact-us.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workday Security\nproviderId: workday-security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Security\n  - Identity\n  - Workday\ndescription: FinOps shape for Workday Security is opaque. API consumption is bundled with a\n  negotiated Workday tenant subscription; there is no per-request meter, FOCUS-aligned cost export,\n  or public usage-billing API.\nsources:\n  - https://www.workday.com/en-us/why-workday/about-us/contact-us.html\n  - https://community.workday.com/api\nnotes: Workday does not expose a usage-billing API or FOCUS export for security-API consumption.\n  Meters, charge categories, and unit economics cannot be reconciled without authenticated access\n  to the customer's Workday Community documentation and contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workday, Inc.\nserviceCategory: HR / Finance SaaS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Workday Security\n  ServiceCategory: HR / Finance SaaS\n  ProviderName: Workday\n  PublisherName: Workday, Inc.\n  InvoiceIssuerName: Workday, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tenant_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: No public usage API for security calls. Customers rely on the Workday Audit API\n      and contract-level reporting to see authentication and security-event volume.\n  - name: Allocation\n    description: Costs allocate by Workday tenant and product subscription line; per-integration\n      attribution requires capturing\
  \ Integration System User identity in client-side telemetry.\n  - name: Optimization\n    description: Levers are integration-design choices (token caching, batched audit reads, SSO\n      reuse) rather than rate or commitment discounts.\n  - name: Accountability\n    description: Workday subscription is owned by HR/IT procurement; security-API consumption is\n      owned by the integrations and IAM teams that issue OAuth/ISU credentials.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-security/refs/heads/main/finops/workday-security-finops.yml
sources:
- https://www.workday.com/en-us/why-workday/about-us/contact-us.html
- https://community.workday.com/api
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Security
- Identity
- Workday
---
