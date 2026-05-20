---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: labvantage-lims-openapi.yml
  format: yaml
  label: LabVantage LIMS API
  slug: labvantage-lims-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/labvantage/refs/heads/main/openapi/labvantage-lims-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Enterprise License (Perpetual or Subscription)
description: 'FOCUS-aligned FinOps for LabVantage: enterprise-licensed LIMS/ELN/LES/SDMS platform with no per-API metering. Cost is dominated by the negotiated platform license plus the underlying compute for the customer''s own deployment. FinOps signal therefore covers license utilization (named users, sites, modules) and infrastructure cost separately.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: LabVantage Solutions, Inc.
  ProviderName: LabVantage
  PublisherName: LabVantage Solutions, Inc.
  ServiceCategory: Laboratory Informatics / LIMS
  ServiceName: LabVantage Platform
layout: finops
meters:
- aggregation: max
  dimensions:
  - module
  - site
  name: named_users
  unit: seat
- aggregation: max
  dimensions:
  - module
  name: concurrent_users
  unit: session
- aggregation: max
  dimensions:
  - site
  name: instrument_integrations
  unit: instrument
- aggregation: sum
  dimensions:
  - protocol
  - module
  - site
  name: api_requests
  unit: request
- aggregation: max
  dimensions:
  - module
  name: storage_consumed
  unit: GB
name: Labvantage Finops
provider_name: LabVantage Solutions
provider_slug: labvantage
publisher_name: LabVantage Solutions, Inc.
service_category: Laboratory Informatics / LIMS
slug: labvantage-finops
source_filename: labvantage-finops.yml
source_heading: FinOps Profile
source_url: https://www.labvantage.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LabVantage\nproviderId: labvantage\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - LIMS\n  - Laboratory\n  - Pharma\ndescription: 'FOCUS-aligned FinOps for LabVantage: enterprise-licensed LIMS/ELN/LES/SDMS platform with\n  no per-API metering. Cost is dominated by the negotiated platform license plus the underlying compute\n  for the customer''s own deployment. FinOps signal therefore covers license utilization (named users,\n  sites, modules) and infrastructure cost separately.'\nsources:\n  - https://www.labvantage.com/\nnotes: No public unit pricing for the API surface. License terms (perpetual + maintenance vs subscription)\n  are quoted per customer.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: LabVantage Solutions, Inc.\nserviceCategory: Laboratory Informatics / LIMS\nbillingModel:\n  pricingCategory: Enterprise License (Perpetual or Subscription)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: LabVantage Platform\n  ServiceCategory: Laboratory Informatics / LIMS\n  ProviderName: LabVantage\n  PublisherName: LabVantage Solutions, Inc.\n  InvoiceIssuerName: LabVantage Solutions, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: named_users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - module\n      - site\n  - name: concurrent_users\n    unit: session\n    aggregation: max\n    dimensions:\n      - module\n  - name: instrument_integrations\n    unit: instrument\n    aggregation: max\n    dimensions:\n      - site\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - protocol\n      - module\n      - site\n  - name: storage_consumed\n    unit: GB\n    aggregation: max\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n    description: Capture seat utilization and integration counts per module against contracted entitlements;\n      monitor underlying infrastructure cost (compute, DB, storage) for the deployment.\n  - name: Allocation\n    description: Allocate license cost per site / lab / project; pair the license bill with the infra\n      bill so total cost-of-ownership is visible to the lab informatics team.\n  - name: Optimization\n    description: Reclaim inactive named-user seats; consolidate test instances; right-size the application\n      server tier; archive aged study/sample data to lower-tier storage.\n  - name: Accountability\n    description: Lab informatics or QA owns the LabVantage agreement and module roster; reviews user\n      entitlements quarterly ahead of renewal.\nmaintainers:\n  - FN: Kin Lane\n \
  \   email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/labvantage/refs/heads/main/finops/labvantage-finops.yml
sources:
- https://www.labvantage.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- LIMS
- Laboratory
- Pharma
---
