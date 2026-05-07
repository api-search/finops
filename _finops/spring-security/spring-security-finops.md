---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-security-oauth2-openapi.yml
  format: yaml
  label: Spring Security OAuth2 API
  slug: spring-security-oauth2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-security/refs/heads/main/openapi/spring-security-oauth2-openapi.yml
- filename: spring-authorization-server-openapi.yml
  format: yaml
  label: Spring Authorization Server API
  slug: spring-authorization-server
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-security/refs/heads/main/openapi/spring-authorization-server-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Open Source
description: Spring Security is open-source self-hosted software with no vendor invoice. FinOps applies only to the cloud infrastructure that hosts the Authorization Server / resource servers and to optional VMware Tanzu Spring / Broadcom commercial support contracts.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Broadcom
  ProviderName: Spring Security
  PublisherName: Broadcom
  ServiceCategory: Identity
  ServiceName: Spring Security
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract_tier
  - cores
  name: spring_runtime_subscription
  unit: month
name: Spring Security Finops
provider_name: Spring Security
provider_slug: spring-security
publisher_name: Broadcom (VMware Tanzu)
service_category: Identity
slug: spring-security-finops
source_filename: spring-security-finops.yml
source_heading: FinOps Profile
source_url: https://spring.io/projects/spring-security
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spring Security\nproviderId: spring-security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Authentication\n  - Authorization\n  - Java\n  - OAuth2\n  - Spring Framework\n  - FinOps\n  - FOCUS\ndescription: Spring Security is open-source self-hosted software with no vendor invoice. FinOps applies only to the cloud infrastructure that hosts the Authorization Server / resource servers and to optional VMware Tanzu Spring / Broadcom commercial support contracts.\nsources:\n  - https://spring.io/projects/spring-security\n  - https://tanzu.vmware.com/spring-runtime\nnotes: No vendor usage meter. Real cost is the compute that runs the Authorization Server plus any Tanzu Spring support contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Broadcom (VMware Tanzu)\nserviceCategory: Identity\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Spring Security\n  ServiceCategory: Identity\n  ProviderName: Spring Security\n  PublisherName: Broadcom\n  InvoiceIssuerName: Broadcom\n  BillingCurrency: USD\nmeters:\n  - name: spring_runtime_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract_tier\n      - cores\nprinciples:\n  - name: Visibility\n    description: Spring Security emits Micrometer counters for authentication outcomes (success, failure, lockout) and OAuth2 token issuance; operators ship these to their SIEM and observability stack. Vendor cost is visible only on the Tanzu Spring invoice.\n  - name: Allocation\n    description: Authorization Server hosting cost is typically a shared\
  \ platform-org line. Allocate downstream resource-server compute by the consuming product team via cloud provider tags.\n  - name: Optimization\n    description: Cost levers are infrastructure-side - cache JWKs, prefer JWT over opaque token introspection to avoid a round-trip per request, and right-size the token endpoint pods against measured login RPS.\n  - name: Accountability\n    description: Platform/security team owns the Authorization Server budget and any Tanzu Spring support contract; product teams own the cost of their resource servers.\nmaintainers:\n  - name: VMware Tanzu / Broadcom\n    url: https://tanzu.vmware.com/spring-runtime\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-security/refs/heads/main/finops/spring-security-finops.yml
sources:
- https://spring.io/projects/spring-security
- https://tanzu.vmware.com/spring-runtime
specification: FinOps Framework
tags:
- Authentication
- Authorization
- Java
- OAuth2
- Spring Framework
- FinOps
- FOCUS
---
