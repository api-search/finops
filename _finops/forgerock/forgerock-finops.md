---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: forgerock-identity-cloud-openapi.yml
  format: yaml
  label: ForgeRock Identity Cloud REST API
  slug: forgerock-identity-cloud-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/forgerock/refs/heads/main/openapi/forgerock-identity-cloud-openapi.yml
- filename: forgerock-access-management-openapi.yml
  format: yaml
  label: ForgeRock Access Management API
  slug: forgerock-access-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/forgerock/refs/heads/main/openapi/forgerock-access-management-openapi.yml
- filename: forgerock-identity-management-openapi.yml
  format: yaml
  label: ForgeRock Identity Management API
  slug: forgerock-identity-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/forgerock/refs/heads/main/openapi/forgerock-identity-management-openapi.yml
- filename: forgerock-identity-gateway-openapi.yml
  format: yaml
  label: ForgeRock Identity Gateway API
  slug: forgerock-identity-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/forgerock/refs/heads/main/openapi/forgerock-identity-gateway-openapi.yml
- filename: forgerock-directory-services-openapi.yml
  format: yaml
  label: ForgeRock Directory Services API
  slug: forgerock-directory-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/forgerock/refs/heads/main/openapi/forgerock-directory-services-openapi.yml
- filename: forgerock-identity-governance-openapi.yml
  format: yaml
  label: ForgeRock Identity Governance API
  slug: forgerock-identity-governance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/forgerock/refs/heads/main/openapi/forgerock-identity-governance-openapi.yml
- filename: forgerock-autonomous-identity-openapi.yml
  format: yaml
  label: ForgeRock Autonomous Identity API
  slug: forgerock-autonomous-identity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/forgerock/refs/heads/main/openapi/forgerock-autonomous-identity-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps mapping for ForgeRock under Ping Identity ownership: tiered subscription IAM/CIAM with per-seat (Workforce) and per-customer (CIAM) licensing, plus add-ons (Passwordless, DaVinci) and self-hosted enterprise contracts.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Ping Identity Corporation
  ProviderName: Ping Identity Corporation
  PublisherName: Ping Identity Corporation
  ServiceCategory: Identity
  ServiceName: ForgeRock / PingOne
layout: finops
meters:
- aggregation: max
  description: Licensed Workforce IAM users (priced per user per month, annual commitment)
  dimensions:
  - tier
  - region
  - department
  name: workforce_users
  unit: seat-month
- aggregation: max
  description: Annual CIAM tier subscription (Essential or Plus)
  dimensions:
  - tier
  name: customer_identity_subscription
  unit: year
- aggregation: max
  description: Monthly Active Customers (CIAM consumption metric tracked under PingOne for Customers)
  dimensions:
  - environment
  - region
  name: monthly_active_customers
  unit: identity
- aggregation: sum
  description: End-user authentication events processed
  dimensions:
  - flow
  - mfa_factor
  name: authentications
  unit: event
- aggregation: sum
  description: PingOne Passwordless / DaVinci orchestration add-on consumption
  dimensions:
  - flow_name
  name: addon_passwordless
  unit: flow
- aggregation: max
  description: Annual ForgeRock Identity Platform (self-hosted) license fee
  dimensions:
  - product
  name: self_hosted_license
  unit: year
name: Forgerock Finops
provider_name: ForgeRock
provider_slug: forgerock
publisher_name: Ping Identity Corporation
service_category: Identity
slug: forgerock-finops
source_filename: forgerock-finops.yml
source_heading: FinOps Profile
source_url: https://www.pingidentity.com/en/platform/pricing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: ForgeRock\nproviderId: forgerock\npublisherName: Ping Identity Corporation\nserviceCategory: Identity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Access Management\n  - Authentication\n  - Identity\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps mapping for ForgeRock under Ping Identity ownership: tiered subscription IAM/CIAM with per-seat (Workforce) and per-customer (CIAM) licensing, plus add-ons (Passwordless, DaVinci) and self-hosted enterprise contracts.'\nsources:\n  - https://www.pingidentity.com/en/platform/pricing.html\n  - https://www.forgerock.com/platform/pricing\nbillingModel:\n  pricingCategory:\
  \ Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: ForgeRock / PingOne\n  ServiceCategory: Identity\n  ProviderName: Ping Identity Corporation\n  PublisherName: Ping Identity Corporation\n  InvoiceIssuerName: Ping Identity Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: workforce_users\n    description: Licensed Workforce IAM users (priced per user per month, annual commitment)\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - tier\n      - region\n      - department\n  - name: customer_identity_subscription\n    description: Annual CIAM tier subscription (Essential or Plus)\n    unit: year\n    aggregation: max\n    dimensions:\n      - tier\n  - name: monthly_active_customers\n    description: Monthly Active Customers (CIAM consumption metric tracked under PingOne for Customers)\n   \
  \ unit: identity\n    aggregation: max\n    dimensions:\n      - environment\n      - region\n  - name: authentications\n    description: End-user authentication events processed\n    unit: event\n    aggregation: sum\n    dimensions:\n      - flow\n      - mfa_factor\n  - name: addon_passwordless\n    description: PingOne Passwordless / DaVinci orchestration add-on consumption\n    unit: flow\n    aggregation: sum\n    dimensions:\n      - flow_name\n  - name: self_hosted_license\n    description: Annual ForgeRock Identity Platform (self-hosted) license fee\n    unit: year\n    aggregation: max\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Pull PingOne admin reports and ForgeRock IDM audit logs into your data warehouse; track Monthly Active Customers and Workforce seats against the contracted minimum (e.g. 5,000-user Workforce floor).\n  - name: Allocation\n    description: Tag tenants/realms by business unit and environment so seat and MAC consumption\
  \ is allocable to product lines.\n  - name: Optimization\n    description: Right-size between Essential and Plus tiers based on which advanced features (orchestration, risk) are actually used; deprovision dormant Workforce seats; consolidate duplicate CIAM tenants ahead of renewal.\n  - name: Accountability\n    description: Identity engineering owns the platform; security/compliance jointly owns CIAM cost; finance reviews seat utilization and MAC trend monthly and renegotiates the annual contract on usage data.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/forgerock/refs/heads/main/finops/forgerock-finops.yml
sources:
- https://www.pingidentity.com/en/platform/pricing.html
- https://www.forgerock.com/platform/pricing
specification: FinOps Framework
tags:
- Access Management
- Authentication
- Identity
- FinOps
- FOCUS
---
