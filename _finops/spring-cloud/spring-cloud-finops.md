---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-cloud-gateway-actuator-openapi.yml
  format: yaml
  label: Spring Cloud Gateway
  slug: spring-cloud-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-cloud/refs/heads/main/openapi/spring-cloud-gateway-actuator-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Open Source
description: Spring Cloud is open-source self-hosted software with no vendor invoice. FinOps applies only to the cloud infrastructure that runs Spring Cloud components (Config Server, Gateway, Eureka, etc.) and to optional VMware Tanzu Spring / Broadcom commercial support contracts.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Broadcom
  ProviderName: Spring Cloud
  PublisherName: Broadcom
  ServiceCategory: Developer Tools
  ServiceName: Spring Cloud
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract_tier
  - cores
  name: spring_runtime_subscription
  unit: month
name: Spring Cloud Finops
provider_name: Spring Cloud
provider_slug: spring-cloud
publisher_name: Broadcom (VMware Tanzu)
service_category: Developer Tools
slug: spring-cloud-finops
source_filename: spring-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://spring.io/projects/spring-cloud
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spring Cloud\nproviderId: spring-cloud\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud Native\n  - Distributed Systems\n  - Java\n  - Microservices\n  - Spring Framework\n  - FinOps\n  - FOCUS\ndescription: Spring Cloud is open-source self-hosted software with no vendor invoice. FinOps applies only to the cloud infrastructure that runs Spring Cloud components (Config Server, Gateway, Eureka, etc.) and to optional VMware Tanzu Spring / Broadcom commercial support contracts.\nsources:\n  - https://spring.io/projects/spring-cloud\n  - https://tanzu.vmware.com/spring-runtime\nnotes: No vendor usage meter. FinOps signal lives in the operator's own cloud-provider invoice and any Tanzu Spring support contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Broadcom (VMware Tanzu)\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Spring Cloud\n  ServiceCategory: Developer Tools\n  ProviderName: Spring Cloud\n  PublisherName: Broadcom\n  InvoiceIssuerName: Broadcom\n  BillingCurrency: USD\nmeters:\n  - name: spring_runtime_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract_tier\n      - cores\nprinciples:\n  - name: Visibility\n    description: Spring Cloud emits Micrometer metrics (request counts, gateway timings, circuit breaker state) that operators ship to their observability stack. Vendor cost is visible only on the Tanzu Spring / Broadcom invoice line.\n  - name: Allocation\n    description: Allocate the underlying compute footprint of Config\
  \ Server, Gateway, Eureka, etc. by team via cloud provider tags. The Tanzu support subscription is typically a single platform-org line, not chargeable per consuming team.\n  - name: Optimization\n    description: Cost levers are infrastructure-side - consolidate Config Server and Eureka into shared platform clusters, autoscale Gateway pods on RPS, and use Resilience4j to shed load before it hits paid downstream APIs.\n  - name: Accountability\n    description: Platform/SRE team owns Spring Cloud control-plane spend; product teams own the cost of their own Spring Boot services that consume it.\nmaintainers:\n  - name: VMware Tanzu / Broadcom\n    url: https://tanzu.vmware.com/spring-runtime\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-cloud/refs/heads/main/finops/spring-cloud-finops.yml
sources:
- https://spring.io/projects/spring-cloud
- https://tanzu.vmware.com/spring-runtime
specification: FinOps Framework
tags:
- Cloud Native
- Distributed Systems
- Java
- Microservices
- Spring Framework
- FinOps
- FOCUS
---
