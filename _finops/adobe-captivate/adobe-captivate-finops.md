---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.json
  format: json
  label: Adobe Captivate Prime API
  slug: ''
  spec_type: OpenAPI
  url: https://learningmanager.adobe.com/primeapi/v2/swagger.json
- filename: adobe-captivate-learning-manager-webhooks-asyncapi.yml
  format: yaml
  label: Adobe Learning Manager Webhooks API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-captivate/refs/heads/main/asyncapi/adobe-captivate-learning-manager-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Purchase
  - Tax
  - Refund
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps shape for Adobe Captivate: simple per-seat monthly or annual subscription managed via the Adobe Admin Console.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: eLearning Authoring
  ServiceName: Adobe Captivate
layout: finops
meters:
- aggregation: sum
  description: Per-seat monthly Captivate subscription
  dimensions:
  - sku
  - geography
  name: captivate_seat
  unit: seat-month
name: Adobe Captivate Finops
provider_name: Adobe Captivate
provider_slug: adobe-captivate
publisher_name: Adobe Inc.
service_category: eLearning Authoring
slug: adobe-captivate-finops
source_filename: adobe-captivate-finops.yml
source_heading: FinOps Profile
source_url: https://www.adobe.com/products/captivate.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Captivate\nproviderId: adobe-captivate\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - eLearning\n  - Authoring\nnotes: >-\n  Adobe Captivate is per-seat SaaS without on-demand metering. FinOps levers\n  are seat hygiene (reclaim unused seats) and right-sizing between\n  individual, teams, and education SKUs. Public list pricing was not\n  retrievable via WebFetch.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe Captivate: simple per-seat monthly\n  or annual subscription managed via the Adobe Admin Console.\nsources:\n  - https://www.adobe.com/products/captivate.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Adobe Inc.\nserviceCategory: eLearning Authoring\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Refund\nfocusColumns:\n  ServiceName: Adobe Captivate\n  ServiceCategory: eLearning Authoring\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: captivate_seat\n    description: Per-seat monthly Captivate subscription\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - sku\n      - geography\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Adobe Admin Console seat assignment report to see active\n      Captivate users per organisation.\n  - name: Allocation\n    description: >-\n      Tag seats with department / cost-center metadata in the Admin Console\n      so seat cost can be allocated to consuming teams.\n  - name: Optimization\n\
  \    description: >-\n      Reclaim seats from inactive authors quarterly; consider Education /\n      Government SKUs where eligible; bundle Captivate with Creative Cloud\n      All Apps where the same author also needs Photoshop / Illustrator.\n  - name: Accountability\n    description: >-\n      L&D / training-team owner is accountable for active seat count;\n      finance reviews annual renewal against actual usage.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-captivate/refs/heads/main/finops/adobe-captivate-finops.yml
sources:
- https://www.adobe.com/products/captivate.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- eLearning
- Authoring
---
