---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-boot-admin-console-openapi.yml
  format: yaml
  label: Spring Boot Admin Server API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-boot-admin-console/refs/heads/main/openapi/spring-boot-admin-console-openapi.yml
billing_model:
  billingCurrency: EUR
  billingFrequency: On-Demand
  chargeCategories:
  - Purchase
  pricingCategory: Open Source
description: Spring Boot Admin is open-source self-hosted software with no vendor invoice. FinOps applies only to the underlying infrastructure that runs the Admin Server (compute, memory, storage) and to optional codecentric commercial support contracts.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: codecentric AG
  ProviderName: Spring Boot Admin
  PublisherName: codecentric AG
  ServiceCategory: Developer Tools
  ServiceName: Spring Boot Admin
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract_tier
  name: support_engagement
  unit: month
name: Spring Boot Admin Console Finops
provider_name: Spring Boot Admin Console
provider_slug: spring-boot-admin-console
publisher_name: codecentric AG
service_category: Developer Tools
slug: spring-boot-admin-console-finops
source_filename: spring-boot-admin-console-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/codecentric/spring-boot-admin
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spring Boot Admin Console\nproviderId: spring-boot-admin-console\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Actuator\n  - Administration\n  - Java\n  - Microservices\n  - Monitoring\n  - Spring Boot\n  - FinOps\n  - FOCUS\ndescription: Spring Boot Admin is open-source self-hosted software with no vendor invoice. FinOps applies only to the underlying infrastructure that runs the Admin Server (compute, memory, storage) and to optional codecentric commercial support contracts.\nsources:\n  - https://github.com/codecentric/spring-boot-admin\n  - https://www.codecentric.de/\nnotes: No vendor billing surface. FinOps signal lives in the operator's own cloud-provider invoice (compute hours / memory) and in any codecentric support contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: codecentric AG\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: On-Demand\n  billingCurrency: EUR\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Spring Boot Admin\n  ServiceCategory: Developer Tools\n  ProviderName: Spring Boot Admin\n  PublisherName: codecentric AG\n  InvoiceIssuerName: codecentric AG\n  BillingCurrency: EUR\nmeters:\n  - name: support_engagement\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract_tier\nprinciples:\n  - name: Visibility\n    description: Costs surface in the operator's cloud bill (the compute/memory hosting the Admin Server) and in any codecentric support invoice. The software itself emits no usage telemetry beyond Spring Boot Actuator metrics.\n  - name: Allocation\n    description: Allocate Admin Server hosting cost to the platform/SRE\
  \ team that owns it. Tag the underlying compute with team and environment via the cloud provider's tagging.\n  - name: Optimization\n    description: Right-size the Admin Server JVM and consolidate multiple environments into a single Admin Server where security boundaries allow. The software is free; the only cost lever is infrastructure footprint.\n  - name: Accountability\n    description: Platform/SRE team owns the Admin Server budget. There is no per-call chargeback because there is no vendor meter.\nmaintainers:\n  - name: codecentric AG\n    url: https://www.codecentric.de/\n    email: info@codecentric.de\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-boot-admin-console/refs/heads/main/finops/spring-boot-admin-console-finops.yml
sources:
- https://github.com/codecentric/spring-boot-admin
- https://www.codecentric.de/
specification: FinOps Framework
tags:
- Actuator
- Administration
- Java
- Microservices
- Monitoring
- Spring Boot
- FinOps
- FOCUS
---
