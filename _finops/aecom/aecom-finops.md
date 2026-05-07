---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for AECOM: project-based consulting with optional digital software components.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AECOM
  ProviderName: AECOM
  PublisherName: AECOM
  ServiceCategory: Engineering and Infrastructure Services
  ServiceName: AECOM
layout: finops
meters:
- aggregation: sum
  dimensions:
  - project
  - role
  name: professional_services_hours
  unit: hour
- aggregation: sum
  dimensions:
  - product
  name: software_subscription
  unit: month
- aggregation: count
  dimensions:
  - project
  name: project_milestones
  unit: milestone
name: Aecom Finops
provider_name: AECOM
provider_slug: aecom
publisher_name: AECOM
service_category: Engineering and Infrastructure Services
slug: aecom-finops
source_filename: aecom-finops.yml
source_heading: FinOps Profile
source_url: https://digital.aecom.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AECOM\nproviderId: aecom\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: AECOM bills consulting/professional-services engagements rather than per-call API usage.\ntags:\n  - FinOps\n  - FOCUS\n  - Engineering\n  - Infrastructure\ndescription: 'FOCUS-aligned FinOps for AECOM: project-based consulting with optional digital\n  software components.'\nsources:\n  - https://digital.aecom.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AECOM\nserviceCategory: Engineering and Infrastructure Services\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n\
  \  ServiceName: AECOM\n  ServiceCategory: Engineering and Infrastructure Services\n  ProviderName: AECOM\n  PublisherName: AECOM\n  InvoiceIssuerName: AECOM\n  BillingCurrency: USD\nmeters:\n  - name: professional_services_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - project\n      - role\n  - name: software_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n  - name: project_milestones\n    unit: milestone\n    aggregation: count\n    dimensions:\n      - project\nprinciples:\n  - name: Visibility\n    description: Reconcile AECOM invoices against project SOWs; track consultant-hour burn against\n      milestones.\n  - name: Allocation\n    description: Tag spend per project, business unit, and capital vs operating budget.\n  - name: Optimization\n    description: Right-size consulting team; renegotiate digital-product subscriptions at renewal.\n  - name: Accountability\n    description: Assign project owner; review monthly\
  \ burn and re-baseline as scope shifts.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aecom/refs/heads/main/finops/aecom-finops.yml
sources:
- https://digital.aecom.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Engineering
- Infrastructure
---
