---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stanley-black-and-decker-tool-connect-api-openapi.yml
  format: yaml
  label: DEWALT Tool Connect API
  slug: dewalt-tool-connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stanley-black-and-decker/refs/heads/main/openapi/stanley-black-and-decker-tool-connect-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: Stanley Black & Decker's connected-tool APIs (DEWALT Tool Connect, Stanley X IoT) are partner-only and not publicly priced. End customers pay a Tool Connect subscription per fleet plus possible third-party data charges. FinOps shape is partner-contract-driven; no public meter or unit price exists to model concretely.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Stanley Black & Decker, Inc.
  ProviderName: Stanley Black & Decker
  PublisherName: Stanley Black & Decker, Inc.
  ServiceCategory: IoT / Connected Hardware
  ServiceName: DEWALT Tool Connect
layout: finops
meters:
- aggregation: sum
  dimensions:
  - fleet
  - region
  name: tool_connect_subscription
  unit: month
name: Stanley Black And Decker Finops
provider_name: Stanley Black & Decker
provider_slug: stanley-black-and-decker
publisher_name: Stanley Black & Decker, Inc.
service_category: IoT / Connected Hardware
slug: stanley-black-and-decker-finops
source_filename: stanley-black-and-decker-finops.yml
source_heading: FinOps Profile
source_url: https://www.dewalt.com/systems/tool-connect
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Stanley Black & Decker\nproviderId: stanley-black-and-decker\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Tools\n  - Hardware\n  - IoT\n  - Connected Tools\n  - FinOps\n  - FOCUS\ndescription: Stanley Black & Decker's connected-tool APIs (DEWALT Tool Connect, Stanley X IoT) are partner-only and not publicly priced. End customers pay a Tool Connect subscription per fleet plus possible third-party data charges. FinOps shape is partner-contract-driven; no public meter or unit price exists to model concretely.\nsources:\n  - https://www.dewalt.com/systems/tool-connect\nnotes: B2B / partner-only. No public price list, no public meter definitions. FOCUS columns and meter set are placeholders pending partner contract terms.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Stanley Black & Decker, Inc.\nserviceCategory: IoT / Connected Hardware\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: DEWALT Tool Connect\n  ServiceCategory: IoT / Connected Hardware\n  ProviderName: Stanley Black & Decker\n  PublisherName: Stanley Black & Decker, Inc.\n  InvoiceIssuerName: Stanley Black & Decker, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tool_connect_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - fleet\n      - region\nprinciples:\n  - name: Visibility\n    description: End-customer fleet managers see consumption in the DEWALT Site Manager dashboard. API partners surface tool inventory and asset-tracking events through the Tool Connect API; cost visibility for the underlying subscription is on the\
  \ customer's invoice from Stanley Black & Decker.\n  - name: Allocation\n    description: Allocate Tool Connect subscription cost to the fleet / jobsite that owns the connected tools. Tag tools at registration with site, project, and crew so consumption rolls up to the right cost center.\n  - name: Optimization\n    description: Right-size the connected-tool fleet to active jobsites, retire stale assignments, and consolidate Tool Connect subscriptions across business units where the licensing model permits. Renegotiate partner API access at renewal as integration volume grows.\n  - name: Accountability\n    description: Construction / fleet operations team owns the Tool Connect subscription; integration partners own their API consumption budget under their partner agreement.\nmaintainers:\n  - name: Stanley Black & Decker\n    url: https://www.stanleyblackanddecker.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stanley-black-and-decker/refs/heads/main/finops/stanley-black-and-decker-finops.yml
sources:
- https://www.dewalt.com/systems/tool-connect
specification: FinOps Framework
tags:
- Tools
- Hardware
- IoT
- Connected Tools
- FinOps
- FOCUS
---
