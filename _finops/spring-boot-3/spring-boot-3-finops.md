---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-boot-3-actuator-openapi.yml
  format: yaml
  label: Spring Boot Actuator API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-boot-3/refs/heads/main/openapi/spring-boot-3-actuator-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FOCUS-aligned FinOps placeholder for Spring Boot 3. The framework is free and open-source; the FinOps surface lives in the optional Tanzu Spring support contract and in the cloud / runtime cost of the applications it powers.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Broadcom Inc.
  ProviderName: Spring Boot (VMware Tanzu)
  PublisherName: Broadcom Inc.
  ServiceCategory: Open-Source Framework
  ServiceName: Spring Boot 3
layout: finops
meters:
- aggregation: sum
  description: Tanzu Spring support subscription that covers Spring Boot. Billing basis is contractual; not publicly disclosed.
  dimensions:
  - support_tier
  name: tanzu_spring_support
  unit: varies
name: Spring Boot 3 Finops
provider_name: Spring Boot 3
provider_slug: spring-boot-3
publisher_name: Broadcom Inc. (VMware Tanzu)
service_category: Open-Source Framework
slug: spring-boot-3-finops
source_filename: spring-boot-3-finops.yml
source_heading: FinOps Profile
source_url: https://spring.io/projects/spring-boot
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spring Boot 3\nproviderId: spring-boot-3\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Framework\n  - Java\n  - Spring Boot\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Spring Boot 3. The framework\n  is free and open-source; the FinOps surface lives in the optional Tanzu Spring\n  support contract and in the cloud / runtime cost of the applications it\n  powers.\nsources:\n  - https://spring.io/projects/spring-boot\n  - https://enterprise.spring.io/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Broadcom Inc. (VMware Tanzu)\nserviceCategory: Open-Source Framework\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency:\
  \ Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Spring Boot 3\n  ServiceCategory: Open-Source Framework\n  ProviderName: Spring Boot (VMware Tanzu)\n  PublisherName: Broadcom Inc.\n  InvoiceIssuerName: Broadcom Inc.\n  BillingCurrency: USD\nmeters:\n  - name: tanzu_spring_support\n    description: Tanzu Spring support subscription that covers Spring Boot.\n      Billing basis is contractual; not publicly disclosed.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - support_tier\nprinciples:\n  - name: Visibility\n    description: Use Spring Boot Actuator metrics exposed via Micrometer\n      (Prometheus, Datadog, Dynatrace, Elastic) to attribute runtime cost to\n      requests and tenants. The framework itself emits no billing telemetry.\n  - name: Allocation\n    description: Allocate Tanzu support fees to the platform team that contracts\n      the subscription; allocate runtime spend per application using cloud-tag\n\
  \      / Kubernetes namespace conventions and Boot's `info` and `metrics`\n      endpoints.\n  - name: Optimization\n    description: Reduce cloud runtime cost with GraalVM native images, Spring\n      Boot 3's AOT processing, and lazy initialization. Tune actuator scrape\n      intervals to balance observability cost. Choose JVM heap and CDS image\n      settings to fit the deployment shape.\n  - name: Accountability\n    description: Tanzu support cost owned by the platform team. Per-application\n      compute and observability cost owned by the workload team operating the\n      Spring Boot service.\nnotes: Open-source library; per-call FinOps applies to the runtime of the\n  consuming application, not to Spring Boot itself.\nmaintainers:\n  - name: VMware Tanzu (Broadcom)\n    email: spring-team@vmware.com\n    url: https://spring.io/team\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-boot-3/refs/heads/main/finops/spring-boot-3-finops.yml
sources:
- https://spring.io/projects/spring-boot
- https://enterprise.spring.io/
specification: FinOps Framework
tags:
- Framework
- Java
- Spring Boot
- FinOps
- FOCUS
---
