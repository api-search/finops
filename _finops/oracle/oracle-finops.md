---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Oracle Cloud Infrastructure REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en-us/iaas/api/
- filename: oci-compute-api-openapi.yml
  format: yaml
  label: OCI Compute API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle/refs/heads/main/openapi/oci-compute-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Oracle API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle
  PublisherName: Oracle
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Oracle Finops
provider_name: Oracle
provider_slug: oracle
publisher_name: Oracle
service_category: API
slug: oracle-finops
source_filename: oracle-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle\nproviderId: oracle\npublisherName: Oracle\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Database\n  - Enterprise\n  - Infrastructure\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle\n  PublisherName: Oracle\n  InvoiceIssuerName: Oracle\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n     \
  \ - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle Cloud Infrastructure REST API\n    baseURL: https://iaas.{region}.oraclecloud.com\n    tags:\n      - Cloud\n      - IaaS\n      - Infrastructure\n    serviceName: Oracle Cloud Infrastructure REST API\n    serviceCategory: API\n  - name: Oracle Database REST APIs\n    baseURL: https://{host}:{port}/ords/\n    tags:\n      - Database\n      - ORDS\n      - SQL\n    serviceName: Oracle Database REST APIs\n    serviceCategory: API\n  - name: Oracle Integration Cloud API\n    baseURL: https://{instance}.integration.ocp.oraclecloud.com\n    tags:\n      - Cloud\n      - Integration\n      - iPaaS\n    serviceName: Oracle Integration Cloud API\n    serviceCategory: API\n  - name: Oracle Fusion Cloud Applications API\n    baseURL: https://{instance}.oraclecloud.com\n\
  \    tags:\n      - CX\n      - ERP\n      - HCM\n      - SaaS\n    serviceName: Oracle Fusion Cloud Applications API\n    serviceCategory: API\n  - name: Oracle Fusion Cloud Financials REST API\n    baseURL: https://{instance}.fa.{region}.oraclecloud.com\n    tags:\n      - Accounting\n      - ERP\n      - Financials\n      - SaaS\n    serviceName: Oracle Fusion Cloud Financials REST API\n    serviceCategory: API\n  - name: Oracle Fusion Cloud HCM REST API\n    baseURL: https://{instance}.fa.{region}.oraclecloud.com/hcmRestApi\n    tags:\n      - HCM\n      - Human Resources\n      - Payroll\n      - SaaS\n    serviceName: Oracle Fusion Cloud HCM REST API\n    serviceCategory: API\n  - name: Oracle Fusion Cloud CX Sales and Service REST API\n    baseURL: https://{instance}.fa.{region}.oraclecloud.com/crmRestApi\n    tags:\n      - CX\n      - SaaS\n      - Sales\n    serviceName: Oracle Fusion Cloud CX Sales and Service REST API\n    serviceCategory: API\n  - name: Oracle Fusion Cloud\
  \ SCM REST API\n    baseURL: https://{instance}.fa.{region}.oraclecloud.com/fscmRestApi\n    tags:\n      - Manufacturing\n      - SaaS\n      - SCM\n      - Supply Chain\n    serviceName: Oracle Fusion Cloud SCM REST API\n    serviceCategory: API\n  - name: Oracle Fusion Cloud Procurement REST API\n    baseURL: https://{instance}.fa.{region}.oraclecloud.com/fscmRestApi\n    tags:\n      - Procurement\n      - Purchasing\n      - SaaS\n    serviceName: Oracle Fusion Cloud Procurement REST API\n    serviceCategory: API\n  - name: Oracle Content Management API\n    baseURL: https://{instance}.ocecdn.oraclecloud.com\n    tags:\n      - CMS\n      - Content Management\n      - Digital Assets\n    serviceName: Oracle Content Management API\n    serviceCategory: API\n  - name: OCI Generative AI API\n    baseURL: https://generativeai.{region}.oci.oraclecloud.com\n    tags:\n      - Artificial Intelligence\n      - Generative AI\n      - LLM\n      - Machine Learning\n    serviceName: OCI Generative\
  \ AI API\n    serviceCategory: API\n  - name: OCI AI Vision API\n    baseURL: https://vision.aiservice.{region}.oci.oraclecloud.com\n    tags:\n      - Artificial Intelligence\n      - Computer Vision\n      - Document AI\n      - Image Analysis\n    serviceName: OCI AI Vision API\n    serviceCategory: API\n  - name: OCI AI Language API\n    baseURL: https://language.aiservice.{region}.oci.oraclecloud.com\n    tags:\n      - Artificial Intelligence\n      - Natural Language Processing\n      - Sentiment Analysis\n      - Text Analysis\n    serviceName: OCI AI Language API\n    serviceCategory: API\n  - name: OCI AI Speech API\n    baseURL: https://speech.aiservice.{region}.oci.oraclecloud.com\n    tags:\n      - Artificial Intelligence\n      - Speech Recognition\n      - Text to Speech\n      - Transcription\n    serviceName: OCI AI Speech API\n    serviceCategory: API\n  - name: OCI API Gateway\n    baseURL: https://apigateway.{region}.oci.oraclecloud.com\n    tags:\n      - API Management\n\
  \      - Cloud\n      - Gateway\n    serviceName: OCI API Gateway\n    serviceCategory: API\n  - name: OCI Container Engine for Kubernetes API\n    baseURL: https://containerengine.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud Native\n      - Containers\n      - Kubernetes\n      - Orchestration\n    serviceName: OCI Container Engine for Kubernetes API\n    serviceCategory: API\n  - name: OCI Functions API\n    baseURL: https://functions.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud Native\n      - FaaS\n      - Functions\n      - Serverless\n    serviceName: OCI Functions API\n    serviceCategory: API\n  - name: OCI DevOps API\n    baseURL: https://devops.{region}.oci.oraclecloud.com\n    tags:\n      - Build\n      - CI/CD\n      - Deployment\n      - DevOps\n    serviceName: OCI DevOps API\n    serviceCategory: API\n  - name: OCI Data Science API\n    baseURL: https://datascience.{region}.oci.oraclecloud.com\n    tags:\n      - AI\n      - Data Science\n      - Machine\
  \ Learning\n      - Model Deployment\n    serviceName: OCI Data Science API\n    serviceCategory: API\n  - name: Oracle Analytics Cloud REST API\n    baseURL: https://{instance}.analytics.ocp.oraclecloud.com\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Data Visualization\n    serviceName: Oracle Analytics Cloud REST API\n    serviceCategory: API\n  - name: Oracle Digital Assistant REST API\n    baseURL: https://{instance}.digitalassistant.oci.oraclecloud.com\n    tags:\n      - Chatbot\n      - Conversational AI\n      - Digital Assistant\n    serviceName: Oracle Digital Assistant REST API\n    serviceCategory: API\n  - name: OCI Identity and Access Management API\n    baseURL: https://identity.{region}.oci.oraclecloud.com\n    tags:\n      - Access Management\n      - IAM\n      - Identity\n      - Security\n    serviceName: OCI Identity and Access Management API\n    serviceCategory: API\n  - name: OCI Object Storage API\n    baseURL: https://objectstorage.{region}.oraclecloud.com\n\
  \    tags:\n      - Cloud\n      - Object Storage\n      - Storage\n    serviceName: OCI Object Storage API\n    serviceCategory: API\n  - name: OCI Monitoring API\n    baseURL: https://telemetry.{region}.oci.oraclecloud.com\n    tags:\n      - Alarms\n      - Metrics\n      - Monitoring\n      - Observability\n    serviceName: OCI Monitoring API\n    serviceCategory: API\n  - name: OCI Notifications API\n    baseURL: https://notification.{region}.oci.oraclecloud.com\n    tags:\n      - Messaging\n      - Notifications\n      - Pub/Sub\n    serviceName: OCI Notifications API\n    serviceCategory: API\n  - name: OCI Streaming API\n    baseURL: https://streaming.{region}.oci.oraclecloud.com\n    tags:\n      - Event Streaming\n      - Kafka\n      - Messaging\n      - Streaming\n    serviceName: OCI Streaming API\n    serviceCategory: API\n  - name: OCI Queue API\n    baseURL: https://queue.{region}.oci.oraclecloud.com\n    tags:\n      - Messaging\n      - Queue\n      - Serverless\n  \
  \  serviceName: OCI Queue API\n    serviceCategory: API\n  - name: OCI Vault API\n    baseURL: https://kms.{region}.oraclecloud.com\n    tags:\n      - Encryption\n      - Key Management\n      - Secrets\n      - Security\n    serviceName: OCI Vault API\n    serviceCategory: API\n  - name: OCI Logging API\n    baseURL: https://logging.{region}.oci.oraclecloud.com\n    tags:\n      - Log Management\n      - Logging\n      - Observability\n    serviceName: OCI Logging API\n    serviceCategory: API\n  - name: OCI Autonomous Database REST API\n    baseURL: https://database.{region}.oraclecloud.com\n    tags:\n      - Autonomous Database\n      - Cloud\n      - Database\n    serviceName: OCI Autonomous Database REST API\n    serviceCategory: API\n  - name: OCI MySQL HeatWave API\n    baseURL: https://mysql.{region}.oraclecloud.com\n    tags:\n      - Database\n      - HeatWave\n      - MySQL\n    serviceName: OCI MySQL HeatWave API\n    serviceCategory: API\n  - name: OCI Events API\n    baseURL:\
  \ https://events.{region}.oci.oraclecloud.com\n    tags:\n      - Automation\n      - Cloud\n      - Events\n    serviceName: OCI Events API\n    serviceCategory: API\n  - name: OCI Logging Analytics API\n    baseURL: https://loganalytics.{region}.oci.oraclecloud.com\n    tags:\n      - Analytics\n      - Log Management\n      - Logging\n      - Observability\n    serviceName: OCI Logging Analytics API\n    serviceCategory: API\n  - name: Oracle Cloud Infrastructure Process Automation API\n    baseURL: https://{instance}.process.oci.oraclecloud.com\n    tags:\n      - BPM\n      - Process Automation\n      - Workflow\n    serviceName: Oracle Cloud Infrastructure Process Automation API\n    serviceCategory: API\n  - name: OCI Compute API\n    baseURL: https://iaas.{region}.oraclecloud.com\n    tags:\n      - Bare Metal\n      - Cloud\n      - Compute\n      - Virtual Machines\n    serviceName: OCI Compute API\n    serviceCategory: API\n  - name: OCI Networking API\n    baseURL: https://iaas.{region}.oraclecloud.com\n\
  \    tags:\n      - Cloud\n      - Infrastructure\n      - Networking\n      - VCN\n    serviceName: OCI Networking API\n    serviceCategory: API\n  - name: OCI Block Volume API\n    baseURL: https://iaas.{region}.oraclecloud.com\n    tags:\n      - Block Volume\n      - Cloud\n      - Storage\n    serviceName: OCI Block Volume API\n    serviceCategory: API\n  - name: OCI File Storage API\n    baseURL: https://filestorage.{region}.oraclecloud.com\n    tags:\n      - Cloud\n      - File Storage\n      - NFS\n      - Storage\n    serviceName: OCI File Storage API\n    serviceCategory: API\n  - name: OCI Load Balancer API\n    baseURL: https://iaas.{region}.oraclecloud.com\n    tags:\n      - Cloud\n      - Load Balancer\n      - Networking\n      - Traffic Management\n    serviceName: OCI Load Balancer API\n    serviceCategory: API\n  - name: OCI DNS API\n    baseURL: https://dns.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud\n      - DNS\n      - Networking\n      - Traffic Management\n\
  \    serviceName: OCI DNS API\n    serviceCategory: API\n  - name: OCI Web Application Firewall API\n    baseURL: https://waf.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud\n      - Firewall\n      - Security\n      - WAF\n    serviceName: OCI Web Application Firewall API\n    serviceCategory: API\n  - name: OCI Email Delivery API\n    baseURL: https://email.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud\n      - Email\n      - Messaging\n    serviceName: OCI Email Delivery API\n    serviceCategory: API\n  - name: OCI Container Registry API\n    baseURL: https://ocir.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud Native\n      - Containers\n      - Docker\n      - Registry\n    serviceName: OCI Container Registry API\n    serviceCategory: API\n  - name: OCI Data Integration API\n    baseURL: https://dataintegration.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud\n      - Data Integration\n      - Data Pipeline\n      - ETL\n    serviceName: OCI Data Integration\
  \ API\n    serviceCategory: API\n  - name: OCI Data Flow API\n    baseURL: https://dataflow.{region}.oci.oraclecloud.com\n    tags:\n      - Apache Spark\n      - Big Data\n      - Cloud\n      - Data Processing\n    serviceName: OCI Data Flow API\n    serviceCategory: API\n  - name: OCI Data Catalog API\n    baseURL: https://datacatalog.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud\n      - Data Catalog\n      - Data Governance\n      - Metadata\n    serviceName: OCI Data Catalog API\n    serviceCategory: API\n  - name: OCI Search with OpenSearch API\n    baseURL: https://search-opensearch.{region}.oci.oraclecloud.com\n    tags:\n      - Cloud\n      - Full-Text Search\n      - OpenSearch\n      - Search\n    serviceName: OCI Search with OpenSearch API\n    serviceCategory: API\n  - name: OCI Resource Manager API\n    baseURL: https://resourcemanager.{region}.oci.oraclecloud.com\n    tags:\n      - Automation\n      - Cloud\n      - Infrastructure as Code\n      - Terraform\n\
  \    serviceName: OCI Resource Manager API\n    serviceCategory: API\n  - name: OCI Bastion API\n    baseURL: https://bastion.{region}.oci.oraclecloud.com\n    tags:\n      - Access Control\n      - Bastion\n      - Cloud\n      - Security\n    serviceName: OCI Bastion API\n    serviceCategory: API\n  - name: Oracle APEX REST API\n    baseURL: https://{instance}.adb.{region}.oraclecloudapps.com/ords\n    tags:\n      - APEX\n      - Application Development\n      - Low-Code\n      - REST\n    serviceName: Oracle APEX REST API\n    serviceCategory: API\n  - name: Oracle Visual Builder REST API\n    baseURL: https://{instance}.builder.ocp.oraclecloud.com\n    tags:\n      - Application Development\n      - Cloud\n      - Low-Code\n      - Visual Builder\n    serviceName: Oracle Visual Builder REST API\n    serviceCategory: API\n  - name: Oracle CX for Industries API\n    baseURL: https://{instance}.oraclecloud.com\n    tags:\n      - CX\n      - Industries\n      - SaaS\n    serviceName:\
  \ Oracle CX for Industries API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle/refs/heads/main/finops/oracle-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Database
- Enterprise
- Infrastructure
- SaaS
- FinOps
- Cost Management
- FOCUS
---
