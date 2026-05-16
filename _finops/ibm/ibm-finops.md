---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: assistant-v2.json
  format: json
  label: IBM Watson Assistant
  slug: ibm-watson-assistant
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/assistant/assistant-v2.json
- filename: natural-language-understanding.json
  format: json
  label: IBM Watson Natural Language Understanding
  slug: ibm-watson-natural-language-understanding
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/natural-language-understanding/natural-language-understanding.json
- filename: language-translator.json
  format: json
  label: IBM Watson Language Translator
  slug: ibm-watson-language-translator
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/language-translator/language-translator.json
- filename: speech-to-text.json
  format: json
  label: IBM Watson Speech to Text
  slug: ibm-watson-speech-to-text
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/speech-to-text/speech-to-text.json
- filename: text-to-speech.json
  format: json
  label: IBM Watson Text to Speech
  slug: ibm-watson-text-to-speech
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/text-to-speech/text-to-speech.json
- filename: ibm-cloud-iam.yml
  format: yaml
  label: IBM Cloud IAM Identity Services
  slug: ibm-cloud-iam-identity-services
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ibm/refs/heads/main/openapi/ibm-cloud-iam.yml
- filename: ibm-cloud-iam.yml
  format: yaml
  label: IBM IAM Policy Management
  slug: ibm-iam-policy-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ibm/refs/heads/main/openapi/ibm-cloud-iam.yml
- filename: ibm-cloud-iam.yml
  format: yaml
  label: IBM IAM Access Groups
  slug: ibm-iam-access-groups
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ibm/refs/heads/main/openapi/ibm-cloud-iam.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for IBM (Cloud + Watsonx + Software).
focus_columns:
  BillingCurrency: USD
  ProviderName: IBM (Cloud + Watsonx + Software)
  PublisherName: IBM (Cloud + Watsonx + Software)
  ServiceCategory: Cloud + AI + Enterprise Software
  ServiceName: IBM (Cloud + Watsonx + Software)
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - region
  - instance_type
  - tenant
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - service
  - tier
  name: storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - egress_type
  - region_pair
  name: data_transfer
  unit: GB
- aggregation: sum
  dimensions:
  - service
  - operation
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - service
  name: managed_services
  unit: varies
name: Ibm Finops
provider_name: IBM
provider_slug: ibm
publisher_name: IBM (Cloud + Watsonx + Software)
service_category: Cloud + AI + Enterprise Software
slug: ibm-finops
source_filename: ibm-finops.yml
source_heading: FinOps Profile
source_url: https://www.ibm.com/cloud/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: IBM (Cloud + Watsonx + Software)\nproviderId: ibm\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud + AI + Enterprise Software\ndescription: FOCUS-aligned FinOps for IBM (Cloud + Watsonx + Software).\nsources:\n  - https://www.ibm.com/cloud/pricing\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: IBM (Cloud + Watsonx + Software)\nserviceCategory: Cloud + AI + Enterprise Software\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: IBM (Cloud + Watsonx + Software)\n  ServiceCategory: Cloud + AI + Enterprise\
  \ Software\n  ProviderName: IBM (Cloud + Watsonx + Software)\n  PublisherName: IBM (Cloud + Watsonx + Software)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track IBM (Cloud + Watsonx + Software) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size;\
  \ reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ibm/refs/heads/main/finops/ibm-finops.yml
sources:
- https://www.ibm.com/cloud/pricing
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud + AI + Enterprise Software
---
