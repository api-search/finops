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
  pricingCategory: Not Applicable (No Public API)
description: FOCUS-aligned FinOps shape for Ducommun trading-partner integrations. Ducommun does not invoice for API consumption; the billable transactions are physical orders / shipments under the customer or supplier master agreement.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Not Applicable
  ProviderName: Ducommun
  PublisherName: Ducommun Incorporated
  ServiceCategory: Aerospace & Defense Manufacturing
  ServiceName: Ducommun (B2B Integration)
layout: finops
meters:
- aggregation: count
  description: EDI documents exchanged with Ducommun (PO / ASN / invoice)
  dimensions:
  - document_type
  - direction
  name: edi_documents
  unit: document
- aggregation: count
  description: Physical orders / shipments billed under the master agreement
  dimensions:
  - program
  name: orders
  unit: order
name: Ducommun Finops
provider_name: Ducommun
provider_slug: ducommun
publisher_name: Ducommun Incorporated
service_category: Aerospace & Defense Manufacturing
slug: ducommun-finops
source_filename: ducommun-finops.yml
source_heading: FinOps Profile
source_url: https://www.ducommun.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ducommun\nproviderId: ducommun\npublisherName: Ducommun Incorporated\nserviceCategory: Aerospace & Defense Manufacturing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Aerospace\n  - Defense\n  - Manufacturing\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Ducommun trading-partner integrations. Ducommun does not\n  invoice for API consumption; the billable transactions are physical orders / shipments under the customer\n  or supplier master agreement.\nnotes: No public API or invoiced API consumption; reconciled=false.\nsources:\n  - https://www.ducommun.com/\nbillingModel:\n  pricingCategory: Not\
  \ Applicable (No Public API)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Ducommun (B2B Integration)\n  ServiceCategory: Aerospace & Defense Manufacturing\n  ProviderName: Ducommun\n  PublisherName: Ducommun Incorporated\n  InvoiceIssuerName: Not Applicable\n  BillingCurrency: USD\nmeters:\n  - name: edi_documents\n    description: EDI documents exchanged with Ducommun (PO / ASN / invoice)\n    unit: document\n    aggregation: count\n    dimensions:\n      - document_type\n      - direction\n  - name: orders\n    description: Physical orders / shipments billed under the master agreement\n    unit: order\n    aggregation: count\n    dimensions:\n      - program\nprinciples:\n  - name: Visibility\n    description: Track EDI/PLM volumes in the consumer's integration platform; physical billing flows\n      through the customer/supplier master agreement, not an API meter.\n  - name: Allocation\n    description: Allocate integration\
  \ cost to the aerospace or defense program owning the trading-partner\n      relationship.\n  - name: Optimization\n    description: Use ASN automation; minimise manual portal sessions; consolidate EDI flows where the\n      master agreement permits.\n  - name: Accountability\n    description: Procurement / customer-relations owner is accountable for the master agreement and integration\n      uptime; ITAR/EAR compliance owner reviews exchanges.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ducommun/refs/heads/main/finops/ducommun-finops.yml
sources:
- https://www.ducommun.com/
specification: FinOps Framework
tags:
- Aerospace
- Defense
- Manufacturing
- FinOps
- FOCUS
---
