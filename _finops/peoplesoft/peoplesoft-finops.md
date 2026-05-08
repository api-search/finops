---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rest-api.yml
  format: yaml
  label: PeopleSoft REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/rest-api.yml
- filename: application-services-framework.yml
  format: yaml
  label: PeopleSoft Application Services Framework API
  slug: application-services-framework-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/application-services-framework.yml
- filename: integration-broker.yml
  format: yaml
  label: PeopleSoft Integration Broker
  slug: integration-broker
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/integration-broker.yml
- filename: query.yml
  format: yaml
  label: PeopleSoft Query API
  slug: query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/query.yml
- filename: component-interface.yml
  format: yaml
  label: PeopleSoft Component Interface API
  slug: component-interface-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/component-interface.yml
- filename: search-framework.yml
  format: yaml
  label: PeopleSoft Search Framework API
  slug: search-framework-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/search-framework.yml
- filename: notification-framework.yml
  format: yaml
  label: PeopleSoft Notification Framework API
  slug: notification-framework-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/notification-framework.yml
- filename: chatbot-integration.yml
  format: yaml
  label: PeopleSoft Chatbot Integration Framework API
  slug: chatbot-integration-framework-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/chatbot-integration.yml
- filename: approval-workflow-engine.yml
  format: yaml
  label: PeopleSoft Approval Workflow Engine API
  slug: approval-workflow-engine-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/approval-workflow-engine.yml
- filename: process-scheduler.yml
  format: yaml
  label: PeopleSoft Process Scheduler API
  slug: process-scheduler-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/process-scheduler.yml
- filename: cloud-manager.yml
  format: yaml
  label: PeopleSoft Cloud Manager API
  slug: cloud-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/cloud-manager.yml
- filename: update-manager.yml
  format: yaml
  label: PeopleSoft Update Manager API
  slug: update-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/update-manager.yml
- filename: pivot-grid.yml
  format: yaml
  label: PeopleSoft Pivot Grid API
  slug: pivot-grid-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/pivot-grid.yml
- filename: hcm.yml
  format: yaml
  label: PeopleSoft HCM API
  slug: hcm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/hcm.yml
- filename: recruiting-talent-management.yml
  format: yaml
  label: PeopleSoft Recruiting and Talent Management API
  slug: recruiting-and-talent-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/recruiting-talent-management.yml
- filename: financials.yml
  format: yaml
  label: PeopleSoft Financials API
  slug: financials-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/financials.yml
- filename: supply-chain-management.yml
  format: yaml
  label: PeopleSoft Supply Chain Management API
  slug: supply-chain-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/supply-chain-management.yml
- filename: crm.yml
  format: yaml
  label: PeopleSoft CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/crm.yml
- filename: campus-solutions.yml
  format: yaml
  label: PeopleSoft Campus Solutions API
  slug: campus-solutions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/campus-solutions.yml
- filename: enterprise-performance-management.yml
  format: yaml
  label: PeopleSoft Enterprise Performance Management API
  slug: enterprise-performance-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/enterprise-performance-management.yml
- filename: interaction-hub.yml
  format: yaml
  label: PeopleSoft Interaction Hub API
  slug: interaction-hub-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/interaction-hub.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Perpetual License + Annual Support (or OCI Cloud Credits)
description: Structural FinOps definition for Oracle PeopleSoft. Licensed via Oracle's enterprise channel with module-, user-, and processor-based metering plus annual support; APIs are bundled.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Oracle Corporation
  ProviderName: Oracle
  PublisherName: Oracle Corporation
  ServiceCategory: Enterprise Software
  ServiceName: Oracle PeopleSoft
layout: finops
meters:
- aggregation: max
  description: Named-user PeopleSoft licenses by module
  dimensions:
  - module
  - environment
  name: named_user_licenses
  unit: user-year
- aggregation: max
  description: Processor-metric licenses for unlimited-user deployments
  dimensions:
  - module
  - server
  name: processor_licenses
  unit: processor-year
- aggregation: count
  description: Oracle annual support / maintenance fee
  dimensions:
  - csi
  name: annual_support
  unit: year
- aggregation: sum
  description: OCI cloud credits consumed by hosted PeopleSoft deployment, where applicable
  dimensions:
  - tenancy
  - region
  name: oci_credits
  unit: credit
name: Peoplesoft Finops
provider_name: PeopleSoft
provider_slug: peoplesoft
publisher_name: Oracle Corporation
service_category: Enterprise Software
slug: peoplesoft-finops
source_filename: peoplesoft-finops.yml
source_heading: FinOps Profile
source_url: https://docs.oracle.com/en/applications/peoplesoft/index.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PeopleSoft\nproviderId: peoplesoft\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: No public pricing. Oracle license + support is bundled across modules and named users;\n  this artifact captures the structural FOCUS-shape only.\ntags:\n  - FinOps\n  - FOCUS\n  - ERP\n  - HCM\n  - Enterprise Software\ndescription: Structural FinOps definition for Oracle PeopleSoft. Licensed via Oracle's enterprise\n  channel with module-, user-, and processor-based metering plus annual support; APIs are\n  bundled.\nsources:\n  - https://docs.oracle.com/en/applications/peoplesoft/index.html\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Oracle Corporation\nserviceCategory: Enterprise Software\nbillingModel:\n  pricingCategory: Perpetual License + Annual Support (or OCI Cloud Credits)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Oracle PeopleSoft\n  ServiceCategory: Enterprise Software\n  ProviderName: Oracle\n  PublisherName: Oracle Corporation\n  InvoiceIssuerName: Oracle Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: named_user_licenses\n    description: Named-user PeopleSoft licenses by module\n    unit: user-year\n    aggregation: max\n    dimensions:\n      - module\n      - environment\n  - name: processor_licenses\n    description: Processor-metric licenses for unlimited-user deployments\n    unit: processor-year\n    aggregation: max\n    dimensions:\n      - module\n      - server\n  - name: annual_support\n    description: Oracle annual support / maintenance fee\n\
  \    unit: year\n    aggregation: count\n    dimensions:\n      - csi\n  - name: oci_credits\n    description: OCI cloud credits consumed by hosted PeopleSoft deployment, where applicable\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - tenancy\n      - region\nprinciples:\n  - name: Visibility\n    description: Visibility comes from Oracle CSI-level invoices, the License Management\n      Service (LMS) audit trail, and OCI billing for hosted deployments — there is no PeopleSoft-native\n      cost API.\n  - name: Allocation\n    description: Allocate by module (HCM / Financials / SCM / CRM / Campus Solutions) and\n      by environment (prod / non-prod); apportion named-user licenses to business units.\n  - name: Optimization\n    description: Optimize by retiring unused named-user licenses at renewal, consolidating\n      to processor licensing where user counts grow, and tuning PeopleTools batch / IB workloads\n      to reduce OCI credit burn.\n  - name: Accountability\n\
  \    description: ERP system owner / CIO accountable for the Oracle contract; module owners\n      accountable for license-utilization at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/finops/peoplesoft-finops.yml
sources:
- https://docs.oracle.com/en/applications/peoplesoft/index.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- ERP
- HCM
- Enterprise Software
---
