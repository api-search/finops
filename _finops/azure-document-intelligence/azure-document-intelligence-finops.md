---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: azure-document-intelligence-openapi.json
  format: json
  label: Azure AI Document Intelligence REST API
  slug: rest
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-document-intelligence/refs/heads/main/openapi/azure-document-intelligence-openapi.json
billing_model:
  billingCurrency: USD (varies by Azure billing currency)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage (per-page) + optional Commitment
description: FOCUS-aligned FinOps profile for Azure AI Document Intelligence. Costs are Azure-billed per-page consumption against tier-specific rates (Read, Prebuilt, Custom Classification, Custom Extraction, Add-Ons, Query Fields) plus optional commitment tiers. Standard Azure cost-management plumbing applies — resource group / subscription / tag-based allocation through Azure Cost Management + Microsoft Cost Management exports (FOCUS-native).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft
  PricingUnit: 1K pages
  ProviderName: Microsoft
  PublisherName: Microsoft
  ServiceCategory: AI Services
  ServiceName: Azure AI Document Intelligence
layout: finops
meters:
- aggregation: sum
  description: OCR (Read model) pages.
  dimensions:
  - resource
  - region
  name: read_pages
  unit: page
- aggregation: sum
  description: Prebuilt-model pages (Invoice / Receipt / ID / etc.).
  dimensions:
  - resource
  - model
  name: prebuilt_pages
  unit: page
- aggregation: sum
  description: Custom classification pages.
  dimensions:
  - resource
  - classifier
  name: custom_classification_pages
  unit: page
- aggregation: sum
  description: Custom extraction (and Custom Generative) pages.
  dimensions:
  - resource
  - model
  name: custom_extraction_pages
  unit: page
- aggregation: sum
  description: Add-on capability invocations (High Resolution, Font, Formula).
  dimensions:
  - resource
  - addon
  name: addon_pages
  unit: page
- aggregation: sum
  description: Query Fields requests.
  dimensions:
  - resource
  name: query_field_pages
  unit: page
- aggregation: sum
  description: Custom-model training hours after first 10h free.
  dimensions:
  - resource
  name: training_hours
  unit: hour
- aggregation: sum
  description: Active commitment-tier subscription (custom / prebuilt / read).
  dimensions:
  - resource
  - tier
  name: commitment_tier
  unit: month
name: Azure Document Intelligence Finops
provider_name: Azure AI Document Intelligence
provider_slug: azure-document-intelligence
publisher_name: Microsoft
service_category: AI / IDP
slug: azure-document-intelligence-finops
source_filename: azure-document-intelligence-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/document-intelligence/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure AI Document Intelligence\nproviderId: azure-document-intelligence\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Document AI\n- Azure\n- IDP\n- OCR\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Azure AI Document Intelligence. Costs are\n  Azure-billed per-page consumption against tier-specific rates (Read,\n  Prebuilt, Custom Classification, Custom Extraction, Add-Ons, Query Fields)\n  plus optional commitment tiers. Standard Azure cost-management plumbing\n  applies — resource group / subscription / tag-based allocation through\n  Azure Cost Management + Microsoft Cost Management exports (FOCUS-native).\nnotes: >-\n  Azure publishes a FOCUS-conformant cost export, so allocation by\n  ResourceTag is straightforward. Add-ons and Query Fields are billed on top\n  of the base prebuilt/custom\
  \ rates and easy to overlook.\nsources:\n- https://azure.microsoft.com/en-us/pricing/details/document-intelligence/\n- https://learn.microsoft.com/en-us/azure/cost-management-billing/dataset-schema/cost-usage-details-focus\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft\nserviceCategory: AI / IDP\nbillingModel:\n  pricingCategory: Usage (per-page) + optional Commitment\n  billingFrequency: Monthly\n  billingCurrency: USD (varies by Azure billing currency)\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Azure AI Document Intelligence\n  ServiceCategory: AI Services\n  ProviderName: Microsoft\n  PublisherName: Microsoft\n  InvoiceIssuerName: Microsoft\n  BillingCurrency: USD\n  ChargeCategory: Usage\n\
  \  PricingUnit: 1K pages\nmeters:\n- name: read_pages\n  description: OCR (Read model) pages.\n  unit: page\n  aggregation: sum\n  dimensions:\n  - resource\n  - region\n- name: prebuilt_pages\n  description: Prebuilt-model pages (Invoice / Receipt / ID / etc.).\n  unit: page\n  aggregation: sum\n  dimensions:\n  - resource\n  - model\n- name: custom_classification_pages\n  description: Custom classification pages.\n  unit: page\n  aggregation: sum\n  dimensions:\n  - resource\n  - classifier\n- name: custom_extraction_pages\n  description: Custom extraction (and Custom Generative) pages.\n  unit: page\n  aggregation: sum\n  dimensions:\n  - resource\n  - model\n- name: addon_pages\n  description: Add-on capability invocations (High Resolution, Font, Formula).\n  unit: page\n  aggregation: sum\n  dimensions:\n  - resource\n  - addon\n- name: query_field_pages\n  description: Query Fields requests.\n  unit: page\n  aggregation: sum\n  dimensions:\n  - resource\n- name: training_hours\n\
  \  description: Custom-model training hours after first 10h free.\n  unit: hour\n  aggregation: sum\n  dimensions:\n  - resource\n- name: commitment_tier\n  description: Active commitment-tier subscription (custom / prebuilt / read).\n  unit: month\n  aggregation: sum\n  dimensions:\n  - resource\n  - tier\nprinciples:\n- name: Visibility\n  description: Use Azure Cost Management + FOCUS export; tag resources by app/team.\n- name: Allocation\n  description: Per-resource and per-tag allocation; leverage subscription/RG separation.\n- name: Optimization\n  description: Use commitment tiers above ~20K pages/mo; prefer Read over Prebuilt where layout-only is sufficient; disable unused add-ons; right-size custom-extraction usage.\n- name: Accountability\n  description: Assign cost-center tags; alert on anomalies via Cost Management.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-document-intelligence/refs/heads/main/finops/azure-document-intelligence-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/document-intelligence/
- https://learn.microsoft.com/en-us/azure/cost-management-billing/dataset-schema/cost-usage-details-focus
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Document AI
- Azure
- IDP
- OCR
- FinOps
- Cost Management
- FOCUS
---
