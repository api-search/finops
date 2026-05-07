---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: whatfix-openapi.yml
  format: yaml
  label: Whatfix API
  slug: whatfix-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/whatfix/refs/heads/main/openapi/whatfix-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription + Per-User
description: FinOps shape for Whatfix is a SaaS platform license - flat platform fee plus user-license fees, with employee-facing apps billed by total licensed users and customer-facing apps billed by monthly active users.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Whatfix Inc.
  ProviderName: Whatfix
  PublisherName: Whatfix Inc.
  ServiceCategory: Digital Adoption Platform
  ServiceName: Whatfix
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product_line
  - tier
  name: platform_subscription
  unit: month
- aggregation: max
  dimensions:
  - product_line
  - tier
  name: licensed_users_employee
  unit: seat
- aggregation: max
  dimensions:
  - product_line
  - tier
  name: monthly_active_users_customer
  unit: monthly_active_user
name: Whatfix Finops
provider_name: Whatfix
provider_slug: whatfix
publisher_name: Whatfix Inc.
service_category: Digital Adoption Platform
slug: whatfix-finops
source_filename: whatfix-finops.yml
source_heading: FinOps Profile
source_url: https://whatfix.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Whatfix\nproviderId: whatfix\npublisherName: Whatfix Inc.\nserviceCategory: Digital Adoption Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Digital Adoption\n  - SaaS Management\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps shape for Whatfix is a SaaS platform license - flat platform fee plus user-license fees, with employee-facing apps billed by total licensed users and customer-facing apps billed by monthly active users.\nsources:\n  - https://whatfix.com/pricing/\nnotes: Public pricing page confirms the flat-fee + per-user model but provides no dollar figures. Meters reflect the documented\
  \ billing shape; unit prices remain in the contract.\nbillingModel:\n  pricingCategory: Subscription + Per-User\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Whatfix\n  ServiceCategory: Digital Adoption Platform\n  ProviderName: Whatfix\n  PublisherName: Whatfix Inc.\n  InvoiceIssuerName: Whatfix Inc.\n  BillingCurrency: USD\nmeters:\n  - name: platform_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product_line\n      - tier\n  - name: licensed_users_employee\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product_line\n      - tier\n  - name: monthly_active_users_customer\n    unit: monthly_active_user\n    aggregation: max\n    dimensions:\n      - product_line\n      - tier\nprinciples:\n  - name: Visibility\n    description: Use the Whatfix admin / Product Analytics dashboards to track active-user counts feeding the MAU-billed lines,\
  \ and reconcile against the order form for licensed-seat lines.\n  - name: Allocation\n    description: Allocate by product line (DAP web, mobile, OS, Product Analytics) and by tenant / business unit; tag MAUs in customer-facing apps to the consuming product.\n  - name: Optimization\n    description: Right-size by trimming unused licensed seats at renewal, and by gating which customer surfaces actually count toward MAU billing.\n  - name: Accountability\n    description: Procurement / IT owns the master subscription and renewal; product owners track MAU drift since they directly drive variable cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/whatfix/refs/heads/main/finops/whatfix-finops.yml
sources:
- https://whatfix.com/pricing/
specification: FinOps Framework
tags:
- Digital Adoption
- SaaS Management
- FinOps
- FOCUS
- Contact Sales
---
