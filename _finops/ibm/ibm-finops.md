---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: assistant-v2.json
  format: json
  label: IBM Watson Assistant
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/assistant/assistant-v2.json
- filename: natural-language-understanding.json
  format: json
  label: IBM Watson Natural Language Understanding
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/natural-language-understanding/natural-language-understanding.json
- filename: language-translator.json
  format: json
  label: IBM Watson Language Translator
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/language-translator/language-translator.json
- filename: speech-to-text.json
  format: json
  label: IBM Watson Speech to Text
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/speech-to-text/speech-to-text.json
- filename: text-to-speech.json
  format: json
  label: IBM Watson Text to Speech
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/watson-developer-cloud/api-spec/master/text-to-speech/text-to-speech.json
- filename: ibm-cloud-iam.yml
  format: yaml
  label: IBM Cloud IAM Identity Services
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ibm/refs/heads/main/openapi/ibm-cloud-iam.yml
- filename: ibm-cloud-iam.yml
  format: yaml
  label: IBM IAM Policy Management
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ibm/refs/heads/main/openapi/ibm-cloud-iam.yml
- filename: ibm-cloud-iam.yml
  format: yaml
  label: IBM IAM Access Groups
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ibm/refs/heads/main/openapi/ibm-cloud-iam.yml
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
description: FinOps framework definition for the IBM API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: IBM
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: IBM
  PublisherName: IBM
  ServiceCategory: Developer Tools / API
  ServiceName: IBM
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
name: Ibm Finops
provider_name: IBM
provider_slug: ibm
publisher_name: IBM
service_category: API
slug: ibm-finops
source_filename: ibm-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: IBM\nproviderId: ibm\npublisherName: IBM\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Management\n  - Artificial Intelligence\n  - Billing\n  - Cloud Computing\n  - Containers\n  - Data Governance\n  - Databases\n  - DevOps\n  - Enterprise\n  - Generative AI\n  - Hybrid Cloud\n  - Infrastructure\n  - Machine Learning\n  - Networking\n  - Observability\n  - Security\n  - Serverless\n  - Storage\n  - Watson\n  - Watsonx\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the IBM API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's\
  \ APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n\
  \    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: IBM\n  ServiceCategory: Developer Tools / API\n  ProviderName: IBM\n  PublisherName: IBM\n  InvoiceIssuerName: IBM\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: IBM Watson Assistant\n    baseURL: https://api.us-south.assistant.watson.cloud.ibm.com\n    tags:\n      - Artificial Intelligence\n      - Chatbots\n      - Conversational AI\n      - NLP\n    serviceName: IBM Watson Assistant\n    serviceCategory: API\n  - name: IBM Watson Natural Language Understanding\n    baseURL: https://api.us-south.natural-language-understanding.watson.cloud.ibm.com\n    tags:\n      - AI\n      - Machine Learning\n      - Natural Language Processing\n      -\
  \ Text Analysis\n    serviceName: IBM Watson Natural Language Understanding\n    serviceCategory: API\n  - name: IBM Watson Language Translator\n    baseURL: https://api.us-south.language-translator.watson.cloud.ibm.com\n    tags:\n      - AI\n      - Language\n      - Translation\n    serviceName: IBM Watson Language Translator\n    serviceCategory: API\n  - name: IBM Watson Speech to Text\n    baseURL: https://api.us-south.speech-to-text.watson.cloud.ibm.com\n    tags:\n      - AI\n      - Audio\n      - Speech Recognition\n      - Transcription\n    serviceName: IBM Watson Speech to Text\n    serviceCategory: API\n  - name: IBM Watson Text to Speech\n    baseURL: https://api.us-south.text-to-speech.watson.cloud.ibm.com\n    tags:\n      - AI\n      - Audio Generation\n      - Text to Speech\n      - Voice Synthesis\n    serviceName: IBM Watson Text to Speech\n    serviceCategory: API\n  - name: IBM Cloud Object Storage\n    baseURL: https://s3.us.cloud-object-storage.appdomain.cloud\n\
  \    tags:\n      - Cloud Storage\n      - Object Storage\n      - S3 Compatible\n      - Storage\n    serviceName: IBM Cloud Object Storage\n    serviceCategory: API\n  - name: IBM Cloud Databases for PostgreSQL\n    baseURL: https://api.us-south.databases.cloud.ibm.com\n    tags:\n      - Cloud\n      - Database\n      - Managed Database\n      - PostgreSQL\n    serviceName: IBM Cloud Databases for PostgreSQL\n    serviceCategory: API\n  - name: IBM Cloud Code Engine\n    baseURL: https://api.us-south.codeengine.cloud.ibm.com\n    tags:\n      - Cloud Native\n      - Containers\n      - Platform\n      - Serverless\n    serviceName: IBM Cloud Code Engine\n    serviceCategory: API\n  - name: IBM watsonx.ai\n    baseURL: https://us-south.ml.cloud.ibm.com\n    tags:\n      - Artificial Intelligence\n      - Foundation Models\n      - Generative AI\n      - Large Language Models\n      - Machine Learning\n    serviceName: IBM watsonx.ai\n    serviceCategory: API\n  - name: IBM watsonx.governance\n\
  \    baseURL: https://us-south.ml.cloud.ibm.com\n    tags:\n      - AI Governance\n      - Artificial Intelligence\n      - Compliance\n      - Model Monitoring\n      - Trust\n    serviceName: IBM watsonx.governance\n    serviceCategory: API\n  - name: IBM Watson Discovery\n    baseURL: https://api.us-south.discovery.watson.cloud.ibm.com\n    tags:\n      - AI\n      - Cognitive Search\n      - Content Analytics\n      - Document Understanding\n    serviceName: IBM Watson Discovery\n    serviceCategory: API\n  - name: IBM Cloud Virtual Private Cloud\n    baseURL: https://us-south.iaas.cloud.ibm.com\n    tags:\n      - Cloud\n      - Compute\n      - Infrastructure\n      - Networking\n      - VPC\n    serviceName: IBM Cloud Virtual Private Cloud\n    serviceCategory: API\n  - name: IBM Cloud Kubernetes Service\n    baseURL: https://containers.cloud.ibm.com\n    tags:\n      - Cloud Native\n      - Containers\n      - Kubernetes\n      - Orchestration\n    serviceName: IBM Cloud Kubernetes\
  \ Service\n    serviceCategory: API\n  - name: IBM Key Protect\n    baseURL: https://us-south.kms.cloud.ibm.com\n    tags:\n      - Data Protection\n      - Encryption\n      - Key Management\n      - Security\n    serviceName: IBM Key Protect\n    serviceCategory: API\n  - name: IBM Cloud IAM Identity Services\n    baseURL: https://iam.cloud.ibm.com\n    tags:\n      - Access Management\n      - Authentication\n      - Identity\n      - Security\n    serviceName: IBM Cloud IAM Identity Services\n    serviceCategory: API\n  - name: IBM Cloud Secrets Manager\n    baseURL: https://us-south.secrets-manager.appdomain.cloud\n    tags:\n      - Credentials\n      - Secrets\n      - Security\n      - Vault\n    serviceName: IBM Cloud Secrets Manager\n    serviceCategory: API\n  - name: IBM Cloud Event Notifications\n    baseURL: https://us-south.event-notifications.cloud.ibm.com\n    tags:\n      - Alerts\n      - Events\n      - Messaging\n      - Notifications\n    serviceName: IBM Cloud Event\
  \ Notifications\n    serviceCategory: API\n  - name: IBM Cloud Container Registry\n    baseURL: https://us.icr.io\n    tags:\n      - Container Registry\n      - Containers\n      - Docker\n      - Images\n    serviceName: IBM Cloud Container Registry\n    serviceCategory: API\n  - name: IBM Cloud Schematics\n    baseURL: https://us-south.schematics.cloud.ibm.com\n    tags:\n      - Automation\n      - Infrastructure as Code\n      - Provisioning\n      - Terraform\n    serviceName: IBM Cloud Schematics\n    serviceCategory: API\n  - name: IBM Cloud Internet Services\n    baseURL: https://api.cis.cloud.ibm.com\n    tags:\n      - CDN\n      - DDoS Protection\n      - DNS\n      - Security\n      - Web Application Firewall\n    serviceName: IBM Cloud Internet Services\n    serviceCategory: API\n  - name: IBM Cloudant\n    baseURL: https://us-south.cloudantnosqldb.appdomain.cloud\n    tags:\n      - Database\n      - Document Database\n      - JSON\n      - NoSQL\n    serviceName: IBM Cloudant\n\
  \    serviceCategory: API\n  - name: IBM Event Streams\n    baseURL: https://us-south.event-streams.cloud.ibm.com\n    tags:\n      - Apache Kafka\n      - Event Streaming\n      - Messaging\n      - Pub/Sub\n    serviceName: IBM Event Streams\n    serviceCategory: API\n  - name: IBM Cloud Security and Compliance Center\n    baseURL: https://us-south.compliance.cloud.ibm.com\n    tags:\n      - Compliance\n      - Governance\n      - Risk Management\n      - Security\n    serviceName: IBM Cloud Security and Compliance Center\n    serviceCategory: API\n  - name: IBM Cloud Functions\n    baseURL: https://us-south.functions.cloud.ibm.com\n    tags:\n      - Apache OpenWhisk\n      - Event-Driven\n      - Functions as a Service\n      - Serverless\n    serviceName: IBM Cloud Functions\n    serviceCategory: API\n  - name: IBM Cloud DNS Services\n    baseURL: https://api.dns-svcs.cloud.ibm.com\n    tags:\n      - DNS\n      - Domain Management\n      - Networking\n    serviceName: IBM Cloud\
  \ DNS Services\n    serviceCategory: API\n  - name: IBM Cloud Monitoring\n    baseURL: https://us-south.monitoring.cloud.ibm.com\n    tags:\n      - Alerting\n      - Metrics\n      - Monitoring\n      - Observability\n    serviceName: IBM Cloud Monitoring\n    serviceCategory: API\n  - name: IBM Cloud Logs\n    baseURL: https://us-south.logs.cloud.ibm.com\n    tags:\n      - Log Analysis\n      - Logging\n      - Observability\n    serviceName: IBM Cloud Logs\n    serviceCategory: API\n  - name: IBM Cloud Activity Tracker\n    baseURL: https://us-south.atracker.cloud.ibm.com\n    tags:\n      - Activity Tracking\n      - Auditing\n      - Compliance\n      - Observability\n    serviceName: IBM Cloud Activity Tracker\n    serviceCategory: API\n  - name: IBM Cloud App ID\n    baseURL: https://us-south.appid.cloud.ibm.com\n    tags:\n      - Authentication\n      - Authorization\n      - Identity\n      - Security\n    serviceName: IBM Cloud App ID\n    serviceCategory: API\n  - name: IBM\
  \ Cloud Transit Gateway\n    baseURL: https://transit.cloud.ibm.com\n    tags:\n      - Connectivity\n      - Hybrid Cloud\n      - Networking\n      - Transit Gateway\n    serviceName: IBM Cloud Transit Gateway\n    serviceCategory: API\n  - name: IBM Cloud Resource Controller\n    baseURL: https://resource-controller.cloud.ibm.com\n    tags:\n      - Cloud Management\n      - Provisioning\n      - Resource Management\n    serviceName: IBM Cloud Resource Controller\n    serviceCategory: API\n  - name: IBM Cloud Global Search\n    baseURL: https://api.global-search-tagging.cloud.ibm.com\n    tags:\n      - Cloud Management\n      - Resource Discovery\n      - Search\n    serviceName: IBM Cloud Global Search\n    serviceCategory: API\n  - name: IBM Cloud Global Tagging\n    baseURL: https://tags.global-search-tagging.cloud.ibm.com\n    tags:\n      - Organization\n      - Resource Management\n      - Tagging\n    serviceName: IBM Cloud Global Tagging\n    serviceCategory: API\n  - name:\
  \ IBM IAM Policy Management\n    baseURL: https://iam.cloud.ibm.com\n    tags:\n      - Access Control\n      - IAM\n      - Policies\n      - Security\n    serviceName: IBM IAM Policy Management\n    serviceCategory: API\n  - name: IBM IAM Access Groups\n    baseURL: https://iam.cloud.ibm.com\n    tags:\n      - Access Groups\n      - Access Management\n      - IAM\n      - Security\n    serviceName: IBM IAM Access Groups\n    serviceCategory: API\n  - name: IBM Cloud Power Virtual Server\n    baseURL: https://us-south.power-iaas.cloud.ibm.com\n    tags:\n      - AIX\n      - IBM I\n      - Infrastructure\n      - Power Systems\n      - Virtual Server\n    serviceName: IBM Cloud Power Virtual Server\n    serviceCategory: API\n  - name: IBM Cloud Enterprise Management\n    baseURL: https://enterprise.cloud.ibm.com\n    tags:\n      - Account Management\n      - Billing\n      - Enterprise\n      - Multi-Account\n    serviceName: IBM Cloud Enterprise Management\n    serviceCategory: API\n\
  \  - name: IBM Cloud Projects\n    baseURL: https://projects.api.cloud.ibm.com\n    tags:\n      - Configuration\n      - Deployment\n      - Governance\n      - Infrastructure as Code\n    serviceName: IBM Cloud Projects\n    serviceCategory: API\n  - name: IBM watsonx.data\n    baseURL: https://us-south.lakehouse.cloud.ibm.com\n    tags:\n      - AI Data\n      - Analytics\n      - Data Lakehouse\n      - Data Management\n      - Open Source\n    serviceName: IBM watsonx.data\n    serviceCategory: API\n  - name: IBM API Connect\n    baseURL: https://api.us-south.apiconnect.cloud.ibm.com\n    tags:\n      - API Gateway\n      - API Management\n      - API Security\n      - Developer Portal\n    serviceName: IBM API Connect\n    serviceCategory: API\n  - name: IBM Cloud Direct Link\n    baseURL: https://directlink.cloud.ibm.com\n    tags:\n      - Connectivity\n      - Hybrid Cloud\n      - Networking\n      - Private Network\n    serviceName: IBM Cloud Direct Link\n    serviceCategory:\
  \ API\n  - name: IBM Cloud Continuous Delivery Toolchain\n    baseURL: https://api.us-south.devops.cloud.ibm.com\n    tags:\n      - CI/CD\n      - Continuous Delivery\n      - DevOps\n      - Toolchain\n    serviceName: IBM Cloud Continuous Delivery Toolchain\n    serviceCategory: API\n  - name: IBM Cloud Tekton Pipeline\n    baseURL: https://api.us-south.devops.cloud.ibm.com\n    tags:\n      - CI/CD\n      - DevOps\n      - Kubernetes\n      - Pipelines\n      - Tekton\n    serviceName: IBM Cloud Tekton Pipeline\n    serviceCategory: API\n  - name: IBM Cloud User Management\n    baseURL: https://user-management.cloud.ibm.com\n    tags:\n      - Account Management\n      - IAM\n      - Identity\n      - User Management\n    serviceName: IBM Cloud User Management\n    serviceCategory: API\n  - name: IBM Cloud Usage Reports\n    baseURL: https://billing.cloud.ibm.com\n    tags:\n      - Billing\n      - Cost Management\n      - Reporting\n      - Usage\n    serviceName: IBM Cloud Usage\
  \ Reports\n    serviceCategory: API\n  - name: IBM Cloud Global Catalog\n    baseURL: https://globalcatalog.cloud.ibm.com\n    tags:\n      - Catalog\n      - Product Catalog\n      - Resource Management\n    serviceName: IBM Cloud Global Catalog\n    serviceCategory: API\n  - name: IBM Cloud Catalog Management\n    baseURL: https://cm.globalcatalog.cloud.ibm.com\n    tags:\n      - Catalog Management\n      - Governance\n      - Private Catalog\n    serviceName: IBM Cloud Catalog Management\n    serviceCategory: API\n  - name: IBM Cloud Context-based Restrictions\n    baseURL: https://cbr.cloud.ibm.com\n    tags:\n      - Access Control\n      - Network Security\n      - Restrictions\n      - Security\n    serviceName: IBM Cloud Context-based Restrictions\n    serviceCategory: API\n  - name: IBM Cloud Databases for Redis\n    baseURL: https://api.us-south.databases.cloud.ibm.com\n    tags:\n      - Caching\n      - Database\n      - In-Memory\n      - Managed Database\n      - Redis\n\
  \    serviceName: IBM Cloud Databases for Redis\n    serviceCategory: API\n  - name: IBM Cloud Databases for MongoDB\n    baseURL: https://api.us-south.databases.cloud.ibm.com\n    tags:\n      - Database\n      - Document Database\n      - Managed Database\n      - MongoDB\n      - NoSQL\n    serviceName: IBM Cloud Databases for MongoDB\n    serviceCategory: API\n  - name: IBM Cloud Databases for Elasticsearch\n    baseURL: https://api.us-south.databases.cloud.ibm.com\n    tags:\n      - Database\n      - Elasticsearch\n      - Log Analytics\n      - Managed Database\n      - Search\n    serviceName: IBM Cloud Databases for Elasticsearch\n    serviceCategory: API\n  - name: IBM Cloud Enterprise Billing Units\n    baseURL: https://billing.cloud.ibm.com\n    tags:\n      - Billing\n      - Cost Management\n      - Credit Management\n      - Enterprise\n    serviceName: IBM Cloud Enterprise Billing Units\n    serviceCategory: API\n  - name: IBM Cloud Enterprise Usage Reports\n    baseURL:\
  \ https://enterprise.cloud.ibm.com\n    tags:\n      - Analytics\n      - Cost Management\n      - Enterprise\n      - Usage Reports\n    serviceName: IBM Cloud Enterprise Usage Reports\n    serviceCategory: API\n  - name: IBM Cloud VMware Solutions\n    baseURL: https://api.us-south.vmware.cloud.ibm.com\n    tags:\n      - Hybrid Cloud\n      - Infrastructure\n      - Virtualization\n      - VMware\n    serviceName: IBM Cloud VMware Solutions\n    serviceCategory: API\n  - name: IBM watsonx.ai Runtime\n    baseURL: https://us-south.ml.cloud.ibm.com\n    tags:\n      - AI\n      - Data Science\n      - Machine Learning\n      - Model Deployment\n      - Model Training\n    serviceName: IBM watsonx.ai Runtime\n    serviceCategory: API\n  - name: IBM Knowledge Catalog\n    baseURL: https://api.dataplatform.cloud.ibm.com\n    tags:\n      - AI Governance\n      - Data Catalog\n      - Data Governance\n      - Metadata Management\n    serviceName: IBM Knowledge Catalog\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: IBM Cloud\n    email: cloud@ibm.com\n    url: https://www.ibm.com/cloud\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ibm/refs/heads/main/finops/ibm-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Management
- Artificial Intelligence
- Billing
- Cloud Computing
- Containers
- Data Governance
- Databases
- DevOps
- Enterprise
- Generative AI
- Hybrid Cloud
- Infrastructure
- Machine Learning
- Networking
- Observability
- Security
- Serverless
- Storage
- Watson
- Watsonx
- FinOps
- Cost Management
- FOCUS
---
