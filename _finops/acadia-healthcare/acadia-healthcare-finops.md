---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories: []
  pricingCategory: Not Applicable (Healthcare Services Provider)
description: FOCUS-aligned FinOps scaffold for Acadia Healthcare. Acadia Healthcare is a clinical services company; there is no commercial API line item to allocate. FinOps relevance is internal to Acadia's IT/EHR spend and to partner integration cost.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Acadia Healthcare Company, Inc.
  ProviderName: Acadia Healthcare
  PublisherName: Acadia Healthcare Company, Inc.
  ServiceCategory: Behavioral Health Services
  ServiceName: Acadia Healthcare
layout: finops
meters: []
name: Acadia Healthcare Finops
provider_name: Acadia Healthcare
provider_slug: acadia-healthcare
publisher_name: Acadia Healthcare Company, Inc.
service_category: Behavioral Health Services
slug: acadia-healthcare-finops
source_filename: acadia-healthcare-finops.yml
source_heading: FinOps Profile
source_url: https://www.acadiahealthcare.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Acadia Healthcare\nproviderId: acadia-healthcare\npublisherName: Acadia Healthcare Company, Inc.\nserviceCategory: Behavioral Health Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Behavioral Health\n  - Mental Health\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Acadia Healthcare. Acadia Healthcare is a clinical services\n  company; there is no commercial API line item to allocate. FinOps relevance is internal to Acadia's\n  IT/EHR spend and to partner integration cost.\nsources:\n  - https://www.acadiahealthcare.com\nnotes: No commercial API invoice exists. The meters below describe\
  \ what an internal FinOps team would\n  track around Acadia's healthcare IT integrations rather than an external billable surface.\nbillingModel:\n  pricingCategory: Not Applicable (Healthcare Services Provider)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Acadia Healthcare\n  ServiceCategory: Behavioral Health Services\n  ProviderName: Acadia Healthcare\n  PublisherName: Acadia Healthcare Company, Inc.\n  InvoiceIssuerName: Acadia Healthcare Company, Inc.\n  BillingCurrency: USD\nmeters: []\nprinciples:\n  - name: Visibility\n    description: There is no Acadia Healthcare API invoice. Visibility applies to internal IT spend on\n      EHR, HL7/FHIR integration, and clearinghouse fees that support clinical operations.\n  - name: Allocation\n    description: Allocate IT and integration cost to facility, region, and service line (acute, specialty,\n      RTC) rather than to API call volume.\n  - name: Optimization\n   \
  \ description: Optimization is operational — payer-mix, length-of-stay, and integration consolidation —\n      not API-level optimization.\n  - name: Accountability\n    description: Facility CFOs and the corporate revenue-cycle team own the operational cost lines; there\n      is no external API consumer accountable for spend.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/acadia-healthcare/refs/heads/main/finops/acadia-healthcare-finops.yml
sources:
- https://www.acadiahealthcare.com
specification: FinOps Framework
tags:
- Behavioral Health
- Mental Health
- FinOps
- FOCUS
---
