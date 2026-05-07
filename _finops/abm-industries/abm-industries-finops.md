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
  pricingCategory: Contract
description: ABM Connect is bundled with ABM facilities-services contracts; there is no metered API invoice. FinOps mapping is structural only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ABM Industries Incorporated
  ProviderName: ABM Industries
  PublisherName: ABM Industries Incorporated
  ServiceCategory: Facilities Management
  ServiceName: ABM Connect
layout: finops
meters:
- aggregation: count
  description: Facilities-services contract bundle — not a metered API unit.
  dimensions:
  - customer
  - service_line
  name: services_contract
  unit: contract
name: Abm Industries Finops
provider_name: ABM Industries
provider_slug: abm-industries
publisher_name: ABM Industries Incorporated
service_category: Facilities Management
slug: abm-industries-finops
source_filename: abm-industries-finops.yml
source_heading: FinOps Profile
source_url: https://www.abm.com/abm-connect
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ABM Industries\nproviderId: abm-industries\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Facilities Management\n  - Engineering\n  - FinOps\n  - FOCUS\ndescription: ABM Connect is bundled with ABM facilities-services contracts; there is no metered API invoice.\n  FinOps mapping is structural only.\nnotes: No public developer pricing — placeholder only. Costs flow through the master services contract,\n  not a metered API line item.\nsources:\n  - https://www.abm.com/abm-connect\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ABM Industries Incorporated\nserviceCategory: Facilities Management\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency:\
  \ Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: ABM Connect\n  ServiceCategory: Facilities Management\n  ProviderName: ABM Industries\n  PublisherName: ABM Industries Incorporated\n  InvoiceIssuerName: ABM Industries Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: services_contract\n    description: Facilities-services contract bundle — not a metered API unit.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - customer\n      - service_line\nprinciples:\n  - name: Visibility\n    description: ABM Connect dashboards expose facility, financial, and IoT data to the customer; track\n      usage as part of facilities operations rather than a metered API.\n  - name: Allocation\n    description: Allocate cost to the facilities-management or real-estate function that owns the ABM\n      services contract.\n  - name: Optimization\n    description: Optimize by tuning IoT polling cadence and analytics-job frequency\
  \ inside ABM Connect\n      to actual decision needs.\n  - name: Accountability\n    description: Real-estate / facilities leadership owns the ABM relationship; IT owns the data-feed\n      integration. Review usage during quarterly business reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abm-industries/refs/heads/main/finops/abm-industries-finops.yml
sources:
- https://www.abm.com/abm-connect
specification: FinOps Framework
tags:
- Facilities Management
- Engineering
- FinOps
- FOCUS
---
