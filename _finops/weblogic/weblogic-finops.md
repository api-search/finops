---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: weblogic-restful-management-services-openapi.yml
  format: yaml
  label: WebLogic RESTful Management Services API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/weblogic/refs/heads/main/openapi/weblogic-restful-management-services-openapi.yml
- filename: weblogic-monitoring-diagnostics-openapi.yml
  format: yaml
  label: WebLogic Monitoring and Diagnostics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/weblogic/refs/heads/main/openapi/weblogic-monitoring-diagnostics-openapi.yml
- filename: weblogic-deployment-openapi.yml
  format: yaml
  label: WebLogic Deployment API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/weblogic/refs/heads/main/openapi/weblogic-deployment-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Software License + Support
description: FinOps placement for Oracle WebLogic Server. WebLogic is sold as a perpetual / subscription software license (per processor / OCPU / Named User Plus), so spend tracks license counts, support renewals, and underlying infrastructure rather than a metered API surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Oracle Corporation
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  ServiceCategory: Application Server / Middleware
  ServiceName: Oracle WebLogic Server
layout: finops
meters:
- aggregation: sum
  description: Oracle WebLogic Server license entitlement, sized per processor / OCPU / Named User Plus per Oracle Technology Price List.
  name: weblogic_license
  unit: varies
- aggregation: sum
  description: Oracle technical support and updates renewal on the WebLogic license.
  name: weblogic_support
  unit: month
name: Weblogic Finops
provider_name: Oracle WebLogic Server APIs
provider_slug: weblogic
publisher_name: Oracle Corporation
service_category: Application Server / Middleware
slug: weblogic-finops
source_filename: weblogic-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/java/weblogic/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle WebLogic Server APIs\nproviderId: weblogic\npublisherName: Oracle Corporation\nserviceCategory: Application Server / Middleware\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Application Server\n  - Enterprise\n  - Java EE\n  - Middleware\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps placement for Oracle WebLogic Server. WebLogic is sold as a perpetual / subscription\n  software license (per processor / OCPU / Named User Plus), so spend tracks license counts, support\n  renewals, and underlying infrastructure rather than a metered API surface.\nnotes: oracle.com pricing 403 on fetch. FOCUS mapping\
  \ reflects software-license shape; no usage-API\n  meters available.\nsources:\n  - https://www.oracle.com/java/weblogic/\nbillingModel:\n  pricingCategory: Software License + Support\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Oracle WebLogic Server\n  ServiceCategory: Application Server / Middleware\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle Corporation\n  BillingCurrency: USD\nmeters:\n  - name: weblogic_license\n    description: Oracle WebLogic Server license entitlement, sized per processor / OCPU / Named User\n      Plus per Oracle Technology Price List.\n    unit: varies\n    aggregation: sum\n  - name: weblogic_support\n    description: Oracle technical support and updates renewal on the WebLogic license.\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility comes from Oracle order documents and the customer's\
  \ License\n      Management Service (LMS) records, not a public usage API.\n  - name: Allocation\n    description: Allocate WebLogic spend by domain, business unit, or hosted application using internal\n      CMDB / cost-center tags on the licensed processors and managed servers.\n  - name: Optimization\n    description: Cost levers are processor-count consolidation, soft-partitioning where Oracle-approved,\n      Named-User-Plus modeling, and renegotiation of ULAs at renewal.\n  - name: Accountability\n    description: Middleware platform owners and Oracle license-management leads coordinate renewals\n      and true-ups with Oracle account management.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/weblogic/refs/heads/main/finops/weblogic-finops.yml
sources:
- https://www.oracle.com/java/weblogic/
specification: FinOps Framework
tags:
- Application Server
- Enterprise
- Java EE
- Middleware
- FinOps
- FOCUS
- Contact Sales
---
