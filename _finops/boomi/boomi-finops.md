---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: OpenAPI_3_0
  format: yaml
  label: Boomi Platform REST API
  slug: platform-rest-api
  spec_type: OpenAPI
  url: https://developer.boomi.com/docs/APIs/PlatformAPI/Introduction/OpenAPI_3_0
- filename: OpenAPI_3_0
  format: yaml
  label: Boomi Platform Partner API
  slug: platform-partner-api
  spec_type: OpenAPI
  url: https://developer.boomi.com/docs/APIs/PlatformAPI/Introduction/OpenAPI_3_0
- filename: boomi-datahub-api-openapi.yml
  format: yaml
  label: Boomi DataHub API
  slug: datahub-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boomi/refs/heads/main/openapi/boomi-datahub-api-openapi.yml
- filename: boomi-event-streams-openapi.yml
  format: yaml
  label: Boomi Event Streams REST API
  slug: event-streams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boomi/refs/heads/main/openapi/boomi-event-streams-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Boomi: tiered subscription editions across Integration, API Management, Data Hub, and Data Integration product lines, with a Pay-as-you-Go option ($99/month plus usage) and contact-sales pricing for upper tiers.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Boomi, LP
  PricingCategory: Standard
  PricingUnit: subscription-month
  ProviderName: Boomi
  PublisherName: Boomi, LP
  ServiceCategory: Integration Platform
  ServiceName: Boomi
layout: finops
meters:
- aggregation: sum
  description: Edition subscription fee billed monthly per account.
  dimensions:
  - product_line
  - edition
  name: subscription_month
  unit: month
- aggregation: max
  description: Number of provisioned source/target connections; connection count gates upgrades between editions.
  dimensions:
  - product_line
  - connection_type
  name: connections
  unit: connection
- aggregation: max
  description: Atom / molecule runtime environments deployed against the account.
  dimensions:
  - environment_type
  - region
  name: runtime_environments
  unit: environment
- aggregation: sum
  description: API calls flowing through Boomi API Management gateway.
  dimensions:
  - api
  - contract
  - environment
  name: api_management_calls
  unit: request
- aggregation: sum
  description: Managed File Transfer events processed under the MFT product line.
  dimensions:
  - direction
  - partner
  name: mft_transfers
  unit: transfer
- aggregation: max
  description: Records mastered / synchronized through Boomi Data Hub.
  dimensions:
  - domain
  name: data_hub_records
  unit: record
- aggregation: sum
  description: Usage component metered on top of the $99/month Pay-as-you-Go platform fee.
  dimensions:
  - service
  name: pay_as_you_go_usage
  unit: varies
name: Boomi Finops
provider_name: Boomi
provider_slug: boomi
publisher_name: Boomi, LP
service_category: Integration Platform (iPaaS)
slug: boomi-finops
source_filename: boomi-finops.yml
source_heading: FinOps Profile
source_url: https://boomi.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Boomi\nproviderId: boomi\npublisherName: Boomi, LP\nserviceCategory: Integration Platform (iPaaS)\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI Agents\n  - Automation\n  - B2B\n  - Data Integration\n  - EDI\n  - Integrations\n  - Management\n  - MFT\n  - Platform\n  - Workflows\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Boomi: tiered subscription editions across Integration, API Management,\n  Data Hub, and Data Integration product lines, with a Pay-as-you-Go option ($99/month plus usage) and\n  contact-sales pricing for upper tiers.'\nsources:\n  - https://boomi.com/pricing/\n  - https://help.boomi.com/\n\
  billingModel:\n  pricingCategory: Tiered Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Boomi\n  ServiceCategory: Integration Platform\n  ProviderName: Boomi\n  PublisherName: Boomi, LP\n  InvoiceIssuerName: Boomi, LP\n  BillingCurrency: USD\n  PricingCategory: Standard\n  PricingUnit: subscription-month\nmeters:\n  - name: subscription_month\n    description: Edition subscription fee billed monthly per account.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product_line\n      - edition\n  - name: connections\n    description: Number of provisioned source/target connections; connection count gates upgrades between\n      editions.\n    unit: connection\n    aggregation: max\n    dimensions:\n      - product_line\n      - connection_type\n  - name: runtime_environments\n    description: Atom / molecule runtime environments\
  \ deployed against the account.\n    unit: environment\n    aggregation: max\n    dimensions:\n      - environment_type\n      - region\n  - name: api_management_calls\n    description: API calls flowing through Boomi API Management gateway.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - contract\n      - environment\n  - name: mft_transfers\n    description: Managed File Transfer events processed under the MFT product line.\n    unit: transfer\n    aggregation: sum\n    dimensions:\n      - direction\n      - partner\n  - name: data_hub_records\n    description: Records mastered / synchronized through Boomi Data Hub.\n    unit: record\n    aggregation: max\n    dimensions:\n      - domain\n  - name: pay_as_you_go_usage\n    description: Usage component metered on top of the $99/month Pay-as-you-Go platform fee.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Pull invoices and\
  \ platform usage exports from the Boomi AtomSphere admin console; track\n      connection count, runtime hours, and API Management call volume against the contracted edition's\n      ceilings.\n  - name: Allocation\n    description: Tag processes, APIs, and connections by business unit and environment so platform fees\n      and gateway calls allocate cleanly to consuming products.\n  - name: Optimization\n    description: Right-size the edition to the actual connection / process count, retire unused integrations,\n      consolidate runtimes where high availability is not required, and apply gateway-level throttling\n      to control downstream cost.\n  - name: Accountability\n    description: Designate an integration / API platform owner per business unit; review monthly invoices\n      and renewal posture against process and API growth, and use Premier / Premier Plus support tiers\n      where uptime tolerance is low.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/boomi/refs/heads/main/finops/boomi-finops.yml
sources:
- https://boomi.com/pricing/
- https://help.boomi.com/
specification: FinOps Framework
tags:
- AI Agents
- Automation
- B2B
- Data Integration
- EDI
- Integrations
- Management
- MFT
- Platform
- Workflows
- FinOps
- FOCUS
---
