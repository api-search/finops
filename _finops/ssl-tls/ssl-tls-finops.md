---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ssl-tls-certificate-management-openapi.yml
  format: yaml
  label: Let's Encrypt ACME API
  slug: lets-encrypt-acme
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ssl-tls/refs/heads/main/openapi/ssl-tls-certificate-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Mixed (Free + Per-Certificate)
description: SSL/TLS is a multi-vendor category index. Cost surfaces vary by certificate authority - Let's Encrypt is free; DigiCert and Sectigo bill per certificate per validation level under partner contracts. There is no single FOCUS-aligned billing model for the category; per-vendor finops artifacts should live in vendor-specific repos.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Per Vendor
  ProviderName: SSL/TLS
  PublisherName: Multiple
  ServiceCategory: Identity
  ServiceName: SSL/TLS
layout: finops
meters:
- aggregation: count
  dimensions:
  - certificate_authority
  - validation_level
  - term_length
  name: certificate_issuance
  unit: certificate
name: Ssl Tls Finops
provider_name: SSL/TLS
provider_slug: ssl-tls
publisher_name: Multiple Certificate Authorities
service_category: Identity
slug: ssl-tls-finops
source_filename: ssl-tls-finops.yml
source_heading: FinOps Profile
source_url: https://letsencrypt.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SSL/TLS\nproviderId: ssl-tls\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - SSL/TLS\n  - TLS\n  - Certificates\n  - PKI\n  - FinOps\n  - FOCUS\ndescription: SSL/TLS is a multi-vendor category index. Cost surfaces vary by certificate authority - Let's Encrypt is free; DigiCert and Sectigo bill per certificate per validation level under partner contracts. There is no single FOCUS-aligned billing model for the category; per-vendor finops artifacts should live in vendor-specific repos.\nsources:\n  - https://letsencrypt.org/\n  - https://www.digicert.com/\n  - https://www.sectigo.com/\nnotes: No unified billing surface. FOCUS columns are placeholders; replace with per-vendor entries (Let's Encrypt = $0, DigiCert / Sectigo = per-certificate per-contract).\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Multiple Certificate Authorities\nserviceCategory: Identity\nbillingModel:\n  pricingCategory: Mixed (Free + Per-Certificate)\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: SSL/TLS\n  ServiceCategory: Identity\n  ProviderName: SSL/TLS\n  PublisherName: Multiple\n  InvoiceIssuerName: Per Vendor\n  BillingCurrency: USD\nmeters:\n  - name: certificate_issuance\n    unit: certificate\n    aggregation: count\n    dimensions:\n      - certificate_authority\n      - validation_level\n      - term_length\nprinciples:\n  - name: Visibility\n    description: Inventory issued certificates via each CA's portal or API (DigiCert Services API, Sectigo Cert Manager, Let's Encrypt ACME account orders endpoint). Aggregate into a single CMDB / certificate-lifecycle tool to see total spend across CAs.\n\
  \  - name: Allocation\n    description: Allocate per-certificate cost to the team that owns the hostname. Tag certificates with team/product at issuance; for ACME automation, derive ownership from the requesting service principal.\n  - name: Optimization\n    description: Default to Let's Encrypt for DV use cases (free, fully automated); reserve OV/EV from paid CAs for explicit business-identity requirements. Consolidate wildcard certificates where possible to reduce per-cert charges.\n  - name: Accountability\n    description: PKI / platform-security team owns the CA contracts and renewal cadence; product teams own remediation when their certificates approach expiry or fail validation.\nmaintainers:\n  - name: API Evangelist\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ssl-tls/refs/heads/main/finops/ssl-tls-finops.yml
sources:
- https://letsencrypt.org/
- https://www.digicert.com/
- https://www.sectigo.com/
specification: FinOps Framework
tags:
- SSL/TLS
- TLS
- Certificates
- PKI
- FinOps
- FOCUS
---
