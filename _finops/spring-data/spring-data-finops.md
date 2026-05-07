---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-data-rest-openapi.yml
  format: yaml
  label: Spring Data REST
  slug: spring-data-rest
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-data/refs/heads/main/openapi/spring-data-rest-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Open Source
description: Spring Data is open-source self-hosted software with no vendor invoice. FinOps applies only to the cloud infrastructure that hosts the application (compute, memory) and to the underlying database the Spring Data repositories talk to (RDS, MongoDB Atlas, Redis Cloud, etc.).
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Broadcom
  ProviderName: Spring Data
  PublisherName: Broadcom
  ServiceCategory: Developer Tools
  ServiceName: Spring Data
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract_tier
  - cores
  name: spring_runtime_subscription
  unit: month
name: Spring Data Finops
provider_name: Spring Data
provider_slug: spring-data
publisher_name: Broadcom (VMware Tanzu)
service_category: Developer Tools
slug: spring-data-finops
source_filename: spring-data-finops.yml
source_heading: FinOps Profile
source_url: https://spring.io/projects/spring-data
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Spring Data\nproviderId: spring-data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Data Access\n  - Database\n  - Java\n  - Spring Framework\n  - FinOps\n  - FOCUS\ndescription: Spring Data is open-source self-hosted software with no vendor invoice. FinOps applies only to the cloud infrastructure that hosts the application (compute, memory) and to the underlying database the Spring Data repositories talk to (RDS, MongoDB Atlas, Redis Cloud, etc.).\nsources:\n  - https://spring.io/projects/spring-data\n  - https://tanzu.vmware.com/spring-runtime\nnotes: No vendor usage meter for Spring Data itself. Real cost lives in the database / datastore invoice that backs the repositories, plus optional Tanzu Spring support.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Broadcom (VMware Tanzu)\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Spring Data\n  ServiceCategory: Developer Tools\n  ProviderName: Spring Data\n  PublisherName: Broadcom\n  InvoiceIssuerName: Broadcom\n  BillingCurrency: USD\nmeters:\n  - name: spring_runtime_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract_tier\n      - cores\nprinciples:\n  - name: Visibility\n    description: Spring Data exposes Micrometer metrics for repository-level query timing and HikariCP pool saturation; operators ship these to their observability stack to attribute database cost back to specific repositories and endpoints.\n  - name: Allocation\n    description: Allocate the underlying database spend\
  \ (RDS, MongoDB Atlas, Redis Cloud) to the team that owns each Spring Data repository. Tag the database resources with team and product in the cloud provider's tagging.\n  - name: Optimization\n    description: Cost levers live in the data layer - tune query plans surfaced via JPA/SQL logging, cap PageSize defaults on Spring Data REST collection resources, and use projections to shrink payload size and downstream egress.\n  - name: Accountability\n    description: Application teams own the cost of the queries their Spring Data repositories generate; platform/SRE owns the shared datastore footprint and any Tanzu Spring support contract.\nmaintainers:\n  - name: VMware Tanzu / Broadcom\n    url: https://tanzu.vmware.com/spring-runtime\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-data/refs/heads/main/finops/spring-data-finops.yml
sources:
- https://spring.io/projects/spring-data
- https://tanzu.vmware.com/spring-runtime
specification: FinOps Framework
tags:
- Data Access
- Database
- Java
- Spring Framework
- FinOps
- FOCUS
---
