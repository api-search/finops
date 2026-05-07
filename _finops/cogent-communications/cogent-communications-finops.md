---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Cogent Communications: contract-based network services (Internet, Ethernet, Colocation, Wavelengths) priced via sales rather than public consumption-metered APIs.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Cogent Communications, Inc.
  ProviderName: Cogent Communications
  PublisherName: Cogent Communications, Inc.
  ServiceCategory: Networking
  ServiceName: Cogent Communications
layout: finops
meters:
- aggregation: sum
  dimensions:
  - port_speed
  - location
  name: dedicated_internet_access
  unit: month
- aggregation: max
  dimensions:
  - market
  - commit_tier
  name: ip_transit_bandwidth
  unit: Mbps
- aggregation: sum
  dimensions:
  - data_center
  name: colocation_space
  unit: rack-month
- aggregation: sum
  dimensions:
  - circuit_speed
  - route
  name: optical_wavelengths
  unit: month
name: Cogent Communications Finops
provider_name: Cogent Communications
provider_slug: cogent-communications
publisher_name: Cogent Communications, Inc.
service_category: Networking
slug: cogent-communications-finops
source_filename: cogent-communications-finops.yml
source_heading: FinOps Profile
source_url: https://www.cogentco.com/en/products-and-services
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cogent Communications\nproviderId: cogent-communications\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Internet\n  - Network\ndescription: 'FOCUS-aligned FinOps for Cogent Communications: contract-based network services (Internet,\n  Ethernet, Colocation, Wavelengths) priced via sales rather than public consumption-metered APIs.'\nsources:\n  - https://www.cogentco.com/en/products-and-services\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cogent Communications, Inc.\nserviceCategory: Networking\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    -\
  \ Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Cogent Communications\n  ServiceCategory: Networking\n  ProviderName: Cogent Communications\n  PublisherName: Cogent Communications, Inc.\n  InvoiceIssuerName: Cogent Communications, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: dedicated_internet_access\n    unit: month\n    aggregation: sum\n    dimensions:\n      - port_speed\n      - location\n  - name: ip_transit_bandwidth\n    unit: Mbps\n    aggregation: max\n    dimensions:\n      - market\n      - commit_tier\n  - name: colocation_space\n    unit: rack-month\n    aggregation: sum\n    dimensions:\n      - data_center\n  - name: optical_wavelengths\n    unit: month\n    aggregation: sum\n    dimensions:\n      - circuit_speed\n      - route\nprinciples:\n  - name: Visibility\n    description: Reconcile Cogent invoices against circuit IDs and port speeds; pull SNMP/utilization\n      data from edge routers to compare contracted bandwidth versus\
  \ consumed.\n  - name: Allocation\n    description: Tag each circuit/wavelength/colo footprint to the consuming business unit, site, or product.\n  - name: Optimization\n    description: Right-size committed bandwidth; consolidate wavelengths where utilization is low; renegotiate\n      multi-circuit contracts at renewal.\n  - name: Accountability\n    description: Network engineering owns circuit utilization; finance owns multi-year commitment decisions\n      and renewal dates.\nnotes: No public API/usage-meter pricing; meters above represent invoice-line abstractions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cogent-communications/refs/heads/main/finops/cogent-communications-finops.yml
sources:
- https://www.cogentco.com/en/products-and-services
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Internet
- Network
---
