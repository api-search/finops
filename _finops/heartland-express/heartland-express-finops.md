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
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for Heartland Express: shipper / 3PL integration bundled into the broader transportation services contract. Meters describe shipment-tendering and tracking volume for allocation across business units.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Heartland Express, Inc.
  PricingCategory: Subscription
  PricingUnit: partner-agreement
  ProviderName: Heartland Express
  PublisherName: Heartland Express, Inc.
  ServiceCategory: Transportation / Logistics Carrier Partner API
  ServiceName: Heartland Express API
layout: finops
meters:
- aggregation: sum
  description: Partner-integration request volume (allocation meter)
  dimensions:
  - partner
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Loads tendered to Heartland Express via the API
  dimensions:
  - partner
  - lane
  name: loads_tendered
  unit: load
- aggregation: sum
  description: Shipment status / tracking events delivered
  dimensions:
  - partner
  - event_type
  name: tracking_events
  unit: event
name: Heartland Express Finops
provider_name: Heartland Express
provider_slug: heartland-express
publisher_name: Heartland Express, Inc.
service_category: Transportation / Logistics Carrier Partner API
slug: heartland-express-finops
source_filename: heartland-express-finops.yml
source_heading: FinOps Profile
source_url: https://www.heartlandexpress.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Heartland Express\nproviderId: heartland-express\npublisherName: Heartland Express, Inc.\nserviceCategory: Transportation / Logistics Carrier Partner API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Trucking\n  - Transportation\n  - Logistics\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Heartland Express: shipper / 3PL integration\n  bundled into the broader transportation services contract. Meters describe shipment-tendering and\n  tracking volume for allocation across business units.'\nnotes: No public commercial model is published for the API. Reconcile against\
  \ the shipper agreement.\nsources:\n  - https://www.heartlandexpress.com/\nprinciples:\n  - name: Visibility\n    description: Track API request volume and shipment events via the Heartland partner gateway\n      logs; correlate with tendered loads and invoiced freight.\n  - name: Allocation\n    description: Allocate integration cost across shipper business units and lanes using the calling\n      partner / TMS identifier.\n  - name: Optimization\n    description: Use webhook-driven status updates rather than high-frequency polling; batch\n      tender/accept and EDI 214 status messages.\n  - name: Accountability\n    description: Designate a partner-integration owner per shipper; review API utilization quarterly\n      against tendered-load volumes.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning\
  \ and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Heartland Express API\n  ServiceCategory: Transportation / Logistics Carrier Partner API\n  ProviderName: Heartland Express\n  PublisherName: Heartland Express, Inc.\n  InvoiceIssuerName: Heartland Express, Inc.\n  PricingCategory: Subscription\n\
  \  PricingUnit: partner-agreement\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_requests\n    description: Partner-integration request volume (allocation meter)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - endpoint\n  - name: loads_tendered\n    description: Loads tendered to Heartland Express via the API\n    unit: load\n    aggregation: sum\n    dimensions:\n      - partner\n      - lane\n  - name: tracking_events\n    description: Shipment status / tracking events delivered\n    unit: event\n    aggregation: sum\n    dimensions:\n      - partner\n      - event_type\napis:\n  - name: Heartland Express API\n    baseURL: https://api.heartlandexpress.com\n    tags:\n      - Trucking\n      - Transportation\n      - Logistics\n    serviceName: Heartland Express API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Load Tendered\n    metric: billed_cost / loads_tendered\n    target: TBD\n  - name: Cost per Tracking\
  \ Event\n    metric: billed_cost / tracking_events\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/heartland-express/refs/heads/main/finops/heartland-express-finops.yml
sources:
- https://www.heartlandexpress.com/
specification: FinOps Framework
tags:
- Trucking
- Transportation
- Logistics
- FinOps
- Cost Management
- FOCUS
---
