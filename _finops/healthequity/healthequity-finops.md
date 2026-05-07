---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for HealthEquity: employer / benefits-admin partner integration bundled into the broader benefits administration contract. Meters describe enrollment-driven volumes and contribution events used for capacity allocation.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: HealthEquity, Inc.
  PricingCategory: Subscription
  PricingUnit: partner-agreement
  ProviderName: HealthEquity
  PublisherName: HealthEquity, Inc.
  ServiceCategory: Healthcare Benefits / HSA Custodian Partner API
  ServiceName: HealthEquity API
layout: finops
meters:
- aggregation: sum
  description: Partner-integration request volume (allocation meter)
  dimensions:
  - partner
  - employer
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Member enrollment events processed via the API
  dimensions:
  - employer
  - benefit_type
  name: enrollments_processed
  unit: enrollment
- aggregation: sum
  description: Contribution / payroll files processed
  dimensions:
  - employer
  - benefit_type
  name: contribution_files
  unit: file
name: Healthequity Finops
provider_name: HealthEquity
provider_slug: healthequity
publisher_name: HealthEquity, Inc.
service_category: Healthcare Benefits / HSA Custodian Partner API
slug: healthequity-finops
source_filename: healthequity-finops.yml
source_heading: FinOps Profile
source_url: https://www.healthequity.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: HealthEquity\nproviderId: healthequity\npublisherName: HealthEquity, Inc.\nserviceCategory: Healthcare Benefits / HSA Custodian Partner API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - HSA\n  - Benefits\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for HealthEquity: employer / benefits-admin partner\n  integration bundled into the broader benefits administration contract. Meters describe\n  enrollment-driven volumes and contribution events used for capacity allocation.'\nnotes: No public commercial model is published for the API. Reconcile against the partner\
  \ / employer\n  agreement.\nsources:\n  - https://www.healthequity.com/\nprinciples:\n  - name: Visibility\n    description: Track API request volume via the HealthEquity partner gateway logs; correlate with\n      enrollment events and contribution cycles.\n  - name: Allocation\n    description: Allocate integration cost across employer clients and benefit programs (HSA / FSA\n      / HRA / commuter) using the calling partner identifier.\n  - name: Optimization\n    description: Batch enrollment uploads and contribution files; cache employer / plan reference\n      data; pre-warm capacity ahead of open enrollment.\n  - name: Accountability\n    description: Designate a HealthEquity integration owner per partner; review API utilization at\n      year-end with attention to open-enrollment surges.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business\
  \ Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: HealthEquity API\n  ServiceCategory: Healthcare Benefits / HSA Custodian Partner API\n  ProviderName: HealthEquity\n  PublisherName: HealthEquity, Inc.\n  InvoiceIssuerName: HealthEquity, Inc.\n\
  \  PricingCategory: Subscription\n  PricingUnit: partner-agreement\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_requests\n    description: Partner-integration request volume (allocation meter)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - employer\n      - endpoint\n  - name: enrollments_processed\n    description: Member enrollment events processed via the API\n    unit: enrollment\n    aggregation: sum\n    dimensions:\n      - employer\n      - benefit_type\n  - name: contribution_files\n    description: Contribution / payroll files processed\n    unit: file\n    aggregation: sum\n    dimensions:\n      - employer\n      - benefit_type\napis:\n  - name: HealthEquity API\n    baseURL: https://api.healthequity.com\n    tags:\n      - Healthcare\n      - HSA\n      - Benefits\n    serviceName: HealthEquity API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Enrollment Processed\n    metric: billed_cost /\
  \ enrollments_processed\n    target: TBD\n  - name: Cost per Employer Client\n    metric: billed_cost / active_employers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/healthequity/refs/heads/main/finops/healthequity-finops.yml
sources:
- https://www.healthequity.com/
specification: FinOps Framework
tags:
- Healthcare
- HSA
- Benefits
- FinOps
- Cost Management
- FOCUS
---
