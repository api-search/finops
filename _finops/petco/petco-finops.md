---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Petco is a pet specialty retailer, not a software / API vendor. From a FinOps perspective, there is no metered API surface; partner integration cost lives in the partner's own integration platform and any contracted Petco-side fees.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  ProviderName: Petco
  PublisherName: Petco Health and Wellness Company, Inc.
  ServiceCategory: B2B Integration
  ServiceName: Petco Partner Integration
layout: finops
meters:
- aggregation: count
  description: Negotiated partner / vendor integration relationship.
  dimensions:
  - partner_type
  name: integration_contract
  unit: contract
name: Petco Finops
provider_name: Petco Animal Supplies
provider_slug: petco
publisher_name: Petco Health and Wellness Company, Inc.
service_category: B2B Integration
slug: petco-finops
source_filename: petco-finops.yml
source_heading: FinOps Profile
source_url: https://www.petco.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Petco Animal Supplies\nproviderId: petco\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Retail\n  - Pet Care\nnotes: Petco is not an API or platform vendor. There is no public metered SKU to model. This\n  artifact captures the FinOps shape only at the contract level for partner integration spend.\ndescription: Petco is a pet specialty retailer, not a software / API vendor. From a FinOps\n  perspective, there is no metered API surface; partner integration cost lives in the partner's\n  own integration platform and any contracted Petco-side fees.\nsources:\n  - https://www.petco.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Petco Health and Wellness Company, Inc.\nserviceCategory: B2B Integration\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Petco Partner Integration\n  ServiceCategory: B2B Integration\n  ProviderName: Petco\n  PublisherName: Petco Health and Wellness Company, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: integration_contract\n    description: Negotiated partner / vendor integration relationship.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - partner_type\nprinciples:\n  - name: Visibility\n    description: Visibility lives at the contract level rather than per-API-call.\n  - name: Allocation\n    description: Allocate integration cost to the consuming Petco line of business (retail, vet,\n      grooming, marketplace).\n  - name: Optimization\n    description: Consolidate vendor integrations onto a managed integration\
  \ platform; avoid\n      redundant point-to-point connections.\n  - name: Accountability\n    description: Vendor side and Petco business-unit owner jointly own the integration.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/petco/refs/heads/main/finops/petco-finops.yml
sources:
- https://www.petco.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Retail
- Pet Care
---
