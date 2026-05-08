---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: virus
  format: yaml
  label: Cloudmersive Virus Scan API
  slug: cloudmersive-virus-scan-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/virus
- filename: security
  format: yaml
  label: Cloudmersive Security Threat Detection API
  slug: cloudmersive-security-threat-detection-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/security
- filename: spam
  format: yaml
  label: Cloudmersive Spam Detection API
  slug: cloudmersive-spam-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/spam
- filename: phishing
  format: yaml
  label: Cloudmersive Phishing Detection API
  slug: cloudmersive-phishing-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/phishing
- filename: cdr
  format: yaml
  label: Cloudmersive Content Disarm and Reconstruction (CDR) API
  slug: cloudmersive-cdr-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/cdr
- filename: fraud
  format: yaml
  label: Cloudmersive Fraud Detection API
  slug: cloudmersive-fraud-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/fraud
- filename: dlp
  format: yaml
  label: Cloudmersive Data Loss Prevention (DLP) API
  slug: cloudmersive-dlp-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/dlp
- filename: convert
  format: yaml
  label: Cloudmersive Document Convert API
  slug: cloudmersive-convert-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/convert
- filename: barcode
  format: yaml
  label: Cloudmersive Barcode API
  slug: cloudmersive-barcode-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/barcode
- filename: image
  format: yaml
  label: Cloudmersive Image Recognition and Processing API
  slug: cloudmersive-image-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/image
- filename: nlp
  format: yaml
  label: Cloudmersive Natural Language Processing API
  slug: cloudmersive-nlp-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/nlp
- filename: ocr
  format: yaml
  label: Cloudmersive OCR API
  slug: cloudmersive-ocr-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/ocr
- filename: speech
  format: yaml
  label: Cloudmersive Speech API
  slug: cloudmersive-speech-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/speech
- filename: validate
  format: yaml
  label: Cloudmersive Validate API
  slug: cloudmersive-validate-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/validate
- filename: video
  format: yaml
  label: Cloudmersive Video API
  slug: cloudmersive-video-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/video
- filename: currency
  format: yaml
  label: Cloudmersive Currency API
  slug: cloudmersive-currency-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/currency
- filename: config
  format: yaml
  label: Cloudmersive Configuration API
  slug: cloudmersive-config-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/config
- filename: dataintegration
  format: yaml
  label: Cloudmersive Data Integration API
  slug: cloudmersive-data-integration-api
  spec_type: OpenAPI
  url: https://api-console.cloudmersive.com/swagger/api/dataintegration
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
description: FinOps framework definition for the Cloudmersive API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cloudmersive
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cloudmersive
  PublisherName: Cloudmersive
  ServiceCategory: Developer Tools / API
  ServiceName: Cloudmersive
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
name: Cloudmersive Finops
provider_name: Cloudmersive
provider_slug: cloudmersive
publisher_name: Cloudmersive
service_category: API
slug: cloudmersive-finops
source_filename: cloudmersive-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cloudmersive\nproviderId: cloudmersive\npublisherName: Cloudmersive\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Barcodes\n  - Conversions\n  - Documents\n  - Image Recognition\n  - Natural Language\n  - OCR\n  - Processing\n  - Validation\n  - Virus Scanning\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cloudmersive API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cloudmersive\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cloudmersive\n  PublisherName: Cloudmersive\n  InvoiceIssuerName: Cloudmersive\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cloudmersive Virus Scan API\n    baseURL: ''\n    tags:\n      - Antivirus\n      - Malware\n      - Security\n      - Virus Scanning\n    serviceName: Cloudmersive Virus Scan API\n    serviceCategory: API\n  - name: Cloudmersive Security Threat Detection API\n    baseURL: ''\n    tags:\n      - Security\n      - SQL Injection\n      - Threat Detection\n      - XSS\n    serviceName: Cloudmersive Security Threat Detection API\n    serviceCategory: API\n  - name: Cloudmersive Spam Detection API\n    baseURL: ''\n    tags:\n      - Email\n      - Spam\n    serviceName: Cloudmersive Spam Detection API\n    serviceCategory:\
  \ API\n  - name: Cloudmersive Phishing Detection API\n    baseURL: ''\n    tags:\n      - Email Security\n      - Phishing\n    serviceName: Cloudmersive Phishing Detection API\n    serviceCategory: API\n  - name: Cloudmersive Content Disarm and Reconstruction (CDR) API\n    baseURL: ''\n    tags:\n      - CDR\n      - Document Sanitization\n      - Security\n    serviceName: Cloudmersive Content Disarm and Reconstruction (CDR) API\n    serviceCategory: API\n  - name: Cloudmersive Fraud Detection API\n    baseURL: ''\n    tags:\n      - Fraud Detection\n      - Risk\n    serviceName: Cloudmersive Fraud Detection API\n    serviceCategory: API\n  - name: Cloudmersive Data Loss Prevention (DLP) API\n    baseURL: ''\n    tags:\n      - Compliance\n      - DLP\n      - PII\n    serviceName: Cloudmersive Data Loss Prevention (DLP) API\n    serviceCategory: API\n  - name: Cloudmersive Document Convert API\n    baseURL: ''\n    tags:\n      - Conversion\n      - Documents\n      - File Formats\n\
  \    serviceName: Cloudmersive Document Convert API\n    serviceCategory: API\n  - name: Cloudmersive Barcode API\n    baseURL: ''\n    tags:\n      - Barcode\n      - QR Code\n    serviceName: Cloudmersive Barcode API\n    serviceCategory: API\n  - name: Cloudmersive Image Recognition and Processing API\n    baseURL: ''\n    tags:\n      - Computer Vision\n      - Image Processing\n      - Image Recognition\n    serviceName: Cloudmersive Image Recognition and Processing API\n    serviceCategory: API\n  - name: Cloudmersive Natural Language Processing API\n    baseURL: ''\n    tags:\n      - NLP\n      - Sentiment Analysis\n      - Translation\n    serviceName: Cloudmersive Natural Language Processing API\n    serviceCategory: API\n  - name: Cloudmersive OCR API\n    baseURL: ''\n    tags:\n      - Documents\n      - OCR\n    serviceName: Cloudmersive OCR API\n    serviceCategory: API\n  - name: Cloudmersive Speech API\n    baseURL: ''\n    tags:\n      - Speech\n      - Speech Recognition\n\
  \      - Text to Speech\n    serviceName: Cloudmersive Speech API\n    serviceCategory: API\n  - name: Cloudmersive Validate API\n    baseURL: ''\n    tags:\n      - Email\n      - Validation\n    serviceName: Cloudmersive Validate API\n    serviceCategory: API\n  - name: Cloudmersive Video API\n    baseURL: ''\n    tags:\n      - Conversion\n      - Video\n    serviceName: Cloudmersive Video API\n    serviceCategory: API\n  - name: Cloudmersive Currency API\n    baseURL: ''\n    tags:\n      - Currency\n      - Exchange Rate\n    serviceName: Cloudmersive Currency API\n    serviceCategory: API\n  - name: Cloudmersive Configuration API\n    baseURL: ''\n    tags:\n      - Configuration\n      - Feature Flags\n    serviceName: Cloudmersive Configuration API\n    serviceCategory: API\n  - name: Cloudmersive Data Integration API\n    baseURL: ''\n    tags:\n      - Data Integration\n      - ETL\n    serviceName: Cloudmersive Data Integration API\n    serviceCategory: API\nunitEconomics:\n\
  \  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudmersive/refs/heads/main/finops/cloudmersive-finops.yml
sources: []
specification: FinOps Framework
tags:
- Barcodes
- Conversions
- Documents
- Image Recognition
- Natural Language
- OCR
- Processing
- Validation
- Virus Scanning
- FinOps
- Cost Management
- FOCUS
---
