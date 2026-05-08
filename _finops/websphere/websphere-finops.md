---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: 9.0.5
  format: yaml
  label: WebSphere Application Server Admin API
  slug: websphere-admin-rest-api
  spec_type: OpenAPI
  url: https://www.ibm.com/docs/en/was/9.0.5?topic=api-openapi-specification
- filename: websphere-liberty-admin-rest-api.yml
  format: yaml
  label: WebSphere Liberty Admin REST API
  slug: websphere-liberty-admin-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-liberty-admin-rest-api.yml
- filename: websphere-liberty-rest-connector-api.yml
  format: yaml
  label: WebSphere Liberty REST Connector API
  slug: websphere-liberty-rest-connector-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-liberty-rest-connector-api.yml
- filename: websphere-mq-rest-api.yml
  format: yaml
  label: WebSphere MQ REST API
  slug: websphere-mq-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-mq-rest-api.yml
- filename: websphere-liberty-collective-controller-rest-api.yml
  format: yaml
  label: WebSphere Liberty Collective Controller REST API
  slug: websphere-liberty-collective-controller-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-liberty-collective-controller-rest-api.yml
- filename: websphere-automation-rest-api.yml
  format: yaml
  label: WebSphere Automation REST API
  slug: websphere-automation-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-automation-rest-api.yml
- filename: open-liberty-apis.yml
  format: yaml
  label: Open Liberty APIs
  slug: open-liberty-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/open-liberty-apis.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Software License + Support
description: FinOps placement for IBM WebSphere. WebSphere is sold as a perpetual / subscription software license (per PVU / VPC / Container core) through IBM Passport Advantage or Cloud Paks; spend tracks license entitlement, S&S renewals, and underlying infrastructure rather than a metered API surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: IBM Corporation
  ProviderName: IBM
  PublisherName: IBM Corporation
  ServiceCategory: Application Server / Middleware
  ServiceName: IBM WebSphere
layout: finops
meters:
- aggregation: sum
  description: WebSphere license entitlement, sized per PVU / VPC / Container core via IBM Passport Advantage or Cloud Pak for Applications.
  name: websphere_license
  unit: varies
- aggregation: sum
  description: IBM Subscription & Support renewal on the WebSphere entitlement.
  name: websphere_subscription_and_support
  unit: month
name: Websphere Finops
provider_name: IBM WebSphere
provider_slug: websphere
publisher_name: IBM Corporation
service_category: Application Server / Middleware
slug: websphere-finops
source_filename: websphere-finops.yml
source_heading: FinOps Profile
source_url: https://www.ibm.com/products/websphere-application-server
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: IBM WebSphere\nproviderId: websphere\npublisherName: IBM Corporation\nserviceCategory: Application Server / Middleware\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Server\n  - Cloud Native\n  - Enterprise Java\n  - J2EE\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps placement for IBM WebSphere. WebSphere is sold as a perpetual / subscription\n  software license (per PVU / VPC / Container core) through IBM Passport Advantage or Cloud Paks; spend\n  tracks license entitlement, S&S renewals, and underlying infrastructure rather than a metered API\n  surface.\nnotes: ibm.com pricing 403 on\
  \ fetch. FOCUS mapping reflects software-license shape; no public usage\n  API meters available.\nsources:\n  - https://www.ibm.com/products/websphere-application-server\nbillingModel:\n  pricingCategory: Software License + Support\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: IBM WebSphere\n  ServiceCategory: Application Server / Middleware\n  ProviderName: IBM\n  PublisherName: IBM Corporation\n  InvoiceIssuerName: IBM Corporation\n  BillingCurrency: USD\nmeters:\n  - name: websphere_license\n    description: WebSphere license entitlement, sized per PVU / VPC / Container core via IBM Passport\n      Advantage or Cloud Pak for Applications.\n    unit: varies\n    aggregation: sum\n  - name: websphere_subscription_and_support\n    description: IBM Subscription & Support renewal on the WebSphere entitlement.\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility\
  \ comes from IBM Passport Advantage entitlement reports and the\n      customer's IBM License Metric Tool (ILMT) deployment.\n  - name: Allocation\n    description: Allocate WebSphere spend by cell, deployment, or business application using ILMT\n      tagging and CMDB ownership records.\n  - name: Optimization\n    description: Cost levers include sub-capacity licensing via ILMT, migration from WAS Traditional to\n      WebSphere Liberty, Cloud Pak entitlement sharing, and consolidation at S&S renewal.\n  - name: Accountability\n    description: Middleware platform owners and IBM software-asset-management leads coordinate true-ups\n      and renewals with IBM account management.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/finops/websphere-finops.yml
sources:
- https://www.ibm.com/products/websphere-application-server
specification: FinOps Framework
tags:
- Application Server
- Cloud Native
- Enterprise Java
- J2EE
- FinOps
- FOCUS
- Contact Sales
---
