---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-ses-openapi.yml
  format: yaml
  label: Amazon SES OpenAPI
  slug: amazon-ses-openapi
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-ses/refs/heads/main/openapi/amazon-ses-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Amazon SES: per-1,000-message rates for outbound and inbound mail, per-GB attachment fees, monthly Dedicated IP charges (Standard or Managed with tiered per-message), and a 12-month 3,000-message-per-month Free Tier.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: Networking and Content Delivery
  ServiceName: Amazon Simple Email Service
  ServiceSubcategory: Email
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - configuration_set
  - sending_identity
  name: outbound_messages
  unit: email
- aggregation: sum
  dimensions:
  - region
  - configuration_set
  name: outbound_attachment_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - rule_set
  - recipient_domain
  name: inbound_messages
  unit: email
- aggregation: sum
  dimensions:
  - region
  - rule_set
  name: inbound_chunks
  unit: chunk
- aggregation: sum
  dimensions:
  - region
  - ip_pool_type
  name: dedicated_ip_months
  unit: ip-month
- aggregation: sum
  dimensions:
  - region
  name: vdm_processed_messages
  unit: email
name: Amazon Ses Finops
provider_name: Amazon SES
provider_slug: amazon-ses
publisher_name: Amazon Web Services, Inc.
service_category: Communication / Email
slug: amazon-ses-finops
source_filename: amazon-ses-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/ses/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon SES\nproviderId: amazon-ses\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - Email\n  - SES\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon SES: per-1,000-message rates for outbound and inbound mail,\n  per-GB attachment fees, monthly Dedicated IP charges (Standard or Managed with tiered per-message),\n  and a 12-month 3,000-message-per-month Free Tier.'\nsources:\n  - https://aws.amazon.com/ses/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Communication / Email\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Amazon Simple Email Service\n  ServiceCategory: Networking and Content Delivery\n  ServiceSubcategory: Email\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: outbound_messages\n    unit: email\n    aggregation: sum\n    dimensions:\n      - region\n      - configuration_set\n      - sending_identity\n  - name: outbound_attachment_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - configuration_set\n  - name: inbound_messages\n    unit: email\n    aggregation: sum\n    dimensions:\n      - region\n      - rule_set\n      - recipient_domain\n  - name: inbound_chunks\n    unit: chunk\n    aggregation: sum\n    dimensions:\n      - region\n      - rule_set\n  - name: dedicated_ip_months\n\
  \    unit: ip-month\n    aggregation: sum\n    dimensions:\n      - region\n      - ip_pool_type\n  - name: vdm_processed_messages\n    unit: email\n    aggregation: sum\n    dimensions:\n      - region\nprinciples:\n  - name: Visibility\n    description: Use SES sending statistics, CloudWatch SES metrics (Send, Bounce, Complaint, Reject),\n      and CUR / FOCUS export for per-configuration-set cost.\n  - name: Allocation\n    description: Tag configuration sets with Application, Channel, Team; set X-SES-CONFIGURATION-SET on\n      sends; enable cost allocation tags.\n  - name: Optimization\n    description: Use Managed Dedicated IPs to consolidate the IP fee and benefit from tiered per-message\n      pricing at scale; suppress invalid recipients; reduce attachment size; use VDM only on streams that\n      need deliverability insights.\n  - name: Accountability\n    description: Set AWS Budgets per configuration-set tag, alert on bounce/complaint rate (which can pause\n      sending),\
  \ and review monthly IP-pool utilization.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Amazon Web Services\n    email: support@aws.amazon.com\n    url: https://aws.amazon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-ses/refs/heads/main/finops/amazon-ses-finops.yml
sources:
- https://aws.amazon.com/ses/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Email
- SES
- Cost Management
---
