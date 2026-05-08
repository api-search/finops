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
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Cloudmersive: flat monthly subscription tiers (Basic through Business Advantage) with included call quotas plus enterprise / on-premises options for committed throughput.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cloudmersive
  PricingCategory: Tiered Subscription
  PricingUnit: subscription-month
  ProviderName: Cloudmersive
  PublisherName: Cloudmersive
  ServiceCategory: Developer Tools / API
  ServiceName: Cloudmersive
layout: finops
meters:
- aggregation: sum
  description: Flat monthly subscription fee for the active plan tier.
  dimensions:
  - plan
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Count of API calls consumed against the plan's monthly allowance.
  dimensions:
  - plan
  - product
  - api_key
  name: api_calls
  unit: request
- aggregation: max
  description: Peak concurrent requests per second observed against the API key.
  dimensions:
  - plan
  - api_key
  name: concurrency_peak
  unit: request
name: Cloudmersive Finops
provider_name: Cloudmersive
provider_slug: cloudmersive
publisher_name: Cloudmersive
service_category: Developer Tools / API
slug: cloudmersive-finops
source_filename: cloudmersive-finops.yml
source_heading: FinOps Profile
source_url: https://www.cloudmersive.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cloudmersive\nproviderId: cloudmersive\npublisherName: Cloudmersive\nserviceCategory: 'Developer Tools / API'\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Documents\n  - Conversions\n  - OCR\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Cloudmersive: flat monthly subscription tiers (Basic through Business\n  Advantage) with included call quotas plus enterprise / on-premises options for committed throughput.'\nsources:\n  - https://www.cloudmersive.com/pricing\n  - https://www.cloudmersive.com/pricing-small-business\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Cloudmersive\n  ServiceCategory: 'Developer Tools / API'\n  ProviderName: Cloudmersive\n  PublisherName: Cloudmersive\n  InvoiceIssuerName: Cloudmersive\n  PricingCategory: Tiered Subscription\n  PricingUnit: subscription-month\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_fee\n    description: Flat monthly subscription fee for the active plan tier.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: api_calls\n    description: Count of API calls consumed against the plan's monthly allowance.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - plan\n      - product\n      - api_key\n  - name: concurrency_peak\n    description: Peak concurrent requests per second observed against the API key.\n    unit: request\n    aggregation: max\n    dimensions:\n      - plan\n\
  \      - api_key\nprinciples:\n  - name: Visibility\n    description: Monitor monthly call counts via the Cloudmersive customer portal; alert before exhausting\n      the plan quota since calls in excess queue rather than fail fast.\n  - name: Allocation\n    description: Issue separate API keys per environment and per consuming application so call counts can\n      be attributed to a team or product.\n  - name: Optimization\n    description: Right-size the plan against observed monthly volume and concurrency. For sustained traffic\n      above 4 calls/second, evaluate single-tenant cloud or on-premises deployment instead of stacking small-business\n      plans.\n  - name: Accountability\n    description: Tie subscription renewals to the engineering team consuming the API; review quota burn-down\n      mid-cycle and escalate to a higher tier before the queue depth materially impacts SLAs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudmersive/refs/heads/main/finops/cloudmersive-finops.yml
sources:
- https://www.cloudmersive.com/pricing
- https://www.cloudmersive.com/pricing-small-business
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Documents
- Conversions
- OCR
- Cost Management
---
