# Assignment 2: Cloud Service Providers Comparison Report  

Name: Rohan Surti (surt0008) [041164260]
---

## 1. Executive Summary
This report compares Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP) for remote data and real-time applications. The comparison includes RESTful APIs, GraphQL, WebSockets, data streaming, and stream analytics. AWS provides strong serverless options such as API Gateway, AppSync, and Kinesis which make real-time and event driven applications easier to build. Azure focuses on enterprise friendly services like API Management, SignalR Service, and Event Hubs which integrate well with Microsoft tools. GCP provides powerful data handling services such as Apigee, Pub Sub, and Dataflow which work well for analytics and large scale data processing.

Pricing varies between providers. AWS usually charges per request or data volume. Azure uses tier based pricing for API Management and unit based pricing for real-time services. GCP mostly charges based on the total bytes processed. For real-time GraphQL systems AWS is a strong choice. For .NET based real-time messaging Azure is the easiest. For high throughput analytics pipelines GCP is usually the best option.

## 2. Introduction

### Purpose and Scope
The purpose of this report is to compare AWS, Azure, and GCP for remote data and real-time cloud use cases. This includes REST APIs, GraphQL APIs, WebSockets, data streaming, and real-time analytics. The comparison helps identify which cloud provider fits specific application needs.

### Overview of Cloud Providers
- **AWS**: Strong serverless and event driven services.  
- **Azure**: Enterprise focused with Microsoft integration.  
- **GCP**: Best known for data and analytics capabilities.

## 3. Service Comparison
## a) RESTful API Services Comparison

| Feature | AWS | Azure | GCP |
|--------|-----|-------|------|
| Main Service | API Gateway | API Management | Apigee, API Gateway |
| Best Use Case | Serverless REST APIs | Enterprise API governance | Large scale API programs |
| Pricing Style | Pay per API call | Tier based | Pay per call or subscription |
| Integration | Lambda, DynamoDB, IAM | Azure Functions, Logic Apps | Cloud Run, IAM |
| Strength | Easy serverless setup | Full API lifecycle | Enterprise API management |

---

## b) GraphQL Services Comparison

| Feature | AWS | Azure | GCP |
|--------|-----|-------|------|
| Main Service | AppSync | Custom hosted GraphQL | Hasura, Apollo on Cloud Run |
| Built in Realtime | Yes (Subscriptions) | No | No (depends on framework) |
| Pricing Style | Per operation and connection minutes | Depends on hosting service | Depends on hosting service |
| Integration | DynamoDB, Lambda | App Service, Functions | Cloud Run, BigQuery (via Hasura) |
| Strength | Fully managed GraphQL | Flexible hosting | Analytics focused GraphQL setups |

---

## c) WebSocket and Real-time Messaging Comparison

| Feature | AWS | Azure | GCP |
|--------|-----|-------|------|
| Main Service | API Gateway WebSockets | Azure SignalR Service | Self hosted WebSocket servers |
| Built in Messaging | Yes | Yes | No (manual setup) |
| Pricing | Based on connections and messages | Based on units and connections | Platform compute cost |
| Best Use Case | Serverless real-time apps | .NET real-time apps | Custom WebSocket workloads |
| Strength | Good Lambda integration | Easiest real-time for .NET | Very flexible but manual |

---

## d) Data Streaming Services Comparison

| Feature | AWS | Azure | GCP |
|--------|-----|-------|------|
| Main Service | Kinesis Data Streams | Event Hubs | Pub Sub |
| Message Throughput | High | Very high | Extremely high |
| Pricing | Shard based or on-demand | Throughput units | Per message and bytes |
| Integration | Lambda, S3, Redshift | Stream Analytics, Functions | Dataflow, BigQuery |
| Best For | Serverless streaming | Enterprise ingestion | Large analytics pipelines |

---

## e) Stream Analytics Comparison

| Feature | AWS | Azure | GCP |
|--------|-----|-------|------|
| Main Service | Kinesis Data Analytics | Azure Stream Analytics | Dataflow |
| Query Type | SQL, Java | SQL | Apache Beam pipelines |
| Best Use Case | Kinesis based analytics | Simple real-time rules | Complex pipelines and ETL |
| Integration | S3, Kinesis | Event Hubs, Power BI | Pub Sub, BigQuery |
| Strength | Easy Kinesis integration | Very simple SQL model | Best for large scale analytics |

## 4. Use Case Analysis

### Use Case A: Real-time Collaborative Chat App  
**(Low latency, many concurrent connections)**

#### Requirements:
- Real-time messaging  
- Presence status  
- Low latency  
- Serverless scaling  
- Medium level message storage  

#### Recommendation:
Azure is a good choice if the app is built with .NET and you want easy real-time features. Azure SignalR makes fan-out and presence very simple.

AWS is a good choice if you want a serverless system using AWS Lambda and GraphQL. AWS AppSync provides GraphQL subscriptions and integrates well with serverless backends.

---

### Use Case B: High-throughput Telemetry Pipeline  
**(IoT or sensor data with real-time analytics)**

#### Requirements:
- Handle millions of events per second  
- Strong durability and auto-scaling  
- Real-time analytics on streaming data  
- Long-term analytics in a data warehouse  

#### Recommendation:
GCP (Pub/Sub, Dataflow, BigQuery) is great if analytics and BigQuery are the main focus.Provides smooth integration and cost-effective pricing for large datasets.

AWS (Kinesis, Kinesis Data Analytics, S3 or Redshift) is strong if your system is already on AWS. Works well with Lambda and other AWS ecosystem services.

## 5. Conclusion
AWS is great for serverless real-time and GraphQL based systems. Azure is best for enterprise environments and .NET based real-time applications. GCP is the strongest for large scale data and analytics pipelines. The best provider depends on the application design and the surrounding cloud ecosystem.

## 6. AI Usage Disclosure
I used AI to help organize the report. I reviewed and edited all information to match my understanding. The final choices and explanations reflect my own learning and interpretation.

## 7. References

### Azure Services

- Azure SignalR Service:
https://learn.microsoft.com/azure/azure-signalr
- Azure Functions:
https://learn.microsoft.com/azure/azure-functions
- Azure Event Hubs:
https://learn.microsoft.com/azure/event-hubs
- Azure Stream Analytics:
https://learn.microsoft.com/azure/stream-analytics
- Azure Cosmos DB:
https://learn.microsoft.com/azure/cosmos-db

### AWS Services

- AWS AppSync (GraphQL):
https://docs.aws.amazon.com/appsync
- AWS Lambda:
https://docs.aws.amazon.com/lambda
- Amazon Kinesis Data Streams:
https://docs.aws.amazon.com/kinesis
- Amazon Kinesis Data Analytics:
https://docs.aws.amazon.com/kinesisanalytics
- Amazon S3:
https://docs.aws.amazon.com/s3
- Amazon Redshift:
https://docs.aws.amazon.com/redshift

### Google Cloud Services

- Google Pub/Sub:
https://cloud.google.com/pubsub
- Google Dataflow:
https://cloud.google.com/dataflow
- Google BigQuery:
https://cloud.google.com/bigquery
