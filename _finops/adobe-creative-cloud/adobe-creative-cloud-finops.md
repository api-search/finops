---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-firefly-api-openapi-original.yml
  format: yaml
  label: Adobe Firefly API
  slug: firefly-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/openapi/adobe-firefly-api-openapi-original.yml
- filename: adobe-cc-libraries-api-openapi-original.yml
  format: yaml
  label: Creative Cloud Libraries API
  slug: cc-libraries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/openapi/adobe-cc-libraries-api-openapi-original.yml
- filename: adobe-stock-api-openapi-original.yml
  format: yaml
  label: Adobe Stock API
  slug: stock-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/openapi/adobe-stock-api-openapi-original.yml
- filename: adobe-pdf-services-api-openapi-original.yml
  format: yaml
  label: Adobe PDF Services API
  slug: pdf-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/openapi/adobe-pdf-services-api-openapi-original.yml
- filename: adobe-io-events-asyncapi-original.yml
  format: yaml
  label: Adobe I/O Events
  slug: io-events
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/asyncapi/adobe-io-events-asyncapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Refund
  - Adjustment
  pricingCategory: Subscription + Generative Credits
description: 'FOCUS-aligned FinOps shape for Adobe Creative Cloud: per-seat monthly / annual subscription plus generative-credit metering for Firefly features.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Creative SaaS
  ServiceName: Adobe Creative Cloud
layout: finops
meters:
- aggregation: sum
  description: Per-seat Creative Cloud subscription
  dimensions:
  - plan
  - geography
  name: cc_seat
  unit: seat-month
- aggregation: max
  description: Cloud storage consumed per seat (included; tracked for capacity)
  dimensions:
  - seat
  name: cloud_storage
  unit: GB-month
- aggregation: sum
  description: Firefly generative-credit consumption inside Creative Cloud apps
  dimensions:
  - app
  - feature
  name: generative_credits
  unit: credit
name: Adobe Creative Cloud Finops
provider_name: Adobe Creative Cloud
provider_slug: adobe-creative-cloud
publisher_name: Adobe Inc.
service_category: Creative SaaS
slug: adobe-creative-cloud-finops
source_filename: adobe-creative-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://www.adobe.com/plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Creative Cloud\nproviderId: adobe-creative-cloud\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Creative Cloud\n  - Generative AI\nnotes: >-\n  Creative Cloud is per-seat SaaS with a generative-credit usage component\n  for Firefly. Public list prices were not retrievable via WebFetch.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe Creative Cloud: per-seat monthly /\n  annual subscription plus generative-credit metering for Firefly features.\nsources:\n  - https://www.adobe.com/plans\n  - https://www.adobe.com/creativecloud/business/teams/plans.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\n\
  serviceCategory: Creative SaaS\nbillingModel:\n  pricingCategory: Subscription + Generative Credits\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: Adobe Creative Cloud\n  ServiceCategory: Creative SaaS\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\nmeters:\n  - name: cc_seat\n    description: Per-seat Creative Cloud subscription\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - plan\n      - geography\n  - name: cloud_storage\n    description: Cloud storage consumed per seat (included; tracked for capacity)\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - seat\n  - name: generative_credits\n    description: Firefly generative-credit consumption inside Creative Cloud apps\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - app\n      -\
  \ feature\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Adobe Admin Console for seat assignment and usage reports;\n      monitor generative-credit balance per seat to spot run-out before\n      end of month.\n  - name: Allocation\n    description: >-\n      Tag seats with department / cost-center metadata in the Admin Console;\n      attribute generative-credit burn to consuming teams via Firefly\n      Services audit logs.\n  - name: Optimization\n    description: >-\n      Right-size between Single App and All Apps based on actual usage;\n      reclaim seats from inactive users; reserve high-credit Firefly calls\n      for final renders; use Adobe Express for lower-cost designers.\n  - name: Accountability\n    description: >-\n      Adobe Admin Console designates a billing contact and seat administrators;\n      finance reconciles monthly seat count against the renewal commitment.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/finops/adobe-creative-cloud-finops.yml
sources:
- https://www.adobe.com/plans
- https://www.adobe.com/creativecloud/business/teams/plans.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Creative Cloud
- Generative AI
---
