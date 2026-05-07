---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pypi-json-api-openapi.yml
  format: yaml
  label: PyPI JSON API
  slug: json
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/openapi/pypi-json-api-openapi.yml
- filename: pypi-index-api-openapi.yml
  format: yaml
  label: PyPI Index API
  slug: index
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/openapi/pypi-index-api-openapi.yml
- filename: pypi-integrity-api-openapi.yml
  format: yaml
  label: PyPI Integrity API
  slug: integrity
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/openapi/pypi-integrity-api-openapi.yml
- filename: pypi-upload-api-openapi.yml
  format: yaml
  label: PyPI Upload API
  slug: upload
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/openapi/pypi-upload-api-openapi.yml
- filename: pypi-stats-api-openapi.yml
  format: yaml
  label: PyPI Stats API
  slug: stats
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/openapi/pypi-stats-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Free
description: FOCUS-aligned FinOps shape for PyPI. PyPI is operated by the Python Software Foundation as donation-supported public infrastructure — there is no vendor invoice, no metered API, and no commercial tier. Consumer-side cost is purely the consumer's own infrastructure (egress, CI runner time, mirror storage).
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: n/a (donation-supported)
  ProviderName: PyPI
  PublisherName: Python Software Foundation
  ServiceCategory: Package Registry
  ServiceName: PyPI
layout: finops
meters:
- aggregation: sum
  dimensions:
  - package
  - version
  name: package_downloads
  unit: request
- aggregation: sum
  dimensions:
  - mirror
  name: consumer_egress
  unit: GB
name: Pypi Finops
provider_name: PyPI
provider_slug: pypi
publisher_name: Python Software Foundation
service_category: Package Registry
slug: pypi-finops
source_filename: pypi-finops.yml
source_heading: FinOps Profile
source_url: https://pypi.org/help/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PyPI\nproviderId: pypi\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Package Registry\n  - Python\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for PyPI. PyPI is operated by the Python Software Foundation\n  as donation-supported public infrastructure — there is no vendor invoice, no metered API, and no\n  commercial tier. Consumer-side cost is purely the consumer's own infrastructure (egress, CI runner\n  time, mirror storage).\nnotes: PyPI does not bill consumers. The only FinOps-relevant cost is the consumer's own bandwidth /\n  CI / mirror infrastructure. Donations to the PSF are voluntary.\nsources:\n  - https://pypi.org/help/\n  - https://docs.pypi.org/api/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Python Software Foundation\nserviceCategory: Package Registry\nbillingModel:\n  pricingCategory: Free\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: PyPI\n  ServiceCategory: Package Registry\n  ProviderName: PyPI\n  PublisherName: Python Software Foundation\n  InvoiceIssuerName: 'n/a (donation-supported)'\n  BillingCurrency: USD\nmeters:\n  - name: package_downloads\n    unit: request\n    aggregation: sum\n    dimensions:\n      - package\n      - version\n  - name: consumer_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - mirror\nprinciples:\n  - name: Visibility\n    description: PyPI publishes BigQuery / Google Cloud Storage download statistics (`bigquery-public-data.pypi.file_downloads`)\n      so consumers and maintainers can see download patterns; consumer cost is observable in the consumer's\n   \
  \   own cloud / CI bill.\n  - name: Allocation\n    description: Allocate consumer-side cost (egress, CI runtime, mirror storage) by team or product\n      using the consumer's own tagging; PyPI itself has no per-consumer billing surface.\n  - name: Optimization\n    description: Use Fastly's CDN cache headers and ETag conditional requests, pin and cache wheels\n      in a private mirror (devpi, Artifactory, Nexus) to reduce repeat egress, and use lockfiles to\n      avoid unnecessary metadata churn.\n  - name: Accountability\n    description: PyPI has no consumer-side budget owner; the PSF funds operation via donations. Consumer\n      organizations should account for their own mirror and CI cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pypi/refs/heads/main/finops/pypi-finops.yml
sources:
- https://pypi.org/help/
- https://docs.pypi.org/api/
specification: FinOps Framework
tags:
- Package Registry
- Python
- Open Source
- FinOps
- FOCUS
---
