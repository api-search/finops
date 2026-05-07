---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for Jazz Pharmaceuticals: a neuroscience-focused biopharma with no public API or rate card. FinOps applies primarily to internal cloud and validated-system spend.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Jazz Pharmaceuticals plc
  ProviderName: Jazz Pharmaceuticals
  PublisherName: Jazz Pharmaceuticals plc
  ServiceCategory: Biopharmaceuticals
  ServiceName: Jazz Pharmaceuticals
layout: finops
meters:
- aggregation: sum
  dimensions:
  - partner
  - integration_type
  name: integration_subscription
  unit: month
- aggregation: sum
  dimensions:
  - study
  name: clinical_data_volume
  unit: GB
name: Jazz Pharmaceuticals Finops
provider_name: Jazz Pharmaceuticals
provider_slug: jazz-pharmaceuticals
publisher_name: Jazz Pharmaceuticals plc
service_category: Biopharmaceuticals
slug: jazz-pharmaceuticals-finops
source_filename: jazz-pharmaceuticals-finops.yml
source_heading: FinOps Profile
source_url: https://www.jazzpharma.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Jazz Pharmaceuticals\nproviderId: jazz-pharmaceuticals\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Pharmaceuticals\n  - Neuroscience\ndescription: 'FOCUS-aligned FinOps placeholder for Jazz Pharmaceuticals: a neuroscience-focused biopharma\n  with no public API or rate card. FinOps applies primarily to internal cloud and validated-system spend.'\nnotes: Jazz does not publish an API rate card. Meters below model the typical partner / clinical-system\n  integration surface; cannot be reconciled without a customer contract.\nsources:\n  - https://www.jazzpharma.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Jazz Pharmaceuticals\
  \ plc\nserviceCategory: Biopharmaceuticals\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Jazz Pharmaceuticals\n  ServiceCategory: Biopharmaceuticals\n  ProviderName: Jazz Pharmaceuticals\n  PublisherName: Jazz Pharmaceuticals plc\n  InvoiceIssuerName: Jazz Pharmaceuticals plc\n  BillingCurrency: USD\nmeters:\n  - name: integration_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - partner\n      - integration_type\n  - name: clinical_data_volume\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - study\nprinciples:\n  - name: Visibility\n    description: Track partner integration invoices and validated-system cloud spend against study\n      and program codes; no public Jazz usage API.\n  - name: Allocation\n    description: Allocate integration cost to the clinical / commercial program driving the data exchange.\n\
  \  - name: Optimization\n    description: Consolidate partner platforms; reuse validated environments across studies where compliance\n      allows.\n  - name: Accountability\n    description: Clinical operations + IT jointly own integration spend; quarterly review against study\n      budgets.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jazz-pharmaceuticals/refs/heads/main/finops/jazz-pharmaceuticals-finops.yml
sources:
- https://www.jazzpharma.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Pharmaceuticals
- Neuroscience
---
