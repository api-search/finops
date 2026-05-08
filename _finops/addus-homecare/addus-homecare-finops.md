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
description: FOCUS-aligned FinOps scaffold for Addus HomeCare. Addus is a clinical services company; there is no commercial API line item to allocate. FinOps relevance is internal — to Addus's own IT, EVV, scheduling, and clearinghouse spend rather than an external billable surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Addus HealthCare, Inc.
  ProviderName: Addus HomeCare
  PublisherName: Addus HealthCare, Inc.
  ServiceCategory: Home Care / Hospice / Home Health Services
  ServiceName: Addus HomeCare
layout: finops
meters: []
name: Addus Homecare Finops
provider_name: Addus HomeCare
provider_slug: addus-homecare
publisher_name: Addus HealthCare, Inc.
service_category: Home Care / Hospice / Home Health Services
slug: addus-homecare-finops
source_filename: addus-homecare-finops.yml
source_heading: FinOps Profile
source_url: https://www.addus.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Addus HomeCare\nproviderId: addus-homecare\npublisherName: Addus HealthCare, Inc.\nserviceCategory: Home Care / Hospice / Home Health Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Home Care\n  - Healthcare Services\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Addus HomeCare. Addus is a clinical services company;\n  there is no commercial API line item to allocate. FinOps relevance is internal — to Addus's own IT,\n  EVV, scheduling, and clearinghouse spend rather than an external billable surface.\nsources:\n  - https://www.addus.com\nnotes: No commercial API invoice exists. Reconciled\
  \ flag is false because there is no provider invoice\n  to map to FOCUS columns.\nbillingModel:\n  pricingCategory: Not Applicable (Healthcare Services Provider)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Addus HomeCare\n  ServiceCategory: Home Care / Hospice / Home Health Services\n  ProviderName: Addus HomeCare\n  PublisherName: Addus HealthCare, Inc.\n  InvoiceIssuerName: Addus HealthCare, Inc.\n  BillingCurrency: USD\nmeters: []\nprinciples:\n  - name: Visibility\n    description: There is no Addus API invoice. Visibility applies to internal IT spend on EVV (Electronic\n      Visit Verification), scheduling, payer EDI, and clearinghouse fees that support clinical operations.\n  - name: Allocation\n    description: Allocate IT and integration cost to branch / region and service line (personal care,\n      hospice, home health) rather than to API call volume.\n  - name: Optimization\n    description: Optimization\
  \ is operational — caregiver utilization, EVV compliance, payer-mix, and\n      consolidation of integration vendors — not API-level optimization.\n  - name: Accountability\n    description: Branch and regional operations leadership own field-cost lines; the corporate revenue-cycle\n      and IT teams own the integration and clearinghouse cost lines. There is no external API consumer\n      accountable for spend.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/addus-homecare/refs/heads/main/finops/addus-homecare-finops.yml
sources:
- https://www.addus.com
specification: FinOps Framework
tags:
- Home Care
- Healthcare Services
- FinOps
- FOCUS
---
