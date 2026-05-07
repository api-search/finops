---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: juniper-networks-apstra-openapi.yml
  format: yaml
  label: Juniper Apstra API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-apstra-openapi.yml
- filename: juniper-networks-junos-telemetry-asyncapi.yml
  format: yaml
  label: Junos XML API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/asyncapi/juniper-networks-junos-telemetry-asyncapi.yml
- filename: juniper-networks-mist-openapi.yml
  format: yaml
  label: Juniper Mist API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-mist-openapi.yml
- filename: juniper-networks-contrail-openapi.yml
  format: yaml
  label: Juniper Contrail API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-contrail-openapi.yml
- filename: juniper-networks-junos-space-openapi.yml
  format: yaml
  label: Junos Space REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-junos-space-openapi.yml
- filename: juniper-networks-vsrx-openapi.yml
  format: yaml
  label: Juniper vSRX REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/openapi/juniper-networks-vsrx-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription / License
description: FOCUS-aligned FinOps scaffold for Juniper Networks product APIs. Treated as subscription / license-bundled access; meters reflect product-line entitlements.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Juniper Networks, Inc.
  ProviderName: Juniper Networks
  PublisherName: Juniper Networks, Inc.
  ServiceCategory: Networking / SDN / Security
  ServiceName: Juniper Networks Product APIs
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - site
  - org
  name: managed_devices
  unit: device
- aggregation: max
  dimensions:
  - site
  - org
  name: managed_aps
  unit: access_point
- aggregation: sum
  dimensions:
  - product
  - org
  name: api_requests
  unit: request
name: Juniper Networks Finops
provider_name: Juniper Networks
provider_slug: juniper-networks
publisher_name: Juniper Networks, Inc.
service_category: Networking / SDN / Security
slug: juniper-networks-finops
source_filename: juniper-networks-finops.yml
source_heading: FinOps Profile
source_url: https://www.juniper.net/us/en/dm/api-catalog.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Juniper Networks\nproviderId: juniper-networks\npublisherName: Juniper Networks, Inc.\nserviceCategory: Networking / SDN / Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Juniper does not expose a per-call usage-billing surface; APIs are entitlements of\n  product subscriptions. FinOps shape inferred from a subscription / license model. Meters\n  reflect typical infrastructure-management billable units (devices, sites, APs).\ntags:\n  - Automation\n  - Cloud\n  - Data Center\n  - Enterprise\n  - Networking\n  - SDN\n  - Security\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Juniper Networks\
  \ product APIs. Treated as\n  subscription / license-bundled access; meters reflect product-line entitlements.\nsources:\n  - https://www.juniper.net/us/en/dm/api-catalog.html\n  - https://www.finops.org/framework/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription / License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Juniper Networks Product APIs\n  ServiceCategory: Networking / SDN / Security\n  ProviderName: Juniper Networks\n  PublisherName: Juniper Networks, Inc.\n  InvoiceIssuerName: Juniper Networks, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: managed_devices\n    unit: device\n    aggregation: max\n    dimensions:\n      - product\n      - site\n      - org\n  - name: managed_aps\n    unit: access_point\n    aggregation: max\n    dimensions:\n      - site\n      - org\n  - name: api_requests\n    unit: request\n   \
  \ aggregation: sum\n    dimensions:\n      - product\n      - org\nprinciples:\n  - name: Visibility\n    description: Track managed-device and AP counts in Mist / Apstra dashboards; reconcile\n      against renewal entitlements.\n  - name: Allocation\n    description: Allocate by site / org_id since most Juniper subscriptions are scoped to\n      organizations and locations.\n  - name: Optimization\n    description: Right-size license tiers (e.g. Mist Wi-Fi Assurance vs Premium Analytics)\n      against the API features your automation actually uses.\n  - name: Accountability\n    description: Network operations team typically owns Juniper spend; pair with the partner /\n      reseller account team for renewal cycles.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/juniper-networks/refs/heads/main/finops/juniper-networks-finops.yml
sources:
- https://www.juniper.net/us/en/dm/api-catalog.html
- https://www.finops.org/framework/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Automation
- Cloud
- Data Center
- Enterprise
- Networking
- SDN
- Security
- FinOps
- FOCUS
---
