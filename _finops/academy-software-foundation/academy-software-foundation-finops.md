---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: academy-software-foundation-opencue.yaml
  format: yaml
  label: OpenCue
  slug: opencue
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/academy-software-foundation/refs/heads/main/openapi/academy-software-foundation-opencue.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Membership / Free Open Source
description: FOCUS-aligned FinOps scaffold for Academy Software Foundation. ASWF projects are free open source libraries; there are no provider invoices to allocate. FinOps relevance is internal — studios track CI/CD compute, storage, and developer time spent on ASWF integrations rather than vendor charges.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: The Linux Foundation
  ProviderName: Academy Software Foundation
  PublisherName: The Linux Foundation
  ServiceCategory: Open Source Software / Standards
  ServiceName: Academy Software Foundation
layout: finops
meters:
- aggregation: sum
  description: Annual Linux Foundation / ASWF membership fee, negotiated by tier.
  dimensions:
  - membership_tier
  name: lf_membership
  unit: year
name: Academy Software Foundation Finops
provider_name: Academy Software Foundation
provider_slug: academy-software-foundation
publisher_name: The Linux Foundation
service_category: Open Source Software / Standards
slug: academy-software-foundation-finops
source_filename: academy-software-foundation-finops.yml
source_heading: FinOps Profile
source_url: https://www.aswf.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Academy Software Foundation\nproviderId: academy-software-foundation\npublisherName: The Linux Foundation\nserviceCategory: Open Source Software / Standards\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Animation\n  - Color Management\n  - Film\n  - Linux Foundation\n  - Open Source\n  - Rendering\n  - Standards\n  - Visual Effects\n  - VFX\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Academy Software Foundation. ASWF projects are free open\n  source libraries; there are no provider invoices to allocate. FinOps relevance is internal — studios\n  track CI/CD compute, storage, and developer\
  \ time spent on ASWF integrations rather than vendor charges.\nsources:\n  - https://www.aswf.io/\n  - https://www.aswf.io/membership/\nnotes: No vendor billing surface. The only direct ASWF cost is Linux Foundation membership (negotiated,\n  not publicly metered). Internal FinOps focus is on the compute and storage costs studios incur when\n  building, testing, and running ASWF-based pipelines — those costs land on the underlying cloud or on-prem\n  provider, not ASWF.\nbillingModel:\n  pricingCategory: Membership / Free Open Source\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Academy Software Foundation\n  ServiceCategory: Open Source Software / Standards\n  ProviderName: Academy Software Foundation\n  PublisherName: The Linux Foundation\n  InvoiceIssuerName: The Linux Foundation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: lf_membership\n    description: Annual Linux Foundation / ASWF\
  \ membership fee, negotiated by tier.\n    unit: year\n    aggregation: sum\n    dimensions:\n      - membership_tier\nprinciples:\n  - name: Visibility\n    description: There is no ASWF invoice to track. Visibility means cataloging which ASWF libraries\n      (OpenEXR, OpenVDB, OpenColorIO, etc.) are linked into internal pipelines, and the build/CI cost\n      of maintaining those integrations.\n  - name: Allocation\n    description: Allocate the compute and storage cost of ASWF-dependent workloads (render farms, color\n      pipelines, image conversion) to the consuming production or studio cost center.\n  - name: Optimization\n    description: Optimize through caching of build artifacts (aswf-docker images), pinning library versions,\n      and choosing the right project for the workload (e.g. OpenImageIO vs custom image code).\n  - name: Accountability\n    description: Studio engineering leadership owns the build/CI cost; the LF membership line, where it\n      exists, is owned by\
  \ studio leadership or a consortium-relations function.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/academy-software-foundation/refs/heads/main/finops/academy-software-foundation-finops.yml
sources:
- https://www.aswf.io/
- https://www.aswf.io/membership/
specification: FinOps Framework
tags:
- Animation
- Color Management
- Film
- Linux Foundation
- Open Source
- Rendering
- Standards
- Visual Effects
- VFX
- FinOps
- FOCUS
---
