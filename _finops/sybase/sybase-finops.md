---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sybase-ase-rest-api-openapi.yml
  format: yaml
  label: Sybase ASE REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sybase/refs/heads/main/openapi/sybase-ase-rest-api-openapi.yml
- filename: openapi.json
  format: json
  label: Sybase IQ REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sybase.example.com/iq/v1/openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual or Term
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise License
description: Sybase (SAP ASE, SQL Anywhere, IQ, Replication Server) is sold under SAP enterprise licensing. This artifact captures publisher and category surface only; meters are placeholders pending an SAP price list. There is no public per-call API meter.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP
  PublisherName: SAP SE
  ServiceCategory: Enterprise Database
  ServiceName: Sybase
layout: finops
meters:
- aggregation: max
  description: SAP licensing metric used (core, CPU, named user, edition); cost realized through the customer's SAP order
  dimensions:
  - product_edition
  - license_type
  name: license_metric
  unit: varies
- aggregation: sum
  description: SAP Enterprise Support / maintenance attached to the underlying license
  dimensions:
  - product_edition
  name: maintenance_support
  unit: year
name: Sybase Finops
provider_name: Sybase
provider_slug: sybase
publisher_name: SAP SE
service_category: Enterprise Database
slug: sybase-finops
source_filename: sybase-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com/products/technology-platform/sybase-ase.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sybase\nproviderId: sybase\npublisherName: SAP SE\nserviceCategory: Enterprise Database\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Database\n  - Enterprise\n  - SAP\ndescription: Sybase (SAP ASE, SQL Anywhere, IQ, Replication Server) is sold under SAP enterprise licensing.\n  This artifact captures publisher and category surface only; meters are placeholders pending an SAP\n  price list. There is no public per-call API meter.\nsources:\n  - https://www.sap.com/products/technology-platform/sybase-ase.html\nnotes: 'Reconciliation marked false: SAP/Sybase pricing is not public; sold via SAP sales\
  \ and partner\n  network under enterprise license metrics (core, named user, term).'\nbillingModel:\n  pricingCategory: Enterprise License\n  billingFrequency: Annual or Term\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Sybase\n  ServiceCategory: Enterprise Database\n  ProviderName: SAP\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n  - name: license_metric\n    description: SAP licensing metric used (core, CPU, named user, edition); cost realized through\n      the customer's SAP order\n    unit: varies\n    aggregation: max\n    dimensions:\n      - product_edition\n      - license_type\n  - name: maintenance_support\n    description: SAP Enterprise Support / maintenance attached to the underlying license\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product_edition\nprinciples:\n  - name: Visibility\n    description: Visibility into Sybase spend is via\
  \ the SAP order schedule and SAP for Me account\n      view; database server consumption is tracked via the SAP-provided usage measurement tools (LAW,\n      USMM).\n  - name: Allocation\n    description: Allocate by SAP system ID and database; SAP licensing metrics tie directly to deployed\n      cores or named users per system.\n  - name: Optimization\n    description: Optimization levers are right-sizing cores, consolidating non-prod ASE/IQ instances,\n      moving from perpetual to subscription where the workload is contracting, and migrating cold workloads\n      to lower-cost editions.\n  - name: Accountability\n    description: Account ownership rests with the SAP Basis / database administration team and the\n      contract owner negotiating with SAP.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sybase/refs/heads/main/finops/sybase-finops.yml
sources:
- https://www.sap.com/products/technology-platform/sybase-ase.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Database
- Enterprise
- SAP
---
