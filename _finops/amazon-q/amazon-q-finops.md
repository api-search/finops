---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-q-business.json
  format: json
  label: Amazon Q Business API
  slug: amazon-q-business-api
  spec_type: OpenAPI
  url: https://example.com/openapi/amazon-q-business.json
- filename: amazon-q-developer.json
  format: json
  label: Amazon Q Developer API
  slug: amazon-q-developer-api
  spec_type: OpenAPI
  url: https://example.com/openapi/amazon-q-developer.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Amazon Q: per-user/month subscriptions for Q Business and Q Developer, hourly Index unit charges, per-media-unit ingestion fees, and consumption-unit pricing for anonymous/embedded use cases.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: AI and Machine Learning
  ServiceName: Amazon Q
  ServiceSubcategory: Generative AI Assistant
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - tier
  - application
  name: q_business_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - tier
  - identity_center_instance
  name: q_developer_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - region
  - application
  - index_type
  name: index_unit_hours
  unit: index-unit-hour
- aggregation: sum
  dimensions:
  - media_type
  - application
  name: media_processing
  unit: varies
- aggregation: sum
  dimensions:
  - language
  - account
  name: code_transformation_lines
  unit: line-of-code
- aggregation: sum
  dimensions:
  - application
  - region
  name: consumption_units
  unit: consumption-unit
name: Amazon Q Finops
provider_name: Amazon Q
provider_slug: amazon-q
publisher_name: Amazon Web Services, Inc.
service_category: AI / Assistant
slug: amazon-q-finops
source_filename: amazon-q-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/q/business/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon Q\nproviderId: amazon-q\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - GenAI\n  - Amazon Q\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon Q: per-user/month subscriptions for Q Business and Q Developer,\n  hourly Index unit charges, per-media-unit ingestion fees, and consumption-unit pricing for anonymous/embedded\n  use cases.'\nsources:\n  - https://aws.amazon.com/q/business/pricing/\n  - https://aws.amazon.com/q/developer/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: AI / Assistant\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Amazon Q\n  ServiceCategory: AI and Machine Learning\n  ServiceSubcategory: Generative AI Assistant\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: q_business_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - region\n      - tier\n      - application\n  - name: q_developer_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tier\n      - identity_center_instance\n  - name: index_unit_hours\n    unit: index-unit-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - application\n      - index_type\n  - name: media_processing\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - media_type\n      - application\n\
  \  - name: code_transformation_lines\n    unit: line-of-code\n    aggregation: sum\n    dimensions:\n      - language\n      - account\n  - name: consumption_units\n    unit: consumption-unit\n    aggregation: sum\n    dimensions:\n      - application\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the AWS Billing console, Cost Explorer with the Amazon Q service filter, and CUR /\n      FOCUS export to see per-user, per-application, per-index spend.\n  - name: Allocation\n    description: Tag Q Business applications and Identity Center groups; map cost-center attributes via\n      cost allocation tags so the Q line items roll up to the right team.\n  - name: Optimization\n    description: Right-size index units (Starter for dev, Enterprise for prod), retire unused user assignments,\n      use Lite tier for low-touch users, and watch the 4,000 LOC pooled transformation budget on Q Developer\n      Pro.\n  - name: Accountability\n    description: Set AWS Budgets\
  \ per Q application/tag and alert on month-over-month seat or index growth;\n      review trial overage closely after the 60-day window.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Amazon Web Services\n    email: support@aws.amazon.com\n    url: https://aws.amazon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-q/refs/heads/main/finops/amazon-q-finops.yml
sources:
- https://aws.amazon.com/q/business/pricing/
- https://aws.amazon.com/q/developer/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- GenAI
- Amazon Q
- Cost Management
---
