---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Regulatory Free Access (no fee)
description: 'FOCUS-aligned FinOps for Humana FHIR APIs: regulatory free access (no vendor invoice), cost surface is the consumer''s own infrastructure (request volume, data egress, identity / consent flow, member outreach) rather than per-call API charges from Humana.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (no Humana invoice for API access)
  ProviderName: Humana
  PublisherName: Humana Inc.
  ServiceCategory: Healthcare Interoperability
  ServiceName: Humana FHIR APIs
layout: finops
meters:
- aggregation: sum
  description: Member-authorized FHIR R4 queries against Patient Access endpoints; not billed but tracked for capacity and rate-limit purposes.
  dimensions:
  - resource_type
  - app
  name: patient_access_requests
  unit: request
- aggregation: sum
  description: Public Provider Directory FHIR queries.
  dimensions:
  - resource_type
  - app
  name: provider_directory_requests
  unit: request
- aggregation: sum
  description: Public Drug Formulary FHIR queries.
  dimensions:
  - resource_type
  - app
  name: drug_formulary_requests
  unit: request
- aggregation: sum
  description: SMART on FHIR consent flows initiated and completed; useful for measuring application activation.
  dimensions:
  - app
  name: oauth_member_authorizations
  unit: authorization
- aggregation: sum
  description: PHI / FHIR resource bytes returned; informs the consumer's own storage and processing cost.
  dimensions:
  - resource_type
  - app
  name: data_egress
  unit: GB
name: Humana Finops
provider_name: Humana
provider_slug: humana
publisher_name: Humana Inc.
service_category: Healthcare Interoperability
slug: humana-finops
source_filename: humana-finops.yml
source_heading: FinOps Profile
source_url: https://developers.humana.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Humana\nproviderId: humana\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - FHIR\n  - Healthcare\n  - CMS\ndescription: 'FOCUS-aligned FinOps for Humana FHIR APIs: regulatory free access (no vendor invoice),\n  cost surface is the consumer''s own infrastructure (request volume, data egress, identity / consent\n  flow, member outreach) rather than per-call API charges from Humana.'\nsources:\n  - https://developers.humana.com/\n  - https://www.cms.gov/regulations-and-guidance/guidance/interoperability/index\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Humana Inc.\nserviceCategory: Healthcare Interoperability\nbillingModel:\n\
  \  pricingCategory: Regulatory Free Access (no fee)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Humana FHIR APIs\n  ServiceCategory: Healthcare Interoperability\n  ProviderName: Humana\n  PublisherName: Humana Inc.\n  InvoiceIssuerName: N/A (no Humana invoice for API access)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: patient_access_requests\n    description: Member-authorized FHIR R4 queries against Patient Access endpoints; not billed but\n      tracked for capacity and rate-limit purposes.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - app\n  - name: provider_directory_requests\n    description: Public Provider Directory FHIR queries.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - app\n  - name: drug_formulary_requests\n    description: Public Drug Formulary FHIR queries.\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - resource_type\n      - app\n  - name: oauth_member_authorizations\n    description: SMART on FHIR consent flows initiated and completed; useful for measuring application\n      activation.\n    unit: authorization\n    aggregation: sum\n    dimensions:\n      - app\n  - name: data_egress\n    description: PHI / FHIR resource bytes returned; informs the consumer's own storage and processing\n      cost.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - app\nprinciples:\n  - name: Visibility\n    description: Humana does not invoice for API access. Track request and member-authorization volumes\n      via your application's own logging (token issuance, FHIR request audit). Reconcile against\n      Humana CapabilityStatement and any sandbox vs production rate-limit guidance.\n  - name: Allocation\n    description: Tag FHIR requests with the originating product feature (member portal, claims explorer,\n      care management\
  \ workflow) so that downstream storage and processing cost can be allocated.\n  - name: Optimization\n    description: Use bulk-data ($export) operations where supported to amortize request overhead.\n      Cache reference data (Provider Directory, Drug Formulary) since they do not require member\n      consent. Use _summary and _elements parameters to reduce payload size and downstream egress\n      cost.\n  - name: Accountability\n    description: Even though API access is free, operational risk is real - mishandled member PHI\n      triggers HIPAA exposure. Establish clear data-retention windows and a periodic audit of which\n      member tokens are still active.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/humana/refs/heads/main/finops/humana-finops.yml
sources:
- https://developers.humana.com/
- https://www.cms.gov/regulations-and-guidance/guidance/interoperability/index
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- FHIR
- Healthcare
- CMS
---
