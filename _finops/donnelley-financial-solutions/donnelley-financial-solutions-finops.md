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
  - Tax
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps shape for DFIN. Billing is enterprise contract per product (ActiveDisclosure, Venue, Arc Suite); per-API-call pricing is not published.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Donnelley Financial Solutions, LLC
  ProviderName: Donnelley Financial Solutions
  PublisherName: Donnelley Financial Solutions, LLC
  ServiceCategory: Financial Regulatory / Compliance Software
  ServiceName: DFIN ActiveDisclosure / Venue / Arc Suite
layout: finops
meters:
- aggregation: count
  description: Active named users under the DFIN contract
  dimensions:
  - product
  name: contract_seats
  unit: seat
- aggregation: count
  description: SEC filings or disclosure documents processed
  dimensions:
  - product
  - filing_type
  name: filings
  unit: document
- aggregation: avg
  description: Storage consumed by Venue data rooms
  dimensions:
  - data_room
  name: data_room_storage
  unit: GB-month
name: Donnelley Financial Solutions Finops
provider_name: Donnelley Financial Solutions
provider_slug: donnelley-financial-solutions
publisher_name: Donnelley Financial Solutions, LLC
service_category: Financial Regulatory / Compliance Software
slug: donnelley-financial-solutions-finops
source_filename: donnelley-financial-solutions-finops.yml
source_heading: FinOps Profile
source_url: https://www.dfinsolutions.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Donnelley Financial Solutions\nproviderId: donnelley-financial-solutions\npublisherName: Donnelley Financial Solutions, LLC\nserviceCategory: Financial Regulatory / Compliance Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial\n  - Regulatory Compliance\n  - Software\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for DFIN. Billing is enterprise contract per product (ActiveDisclosure,\n  Venue, Arc Suite); per-API-call pricing is not published.\nnotes: No public per-meter billing; reconciled=false.\nsources:\n  - https://www.dfinsolutions.com/\n  - https://www.dfinsolutions.com/about\n\
  billingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: DFIN ActiveDisclosure / Venue / Arc Suite\n  ServiceCategory: Financial Regulatory / Compliance Software\n  ProviderName: Donnelley Financial Solutions\n  PublisherName: Donnelley Financial Solutions, LLC\n  InvoiceIssuerName: Donnelley Financial Solutions, LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_seats\n    description: Active named users under the DFIN contract\n    unit: seat\n    aggregation: count\n    dimensions:\n      - product\n  - name: filings\n    description: SEC filings or disclosure documents processed\n    unit: document\n    aggregation: count\n    dimensions:\n      - product\n      - filing_type\n  - name: data_room_storage\n    description: Storage consumed by Venue data rooms\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n\
  \      - data_room\nprinciples:\n  - name: Visibility\n    description: Reconcile the DFIN enterprise invoice against contracted seats, filings, and Venue data-room\n      storage; per-API-call usage is not invoiced.\n  - name: Allocation\n    description: Allocate DFIN cost to the legal/compliance team or deal team owning the SEC filing or\n      M&A data room.\n  - name: Optimization\n    description: Right-size data-room scope; archive completed deal rooms; reuse ActiveDisclosure templates\n      across recurring filings.\n  - name: Accountability\n    description: Compliance / corporate-secretary function owns DFIN spend and contract renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/donnelley-financial-solutions/refs/heads/main/finops/donnelley-financial-solutions-finops.yml
sources:
- https://www.dfinsolutions.com/
- https://www.dfinsolutions.com/about
specification: FinOps Framework
tags:
- Financial
- Regulatory Compliance
- Software
- FinOps
- FOCUS
---
