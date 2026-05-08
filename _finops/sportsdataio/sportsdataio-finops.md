---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sportsdataio-nfl-openapi.yml
  format: yaml
  label: SportsDataIO NFL API
  slug: sportsdataio-nfl
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sportsdataio/refs/heads/main/openapi/sportsdataio-nfl-openapi.yml
- filename: sportsdataio-mlb-openapi.yml
  format: yaml
  label: SportsDataIO MLB API
  slug: sportsdataio-mlb
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sportsdataio/refs/heads/main/openapi/sportsdataio-mlb-openapi.yml
- filename: sportsdataio-nba-openapi.yml
  format: yaml
  label: SportsDataIO NBA API
  slug: sportsdataio-nba
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sportsdataio/refs/heads/main/openapi/sportsdataio-nba-openapi.yml
- filename: sportsdataio-nhl-openapi.yml
  format: yaml
  label: SportsDataIO NHL API
  slug: sportsdataio-nhl
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sportsdataio/refs/heads/main/openapi/sportsdataio-nhl-openapi.yml
- filename: sportsdataio-soccer-openapi.yml
  format: yaml
  label: SportsDataIO Soccer API
  slug: sportsdataio-soccer
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sportsdataio/refs/heads/main/openapi/sportsdataio-soccer-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription
description: FOCUS-aligned FinOps for SportsDataIO. Self-serve customers pay a flat monthly Discovery Lab subscription ($99–$149) with a daily call cap; commercial customers pay an annual license that bundles unlimited calls within contracted sport scope.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: SportsDataIO, LLC
  ProviderName: SportsDataIO
  PublisherName: SportsDataIO, LLC
  ServiceCategory: Sports Data
  ServiceName: SportsDataIO
layout: finops
meters:
- aggregation: sum
  description: Discovery Lab monthly subscription seat ($99–$149/month).
  dimensions:
  - tier
  - sport
  name: discovery_lab_subscription
  unit: month
- aggregation: count
  description: Daily API calls consumed against the per-key quota; relevant for Free Trial and Discovery Lab tiers.
  dimensions:
  - sport
  - endpoint
  - key
  name: api_calls_daily
  unit: request
- aggregation: sum
  description: Annual commercial license seat for production use of sport feeds, the Leagues API, or the Global Sports API.
  dimensions:
  - sport
  - use_case
  name: commercial_license
  unit: year
name: Sportsdataio Finops
provider_name: SportsDataIO
provider_slug: sportsdataio
publisher_name: SportsDataIO, LLC
service_category: Sports Data
slug: sportsdataio-finops
source_filename: sportsdataio-finops.yml
source_heading: FinOps Profile
source_url: https://sportsdata.io/developers/api-documentation
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SportsDataIO\nproviderId: sportsdataio\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Sports Data\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for SportsDataIO. Self-serve customers pay a\n  flat monthly Discovery Lab subscription ($99–$149) with a daily call cap;\n  commercial customers pay an annual license that bundles unlimited calls within\n  contracted sport scope.\nsources:\n  - https://sportsdata.io/developers/api-documentation\n  - https://sportsdata.io/developers/getting-started\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SportsDataIO, LLC\nserviceCategory: Sports Data\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: SportsDataIO\n  ServiceCategory: Sports Data\n  ProviderName: SportsDataIO\n  PublisherName: SportsDataIO, LLC\n  InvoiceIssuerName: SportsDataIO, LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: discovery_lab_subscription\n    description: Discovery Lab monthly subscription seat ($99–$149/month).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - sport\n  - name: api_calls_daily\n    description: Daily API calls consumed against the per-key quota; relevant\n      for Free Trial and Discovery Lab tiers.\n    unit: request\n    aggregation: count\n    dimensions:\n      - sport\n      - endpoint\n      - key\n  - name: commercial_license\n    description: Annual commercial license seat for production use of sport\n      feeds, the Leagues API, or the Global Sports API.\n    unit: year\n    aggregation: sum\n    dimensions:\n\
  \      - sport\n      - use_case\nprinciples:\n  - name: Visibility\n    description: Track daily call counts against the Discovery Lab quota in the\n      developer portal; reconcile commercial license utilization through the\n      account team's contract reporting.\n  - name: Allocation\n    description: Allocate cost by sport (each sport feed is licensable\n      separately) and by the consuming product team — fantasy, media, or\n      sportsbook.\n  - name: Optimization\n    description: Respect each endpoint's documented Call Interval to stay within\n      Discovery Lab daily caps; consolidate redundant pulls; move from sport-\n      specific feeds to the Leagues API when coverage breadth justifies the\n      bundle.\n  - name: Accountability\n    description: Sport-feed cost ownership sits with the product owner of each\n      consuming surface (DFS product, sportsbook, scoreboard) since the contract\n      scopes which sports are licensed.\nmaintainers:\n  - FN: API Evangelist\n\
  \    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sportsdataio/refs/heads/main/finops/sportsdataio-finops.yml
sources:
- https://sportsdata.io/developers/api-documentation
- https://sportsdata.io/developers/getting-started
specification: FinOps Framework
tags:
- Sports Data
- FinOps
- FOCUS
---
