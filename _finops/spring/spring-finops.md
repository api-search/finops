---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-boot-actuator-openapi.yml
  format: yaml
  label: Spring Boot Actuator API
  slug: spring-boot-actuator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring/refs/heads/main/openapi/spring-boot-actuator-openapi.yml
- filename: spring-initializr-api-openapi.yml
  format: yaml
  label: Spring Initializr API
  slug: spring-initializr-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring/refs/heads/main/openapi/spring-initializr-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FOCUS-aligned FinOps placeholder for the Spring Framework. The framework itself has no consumption cost; the FinOps surface lives in the optional Tanzu Spring support contract and in the cloud / runtime cost of applications built with Spring.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Broadcom Inc.
  ProviderName: Spring (VMware Tanzu)
  PublisherName: Broadcom Inc.
  ServiceCategory: Open-Source Framework
  ServiceName: Spring Framework
layout: finops
meters:
- aggregation: sum
  description: Tanzu Spring / Spring Enterprise support subscription. Billing basis is contractual (typically per-application or per-VM); not publicly disclosed.
  dimensions:
  - support_tier
  name: tanzu_spring_support
  unit: varies
name: Spring Finops
provider_name: Spring Framework
provider_slug: spring
publisher_name: Broadcom Inc. (VMware Tanzu)
service_category: Open-Source Framework
slug: spring-finops
source_filename: spring-finops.yml
source_heading: FinOps Profile
source_url: https://spring.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spring Framework\nproviderId: spring\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Framework\n  - Java\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for the Spring Framework. The\n  framework itself has no consumption cost; the FinOps surface lives in the\n  optional Tanzu Spring support contract and in the cloud / runtime cost of\n  applications built with Spring.\nsources:\n  - https://spring.io/\n  - https://enterprise.spring.io/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Broadcom Inc. (VMware Tanzu)\nserviceCategory: Open-Source Framework\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency:\
  \ Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Spring Framework\n  ServiceCategory: Open-Source Framework\n  ProviderName: Spring (VMware Tanzu)\n  PublisherName: Broadcom Inc.\n  InvoiceIssuerName: Broadcom Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tanzu_spring_support\n    description: Tanzu Spring / Spring Enterprise support subscription. Billing\n      basis is contractual (typically per-application or per-VM); not publicly\n      disclosed.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - support_tier\nprinciples:\n  - name: Visibility\n    description: The framework itself has no usage telemetry. FinOps visibility\n      lives downstream — APM (e.g. JFR, Micrometer to Prometheus / Datadog) for\n      runtime cost, and the Tanzu support contract for the support fee line.\n  - name: Allocation\n    description: Allocate Tanzu Spring support against the platform team that\n      contracts the subscription;\
  \ allocate runtime cost of Spring applications\n      to the workload team via cloud-account / namespace tagging.\n  - name: Optimization\n    description: At the framework level, optimize startup time and memory (GraalVM\n      native images, Spring Boot lazy initialization, AOT processing) to reduce\n      cloud runtime cost. At the support level, scope the Tanzu subscription to\n      production application count rather than dev/test.\n  - name: Accountability\n    description: Tanzu support cost owned by the platform team; per-application\n      runtime cost owned by the application team that operates each service.\nnotes: Open-source framework; per-call FinOps applies to the consuming\n  application's runtime, not to Spring itself.\nmaintainers:\n  - name: VMware Tanzu (Broadcom)\n    email: spring-team@vmware.com\n    url: https://spring.io/team\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring/refs/heads/main/finops/spring-finops.yml
sources:
- https://spring.io/
- https://enterprise.spring.io/
specification: FinOps Framework
tags:
- Framework
- Java
- Open Source
- FinOps
- FOCUS
---
