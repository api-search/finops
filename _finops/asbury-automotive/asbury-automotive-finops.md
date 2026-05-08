---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable (No Public API)
description: FinOps shape for Asbury Automotive Group — Asbury is an automotive retailer, not an API provider. There is no public API consumption to bill or allocate. This artifact captures the FOCUS-aligned null shape so the Plans/Rate-Limits/FinOps triad is structurally complete.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Asbury Automotive Group, Inc.
  PricingCategory: Not Applicable
  ProviderName: Asbury Automotive Group
  PublisherName: Asbury Automotive Group, Inc.
  ServiceCategory: Automotive Retail
  ServiceName: Asbury Automotive Group
layout: finops
meters:
- aggregation: count
  description: No API-level metering exists for this provider
  name: not_applicable
  unit: varies
name: Asbury Automotive Finops
provider_name: Asbury Automotive Group
provider_slug: asbury-automotive
publisher_name: Asbury Automotive Group, Inc.
service_category: Automotive Retail
slug: asbury-automotive-finops
source_filename: asbury-automotive-finops.yml
source_heading: FinOps Profile
source_url: https://www.asburyauto.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Asbury Automotive Group\nproviderId: asbury-automotive\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Automotive\n  - Dealerships\n  - Retail\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Asbury Automotive Group — Asbury is an automotive retailer, not an API\n  provider. There is no public API consumption to bill or allocate. This artifact captures the\n  FOCUS-aligned null shape so the Plans/Rate-Limits/FinOps triad is structurally complete.\nsources:\n  - https://www.asburyauto.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: No API-level billing exists. Any FinOps treatment would apply to Asbury's vendor spend with its\n  DMS/OEM/marketing-tech partners, which is outside this artifact's scope.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Asbury Automotive Group, Inc.\nserviceCategory: Automotive Retail\nbillingModel:\n  pricingCategory: Not Applicable (No Public API)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Asbury Automotive Group\n  ServiceCategory: Automotive Retail\n  ProviderName: Asbury Automotive Group\n  PublisherName: Asbury Automotive Group, Inc.\n  InvoiceIssuerName: Asbury Automotive Group, Inc.\n  BillingCurrency: USD\n  PricingCategory: Not Applicable\nmeters:\n  - name: not_applicable\n    description: No API-level metering exists for this provider\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Not applicable — no API consumption to surface.\n  - name: Allocation\n    description: Not applicable — no API spend to allocate.\n  - name: Optimization\n    description:\
  \ Not applicable — no API consumption levers.\n  - name: Accountability\n    description: Not applicable — no API-level cost owner.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/asbury-automotive/refs/heads/main/finops/asbury-automotive-finops.yml
sources:
- https://www.asburyauto.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Automotive
- Dealerships
- Retail
- FinOps
- FOCUS
---
