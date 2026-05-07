---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rekor-openapi.yaml
  format: yaml
  label: Rekor Transparency Log API
  slug: rekor
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/openapi/rekor-openapi.yaml
- filename: fulcio-openapi.json
  format: json
  label: Fulcio Certificate Authority API
  slug: fulcio
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/openapi/fulcio-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories: []
  pricingCategory: Free Public Good (self-hosting infra cost only)
description: FOCUS-aligned FinOps for Sigstore. The public-good service is free and emits no invoice; the only FinOps-relevant cost surface is the infrastructure spend incurred when an organization self-hosts Fulcio/Rekor or contracts a vendor to operate a dedicated Sigstore instance.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Linux Foundation / OpenSSF
  ProviderName: Sigstore
  PublisherName: Linux Foundation / OpenSSF
  ServiceCategory: Software Supply Chain Security
  ServiceName: Sigstore
layout: finops
meters:
- aggregation: sum
  description: Sigstore signing operations performed; not billed by Sigstore but useful as a sizing meter for self-hosted Fulcio capacity planning.
  dimensions:
  - identity_provider
  - workflow
  name: signing_events
  unit: signing-event
- aggregation: sum
  description: Transparency log entries written to Rekor; relevant for self-hosted storage sizing.
  dimensions:
  - log
  name: rekor_log_entries
  unit: entry
name: Sigstore Finops
provider_name: Sigstore
provider_slug: sigstore
publisher_name: Linux Foundation / Open Source Security Foundation (OpenSSF)
service_category: Software Supply Chain Security
slug: sigstore-finops
source_filename: sigstore-finops.yml
source_heading: FinOps Profile
source_url: https://docs.sigstore.dev/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sigstore\nproviderId: sigstore\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Code Signing\n  - Security\n  - Open Source\n  - Public Good\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Sigstore. The public-good service is free and emits no invoice;\n  the only FinOps-relevant cost surface is the infrastructure spend incurred when an organization\n  self-hosts Fulcio/Rekor or contracts a vendor to operate a dedicated Sigstore instance.\nsources:\n  - https://docs.sigstore.dev/\n  - https://www.sigstore.dev/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Linux Foundation / Open Source Security Foundation (OpenSSF)\nserviceCategory: Software\
  \ Supply Chain Security\nbillingModel:\n  pricingCategory: Free Public Good (self-hosting infra cost only)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Sigstore\n  ServiceCategory: Software Supply Chain Security\n  ProviderName: Sigstore\n  PublisherName: Linux Foundation / OpenSSF\n  InvoiceIssuerName: Linux Foundation / OpenSSF\n  BillingCurrency: USD\nmeters:\n  - name: signing_events\n    description: Sigstore signing operations performed; not billed by Sigstore but useful as a sizing\n      meter for self-hosted Fulcio capacity planning.\n    unit: signing-event\n    aggregation: sum\n    dimensions:\n      - identity_provider\n      - workflow\n  - name: rekor_log_entries\n    description: Transparency log entries written to Rekor; relevant for self-hosted storage sizing.\n    unit: entry\n    aggregation: sum\n    dimensions:\n      - log\nprinciples:\n  - name: Visibility\n    description: For consumers of the public-good\
  \ service there is no spend to track. For self-hosters,\n      visibility comes from the underlying cloud/Kubernetes telemetry of the Fulcio and Rekor deployments.\n  - name: Allocation\n    description: Self-hosted Sigstore cost is allocated to the platform/security team that operates\n      it, with chargeback to consuming teams optional and typically not enforced.\n  - name: Optimization\n    description: Use the public-good service for low-volume signing where appropriate. For high-volume\n      workloads, run a private Fulcio/Rekor and right-size Rekor storage retention rather than over-provisioning\n      the public good.\n  - name: Accountability\n    description: Platform security or supply-chain owners are accountable for self-hosted Sigstore\n      infrastructure; consuming teams are accountable for ensuring their CI signs artifacts correctly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sigstore/refs/heads/main/finops/sigstore-finops.yml
sources:
- https://docs.sigstore.dev/
- https://www.sigstore.dev/
specification: FinOps Framework
tags:
- Code Signing
- Security
- Open Source
- Public Good
- FinOps
- FOCUS
---
