---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ncbi-e-utilities-openapi.yml
  format: yaml
  label: NCBI E-Utilities API
  slug: ncbi-e-utilities-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-national-library-of-medicine/refs/heads/main/openapi/ncbi-e-utilities-openapi.yml
- filename: openapi3.docs.yaml
  format: yaml
  label: NCBI Datasets REST API
  slug: ncbi-datasets-api
  spec_type: OpenAPI
  url: https://www.ncbi.nlm.nih.gov/datasets/docs/v2/openapi3/openapi3.docs.yaml
- filename: ncbi-blast-openapi.yml
  format: yaml
  label: NCBI BLAST URL API
  slug: ncbi-blast-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-national-library-of-medicine/refs/heads/main/openapi/ncbi-blast-openapi.yml
- filename: nlm-clinicaltrials-openapi.yml
  format: yaml
  label: ClinicalTrials.gov API
  slug: nlm-clinical-trials-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-national-library-of-medicine/refs/heads/main/openapi/nlm-clinicaltrials-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the United States National Library of Medicine API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: United States National Library of Medicine
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: United States National Library of Medicine
  PublisherName: United States National Library of Medicine
  ServiceCategory: Developer Tools / API
  ServiceName: United States National Library of Medicine
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: United States National Library Of Medicine Finops
provider_name: United States National Library of Medicine
provider_slug: united-states-national-library-of-medicine
publisher_name: United States National Library of Medicine
service_category: API
slug: united-states-national-library-of-medicine-finops
source_filename: united-states-national-library-of-medicine-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: United States National Library of Medicine\nproviderId: united-states-national-library-of-medicine\npublisherName: United States National Library of Medicine\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Federal Government\n  - Biomedical Research\n  - Healthcare\n  - Genomics\n  - Literature\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the United States National Library of Medicine API surface.\n  Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting\n  across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible\
  \ to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: United States National Library of Medicine\n  ServiceCategory: Developer Tools / API\n  ProviderName: United States National Library of Medicine\n  PublisherName: United States National Library of Medicine\n  InvoiceIssuerName: United States National Library of Medicine\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable\
  \ API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: NCBI E-Utilities API\n    baseURL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils\n    tags:\n      - Biomedical\n      - PubMed\n      - Literature\n      - Genomics\n      - Federal Government\n    serviceName: NCBI E-Utilities API\n    serviceCategory: API\n  - name: NCBI Datasets REST API\n    baseURL: https://api.ncbi.nlm.nih.gov/datasets/v2\n    tags:\n      - Genomics\n      - Biological Sequences\n      - Gene Data\n   \
  \   - Federal Government\n    serviceName: NCBI Datasets REST API\n    serviceCategory: API\n  - name: NCBI BLAST URL API\n    baseURL: https://blast.ncbi.nlm.nih.gov/blast/Blast.cgi\n    tags:\n      - Genomics\n      - Sequence Alignment\n      - Bioinformatics\n      - Federal Government\n    serviceName: NCBI BLAST URL API\n    serviceCategory: API\n  - name: ClinicalTrials.gov API\n    baseURL: https://clinicaltrials.gov/api/v2\n    tags:\n      - Clinical Trials\n      - Healthcare\n      - Research\n      - Federal Government\n    serviceName: ClinicalTrials.gov API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/united-states-national-library-of-medicine/refs/heads/main/finops/united-states-national-library-of-medicine-finops.yml
sources: []
specification: FinOps Framework
tags:
- Federal Government
- Biomedical Research
- Healthcare
- Genomics
- Literature
- FinOps
- Cost Management
- FOCUS
---
