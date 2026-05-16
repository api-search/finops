---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: reactor-api.yml
  format: yaml
  label: Adobe Launch Reactor API
  slug: adobe-launch-reactor-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-launch/refs/heads/main/openapi/reactor-api.yml
- filename: extension-api.yml
  format: yaml
  label: Adobe Launch Extension API
  slug: adobe-launch-extension-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-launch/refs/heads/main/openapi/extension-api.yml
- filename: event-forwarding-api.yml
  format: yaml
  label: Adobe Experience Platform Event Forwarding API
  slug: adobe-experience-platform-event-forwarding-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-launch/refs/heads/main/openapi/event-forwarding-api.yml
- filename: data-collection-api.yml
  format: yaml
  label: Adobe Experience Platform Data Collection API
  slug: adobe-experience-platform-data-collection-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-launch/refs/heads/main/openapi/data-collection-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Bundled
  chargeCategories:
  - Adjustment
  pricingCategory: Bundled (No Incremental Charge)
description: 'FOCUS-aligned FinOps shape for Adobe Launch / Experience Platform Tags: bundled with Experience Cloud product licenses; no incremental billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Adjustment
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Tag Management
  ServiceName: Adobe Experience Platform Tags
layout: finops
meters:
- aggregation: max
  description: Tag-management properties under management (operational, not billed)
  dimensions:
  - environment
  name: tag_properties
  unit: property
- aggregation: max
  description: Active tag-management rules (operational, not billed)
  dimensions:
  - property
  name: tag_rules
  unit: rule
- aggregation: avg
  description: Published tag-library payload size delivered to visitors
  dimensions:
  - property
  - environment
  name: library_size
  unit: KB
name: Adobe Launch Finops
provider_name: Adobe Launch
provider_slug: adobe-launch
publisher_name: Adobe Inc.
service_category: Tag Management
slug: adobe-launch-finops
source_filename: adobe-launch-finops.yml
source_heading: FinOps Profile
source_url: https://experienceleague.adobe.com/docs/experience-platform/tags/home.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe Launch\nproviderId: adobe-launch\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Tag Management\n  - Experience Platform\nnotes: >-\n  Adobe Launch / Experience Platform Tags is bundled with every Experience\n  Cloud product license at no incremental cost. There is no separate\n  invoice line; FinOps levers focus on operational hygiene (property\n  cleanup, library size) rather than cost optimization.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe Launch / Experience Platform Tags:\n  bundled with Experience Cloud product licenses; no incremental billing.\nsources:\n  - https://experienceleague.adobe.com/docs/experience-platform/tags/home.html\n  - https://developer.adobe.com/experience-platform-apis/references/reactor/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\nserviceCategory: Tag Management\nbillingModel:\n  pricingCategory: Bundled (No Incremental Charge)\n  billingFrequency: Bundled\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Adobe Experience Platform Tags\n  ServiceCategory: Tag Management\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\n  ChargeCategory: Adjustment\nmeters:\n  - name: tag_properties\n    description: Tag-management properties under management (operational, not billed)\n    unit: property\n    aggregation: max\n    dimensions:\n      - environment\n  - name: tag_rules\n    description: Active tag-management rules (operational, not billed)\n    unit: rule\n    aggregation: max\n    dimensions:\n      - property\n  - name: library_size\n    description: Published tag-library payload\
  \ size delivered to visitors\n    unit: KB\n    aggregation: avg\n    dimensions:\n      - property\n      - environment\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Tags UI and Reactor API to inventory all properties,\n      libraries, and rules; track library payload size to monitor\n      visitor-side performance impact.\n  - name: Allocation\n    description: >-\n      Group properties by brand / business unit; restrict Reactor API\n      credentials per team to attribute tag-management ownership.\n  - name: Optimization\n    description: >-\n      Reduce library payload size by removing unused extensions, rules,\n      and data elements; consolidate redundant analytics tags; use Edge\n      tags where possible to reduce client-side load.\n  - name: Accountability\n    description: >-\n      Marketing analytics or web platform team owns property hygiene and\n      change control; deprecation reviews quarterly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-launch/refs/heads/main/finops/adobe-launch-finops.yml
sources:
- https://experienceleague.adobe.com/docs/experience-platform/tags/home.html
- https://developer.adobe.com/experience-platform-apis/references/reactor/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Tag Management
- Experience Platform
---
