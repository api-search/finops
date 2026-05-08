---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lumen-internet-on-demand-api-openapi.yml
  format: yaml
  label: Lumen Internet On-Demand API
  slug: internet-on-demand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lumen-technologies/refs/heads/main/openapi/lumen-internet-on-demand-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: 'FOCUS-aligned FinOps for Lumen Technologies: enterprise contract-based network services (fiber, IP, Internet On-Demand, edge cloud, managed security). APIs themselves are not separately metered — they orchestrate underlying chargeable network services.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Lumen Technologies, Inc.
  ProviderName: Lumen Technologies
  PublisherName: Lumen Technologies, Inc.
  ServiceCategory: Networking
  ServiceName: Lumen
layout: finops
meters:
- aggregation: max
  dimensions:
  - circuit
  - location
  name: bandwidth_mbps
  unit: Mbps
- aggregation: sum
  dimensions:
  - circuit
  name: bandwidth_volume
  unit: GB
- aggregation: sum
  dimensions:
  - service
  name: on_demand_hours
  unit: instance-hour
- aggregation: max
  name: fiber_circuits
  unit: circuit
- aggregation: sum
  dimensions:
  - api
  - endpoint
  name: api_requests
  unit: request
name: Lumen Technologies Finops
provider_name: Lumen Technologies
provider_slug: lumen-technologies
publisher_name: Lumen Technologies, Inc.
service_category: Networking
slug: lumen-technologies-finops
source_filename: lumen-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.lumen.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lumen Technologies\nproviderId: lumen-technologies\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Network\n  - Telecom\n  - Edge Cloud\ndescription: 'FOCUS-aligned FinOps for Lumen Technologies: enterprise contract-based network services\n  (fiber, IP, Internet On-Demand, edge cloud, managed security). APIs themselves are not separately\n  metered — they orchestrate underlying chargeable network services.'\nsources:\n  - https://www.lumen.com\nnotes: No public pricing/billing for the API itself; meters represent the underlying network services\n  the APIs provision.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lumen Technologies,\
  \ Inc.\nserviceCategory: Networking\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Lumen\n  ServiceCategory: Networking\n  ProviderName: Lumen Technologies\n  PublisherName: Lumen Technologies, Inc.\n  InvoiceIssuerName: Lumen Technologies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: bandwidth_mbps\n    unit: Mbps\n    aggregation: max\n    dimensions:\n      - circuit\n      - location\n  - name: bandwidth_volume\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - circuit\n  - name: on_demand_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n  - name: fiber_circuits\n    unit: circuit\n    aggregation: max\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\nprinciples:\n  - name: Visibility\n    description:\
  \ Pull bandwidth and on-demand usage from the Lumen customer portal and reconcile against\n      the monthly invoice.\n  - name: Allocation\n    description: Tag circuits and Internet On-Demand instances to internal sites/teams for chargeback.\n  - name: Optimization\n    description: Use Internet On-Demand to scale bandwidth to actual need rather than committing to peak;\n      consolidate sites onto fewer circuits where SLAs allow.\n  - name: Accountability\n    description: Network owners review monthly burn vs. contract; renegotiate at renewal as site/bandwidth mix changes.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lumen-technologies/refs/heads/main/finops/lumen-technologies-finops.yml
sources:
- https://www.lumen.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Network
- Telecom
- Edge Cloud
---
