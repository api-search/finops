---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Annual / Per-Device
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Credit
  pricingCategory: Bundled with Device / Service Contract
description: 'FOCUS-aligned FinOps shape for Medtronic: connected medical-device platform where APIs are bundled with device / service contracts. Cost is allocated by program, device line, and reimbursement context rather than per-API-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Medtronic, Inc.
  ProviderName: Medtronic
  PublisherName: Medtronic plc
  ServiceCategory: Medical Devices / Connected Health
  ServiceName: Medtronic Developer Programs
layout: finops
meters:
- aggregation: avg
  description: Devices actively reporting telemetry through Medtronic platforms.
  dimensions:
  - device_line
  - care_setting
  - region
  name: connected_devices
  unit: device-month
- aggregation: avg
  description: Distinct patient records integrated under HIPAA / GDPR-permitted scope.
  dimensions:
  - program
  - region
  name: patient_records
  unit: patient-month
- aggregation: avg
  description: Clinician users active in CareLink / EHR integration consoles.
  dimensions:
  - program
  - care_setting
  name: clinician_seats
  unit: seat-month
- aggregation: sum
  description: Clinical telemetry events ingested (e.g. CGM readings, pacemaker check-ins).
  dimensions:
  - device_line
  - region
  name: telemetry_events
  unit: event
name: Medtronic Finops
provider_name: Medtronic
provider_slug: medtronic
publisher_name: Medtronic plc
service_category: Medical Devices / Connected Health
slug: medtronic-finops
source_filename: medtronic-finops.yml
source_heading: FinOps Profile
source_url: https://developer.medtronic.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Medtronic\nproviderId: medtronic\npublisherName: Medtronic plc\nserviceCategory: Medical Devices / Connected Health\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - Medical Devices\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Medtronic: connected medical-device platform where APIs\n  are bundled with device / service contracts. Cost is allocated by program, device line, and reimbursement\n  context rather than per-API-call billing.'\nnotes: |\n  No public per-API pricing. Meters reflect partner-program economic units (active devices, patient\n  records, clinician seats) rather than\
  \ raw API requests.\nsources:\n  - https://developer.medtronic.com/\n  - https://www.medtronic.com/\nprinciples:\n  - name: Visibility\n    description: Track integration consumption by program (CareLink, diabetes platform, EHR connectivity)\n      via the Medtronic developer portal usage view; reconcile against partner agreements and device\n      service contracts.\n  - name: Allocation\n    description: Allocate by partner program, device line, and care setting (hospital, clinic, home).\n      For payors and ACOs, allocate by attributed patient population.\n  - name: Optimization\n    description: Reduce sync frequency for non-clinically-critical telemetry, cache device metadata, and\n      consolidate integrations per care setting (single connector for cardiac + diabetes where both\n      programs are present).\n  - name: Accountability\n    description: Assign a clinical integration owner per program responsible for compliance with HIPAA /\n      GDPR controls, partner agreement renewals,\
  \ and clinical workflow validation.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Bundled with Device / Service Contract\n  billingFrequency: Annual / Per-Device\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Medtronic Developer Programs\n  ServiceCategory: Medical Devices / Connected Health\n  ProviderName: Medtronic\n  PublisherName: Medtronic plc\n  InvoiceIssuerName: Medtronic, Inc.\n\
  \  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: connected_devices\n    description: Devices actively reporting telemetry through Medtronic platforms.\n    unit: device-month\n    aggregation: avg\n    dimensions:\n      - device_line\n      - care_setting\n      - region\n  - name: patient_records\n    description: Distinct patient records integrated under HIPAA / GDPR-permitted scope.\n    unit: patient-month\n    aggregation: avg\n    dimensions:\n      - program\n      - region\n  - name: clinician_seats\n    description: Clinician users active in CareLink / EHR integration consoles.\n    unit: seat-month\n    aggregation: avg\n    dimensions:\n      - program\n      - care_setting\n  - name: telemetry_events\n    description: Clinical telemetry events ingested (e.g. CGM readings, pacemaker check-ins).\n    unit: event\n    aggregation: sum\n    dimensions:\n      - device_line\n      - region\napis:\n  - name: Medtronic API\n    baseURL: https://api.medtronic.com\n\
  \    tags:\n      - Healthcare\n      - Medical Devices\n    serviceName: Medtronic API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Connected Device\n    metric: program_cost / connected_devices\n    target: TBD\n  - name: Cost per Patient Record\n    metric: program_cost / patient_records\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/medtronic/refs/heads/main/finops/medtronic-finops.yml
sources:
- https://developer.medtronic.com/
- https://www.medtronic.com/
specification: FinOps Framework
tags:
- Healthcare
- Medical Devices
- FinOps
- FOCUS
---
