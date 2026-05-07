---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: springer-nature-meta-openapi.yml
  format: yaml
  label: Springer Nature Meta API
  slug: springer-nature-meta-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/springer-nature/refs/heads/main/openapi/springer-nature-meta-openapi.yml
- filename: springer-nature-openaccess-openapi.yml
  format: yaml
  label: Springer Nature Open Access API
  slug: springer-nature-openaccess-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/springer-nature/refs/heads/main/openapi/springer-nature-openaccess-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: Springer Nature's developer APIs are sold as a Basic free tier and a Premium subscription tier. Premium pricing and meter definitions are not publicly published; FinOps for the Premium tier is therefore a Contact Sales placeholder until contract terms are available.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Springer Nature
  ProviderName: Springer Nature
  PublisherName: Springer Nature
  ServiceCategory: Content / Publishing
  ServiceName: Springer Nature API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - tier
  name: api_requests
  unit: request
name: Springer Nature Finops
provider_name: Springer Nature
provider_slug: springer-nature
publisher_name: Springer Nature
service_category: Content / Publishing
slug: springer-nature-finops
source_filename: springer-nature-finops.yml
source_heading: FinOps Profile
source_url: https://dev.springernature.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Springer Nature\nproviderId: springer-nature\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Academic Publishing\n  - Open Access\n  - Research\n  - FinOps\n  - FOCUS\ndescription: Springer Nature's developer APIs are sold as a Basic free tier and a Premium subscription tier. Premium pricing and meter definitions are not publicly published; FinOps for the Premium tier is therefore a Contact Sales placeholder until contract terms are available.\nsources:\n  - https://dev.springernature.com/\nnotes: Premium API pricing not publicly disclosed. FOCUS columns and meter unit are placeholders pending a Premium contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Springer Nature\nserviceCategory: Content / Publishing\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Springer Nature API\n  ServiceCategory: Content / Publishing\n  ProviderName: Springer Nature\n  PublisherName: Springer Nature\n  InvoiceIssuerName: Springer Nature\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tier\nprinciples:\n  - name: Visibility\n    description: The dev.springernature.com portal shows daily quota consumption per registered API key; consumers can monitor usage there. The Premium tier presumably exposes richer reporting through the account team but is not publicly documented.\n  - name: Allocation\n    description: Issue one API key per consuming application or research workflow so daily-quota consumption is allocable to the team that owns the key.\n  -\
  \ name: Optimization\n    description: Cache Meta API metadata responses aggressively (publication metadata is stable), batch DOI lookups where the API supports it, and limit Full-Text / TDM calls to documents not already in local repository to avoid re-fetch.\n  - name: Accountability\n    description: Library / research-data team typically owns the Springer Nature API contract and its Premium upgrade decision; consuming research teams accept fair-use limits per key.\nmaintainers:\n  - name: Springer Nature\n    url: https://dev.springernature.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/springer-nature/refs/heads/main/finops/springer-nature-finops.yml
sources:
- https://dev.springernature.com/
specification: FinOps Framework
tags:
- Academic Publishing
- Open Access
- Research
- FinOps
- FOCUS
---
