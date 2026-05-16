---
aligned_with: {}
api_specs:
- filename: openapi.json
  format: json
  label: PostalCodes.info Postal Code Reference API
  slug: postal-code-reference-api
  spec_type: OpenAPI
  url: https://postalcodes.info/openapi.json
billing_model: {}
description: ''
focus_columns: {}
layout: finops
meters: []
name: Postalcodes Info Finops
provider_name: PostalCodes.info
provider_slug: postalcodes-info
publisher_name: ''
service_category: ''
slug: postalcodes-info-finops
source_filename: postalcodes-info-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "finopsSpec: '0.1'\nfocusVersion: '1.1'\nprovider:\n  id: postalcodes-info\n  name: PostalCodes.info\n  url: https://postalcodes.info/\n  contact:\n    email: social@genera.work\n    url: https://postalcodes.info/contact\n\nreconciled: false\nreconciliationNotes: |\n  PostalCodes.info has no chargeable billing surface for consumers of the\n  reference API or country datasets. There is no metered SKU, no invoicing\n  surface, no FOCUS-aligned cost data feed, and no public commercial price\n  list to reconcile. The FinOps view below documents the indirect cost shape\n  (consumer-side compute / storage / egress costs for ingesting and caching\n  PostalCodes.info data) and the provider-side operating model, which is\n  funded outside of consumer billing.\n\nbillingSurface:\n  exists: false\n  notes: |\n    The provider does not invoice consumers. Access is governed by ODbL 1.0\n    attribution. There are no chargeable SKUs to map to FOCUS columns such as\n    BilledCost, EffectiveCost,\
  \ ListCost, or CommitmentDiscountStatus.\n\nfocusAlignment:\n  approach: consumer-side-only\n  notes: |\n    Because there is no provider invoice, FOCUS reconciliation is only useful\n    on the consumer side, where teams may capture:\n\n      - BilledCost for storage of downloaded country corpora\n      - BilledCost for compute that ingests / normalizes the data\n      - BilledCost for CDN / egress when re-serving derivative postal data\n      - ServiceCategory: 'Data Integration'\n      - ServiceName: 'PostalCodes.info Reference Data'\n      - ProviderName: 'PostalCodes.info'\n      - PublisherName: 'PostalCodes.info'\n      - InvoiceIssuerName: <consumer's own cloud or data platform>\n      - ChargeCategory: 'Usage' (consumer-side infra), not 'Purchase'\n  focusFieldsApplicable:\n    - ProviderName\n    - PublisherName\n    - ServiceCategory\n    - ServiceName\n    - ChargeCategory\n    - ChargeDescription\n    - PricingUnit\n  focusFieldsNotApplicable:\n    - BilledCost\n    - EffectiveCost\n\
  \    - ListCost\n    - ContractedCost\n    - CommitmentDiscountStatus\n    - CommitmentDiscountType\n    - CommitmentDiscountId\n    - InvoiceIssuerName\n    - PricingCategory\n    - SkuId\n    - SkuPriceId\n\ncostDrivers:\n  - id: ingest-volume\n    name: Country Dataset Ingest Volume\n    description: |\n      Storage and compute costs grow with the number of country datasets\n      ingested. Featured corpora include Portugal (~207k records), UAE (~178k),\n      India (~156k), Japan (~147k), Mexico (~145k). Plan capacity around the\n      annual master snapshot (e.g., 2026.1) plus weekly minor updates.\n    unit: country-dataset\n    direction: consumer-side\n  - id: refresh-cadence\n    name: Refresh Cadence\n    description: |\n      Annual master snapshot + weekly minor refreshes. Cost grows with how\n      aggressively the consumer re-pulls full country files versus diffing.\n    unit: refresh-event\n    direction: consumer-side\n  - id: live-lookup-volume\n    name: Live Lookup\
  \ Volume\n    description: |\n      Per-request compute and egress on the consumer side when calling /search\n      and /ajax-preview from production traffic instead of caching results.\n    unit: request\n    direction: consumer-side\n  - id: egress-redistribution\n    name: Egress for Redistribution\n    description: |\n      If the consumer re-serves derivative postal data, egress and CDN costs\n      apply. ODbL attribution is required on derivatives.\n    unit: GB-egressed\n    direction: consumer-side\n\nproviderOperatingModel:\n  funding: |\n    PostalCodes.info is funded by the maintainer (Pablo Cirre / PostalCodes.info)\n    and infrastructure partners. Stated infrastructure: Oracle Cloud hosting;\n    GeoNames as upstream data source. No consumer billing is in scope.\n  hostingPartner: Oracle Cloud\n  upstreamData: GeoNames\n\nrecommendations:\n  - 'Cache country downloads by snapshot version (e.g., 2026.1) to avoid redundant transfer cost.'\n  - 'Prefer bulk /download.php over\
  \ repeated /search calls for high-volume ingest.'\n  - 'Diff against the prior snapshot when possible; weekly minor updates are usually small.'\n  - 'Tag consumer-side cloud spend with ServiceName=PostalCodes.info Reference Data for FinOps visibility.'\n\nreferences:\n  - type: License\n    url: https://postalcodes.info/licensing\n  - type: UpdatePolicy\n    url: https://postalcodes.info/update-policy\n  - type: DataSources\n    url: https://postalcodes.info/data-sources\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/postalcodes-info/refs/heads/main/finops/postalcodes-info-finops.yml
sources: []
specification: ''
tags:
- Postal Codes
- Geocoding
- Open Data
- Address Validation
- Logistics
---
