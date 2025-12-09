# Telemetry Notes

Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[brown9804](https://github.com/brown9804)

Aug, 2022

----------

`Use telemetry when you need to collect and transmit data from remote sources, such as equipment or systems in hard-to-reach or hazardous environments. Telemetry is often used for performance monitoring, asset tracking, and predictive maintenance.`

  <img width="1659" alt="image" src="https://github.com/brown9804/CenLog_LPath/assets/24630902/c794fbc3-0fc9-41a4-916b-7519a874684d">

## Content 

- [Telemetry Notes](#telemetry-notes)
  - [Content](#content)
  - [Open Telemetry](#open-telemetry)
  - [Observability Backends](#observability-backends)


## Open Telemetry

`OpenTelemetry is a collection of APIs, SDKs, and client libraries used to generate telemetry data from your application code`

- [What is OpenTelemetry?](https://www.youtube.com/watch?v=jt5HLptVvbM), [example](https://www.youtube.com/watch?v=UzeExvj_Q4s).

  <img width="1510" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/510c002b-e0ab-40a7-8166-af9e5e4c2e34">

- [How Does Open Telemetry Work?](https://www.youtube.com/watch?v=YwyfYfgjG0w), look [OpenTelemetry as a Service](https://medium.com/@magstherdev/opentelemetry-as-a-service-497068b81f7c). 

  ![image](https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/5da3a80d-2cf9-49da-8450-04a975aeccf9)

  <img width="726" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/8dad1b3b-51a6-4652-90ba-b4e53bcb77e8">

  <img width="1221" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/76ee4572-6774-4242-8dd1-78eebc954632">

- [A beginner’s guide](https://faun.pub/opentelemetry-d71d369c83d7) to OpenTelemetry. <br/>

  <img width="1226" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/33282fc4-9e5c-4947-b2c6-07a36e36e864">

  <img width="1080" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/6edf6a2a-4dbc-45d3-8615-17ad467913dd">
  
- [Telemetry with OpenTelemetry, Prometheus and Jaeger](https://medium.com/@guilospanck/telemetry-with-opentelemetry-prometheus-and-jaeger-46a2d9dec86b)

  <img width="817" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/880b1806-36b2-4197-a7b4-aed3c5a5ccaf">

- [The Basics of Distributed Tracing](https://www.youtube.com/watch?v=uxT032OxVOA)

  <img width="1512" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/bf3d22b6-270d-46dd-a524-f9c90619c497">

- [Introduction to EDA & Tracing Challenges](https://www.youtube.com/watch?v=u9oBD5pqDig)

  <img width="1441" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/301c5c0f-eada-4c35-83e5-3be9e0c83c40">

- [How Does Distributed Tracing Work With an Event Broker?](https://www.youtube.com/watch?v=q4035-O4bww)

  <img width="833" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/09697172-a9ea-4c5e-8c91-41d972602c50">

  <img width="983" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/7b8a4517-0eb9-42a6-bd5f-56a7072e3bc2">

- [OpenTelemetry code instrumentation](https://opentelemetry.io/docs/instrumentation/) is supported for many popular programming languages, [more details on Observability Agent](https://docs.fusion-reactor.com/Getting-started/GSOTel/)

  <img width="744" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/837e2c42-a29c-411a-b0e8-b0adc5302201">

  <img width="742" alt="image" src="https://github.com/brown9804/Obs_Mon_LPath/assets/24630902/2344144c-07fa-4303-ad63-7346d993da58">



## Observability Backends 

| Name | Data Type | Pricing | Azure Service | Definition | Pros | Cons |
| --- | --- | --- | --- | --- | --- | --- |
| **Azure Monitor** | [Metrics](https://docs.microsoft.com/en-us/azure/azure-monitor/essentials/metrics-supported) <br/> [Traces](https://docs.microsoft.com/en-us/azure/azure-monitor/app/distributed-tracing) <br/> [Logs](https://docs.microsoft.com/en-us/azure/azure-monitor/logs/) | Pay-as-you-go <br/> Commitment tiers <br/> [Azure Monitor Pricing](https://azure.microsoft.com/en-us/pricing/details/monitor/) | [Azure Monitor](https://azure.microsoft.com/en-us/products/monitor) + [Application Insights](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview) | Azure's native observability platform providing full-stack monitoring with deep integration across all Azure services. Supports OpenTelemetry for hybrid cloud scenarios and integrates with open source tools like Grafana, Prometheus, and Jaeger. | - **Native Azure Integration**: Seamless monitoring of all Azure services with automatic discovery <br/> - **OpenTelemetry Support**: Full OTEL compatibility for vendor-neutral instrumentation <br/> - **AI-Powered Insights**: Smart detection and root cause analysis using Azure AI <br/> - **Unified Platform**: Single pane of glass for metrics, logs, and traces <br/> - **Open Source Bridge**: Works with Grafana, Prometheus exporters, and OTEL collectors | - **Azure-Centric**: Less optimized for multi-cloud or pure on-premises scenarios <br/> - **Learning Curve**: Rich feature set requires investment in Azure-specific knowledge <br/> - **Cost Management**: Requires careful monitoring of data ingestion volumes |
| **Azure Managed Grafana** | [Metrics](https://docs.microsoft.com/en-us/azure/managed-grafana/overview) <br/> [Dashboards](https://grafana.com/docs/grafana/latest/dashboards/) | Essentials <br/> Standard <br/> [Azure Managed Grafana Pricing](https://azure.microsoft.com/en-us/pricing/details/managed-grafana/) | [Azure Managed Grafana](https://azure.microsoft.com/en-us/products/managed-grafana) | Fully managed Grafana service on Azure with native Azure Monitor integration, Azure AD authentication, and enterprise security. Combines open source Grafana with Azure's enterprise features and managed infrastructure. | - **Zero Infrastructure Management**: Fully managed Grafana with Azure SLA <br/> - **Azure AD Integration**: Enterprise authentication and RBAC out of the box <br/> - **Native Data Sources**: Built-in connectors to Azure Monitor, Log Analytics, and Azure Data Explorer <br/> - **Open Source Compatibility**: Full Grafana plugin ecosystem support <br/> - **Enterprise Features**: High availability, backup, and compliance built-in | - **Azure Dependency**: Requires Azure subscription and tied to Azure ecosystem <br/> - **Limited Customization**: Some advanced Grafana configurations may be restricted <br/> - **Cost for Small Teams**: May be expensive for small-scale monitoring needs |
| **Azure Monitor for Containers** | [Metrics](https://docs.microsoft.com/en-us/azure/azure-monitor/containers/prometheus-metrics) <br/> [Alerting](https://docs.microsoft.com/en-us/azure/azure-monitor/containers/prometheus-metrics-scrape-configuration) | Included with AKS <br/> Pay-per-use for data storage <br/> [Container Insights Pricing](https://azure.microsoft.com/en-us/pricing/details/monitor/) | [Azure Monitor for Containers](https://docs.microsoft.com/en-us/azure/azure-monitor/containers/container-insights-overview) + Managed Prometheus | Azure's managed Prometheus service integrated with AKS, providing Prometheus-compatible metrics collection with Azure Monitor backend storage and querying. Supports standard PromQL and integrates with Azure Managed Grafana. | - **Kubernetes Native**: Deep AKS integration with zero-config monitoring <br/> - **Prometheus Compatibility**: Standard PromQL queries and Prometheus exporters work seamlessly <br/> - **Azure Scale**: Leverages Azure Monitor's global scale and reliability <br/> - **Cost Optimization**: Intelligent sampling and data retention policies <br/> - **GitOps Ready**: Works with Azure Arc and hybrid Kubernetes environments | - **Kubernetes Focus**: Primarily designed for containerized workloads <br/> - **Azure Ecosystem**: Less suitable for non-Azure Kubernetes distributions <br/> - **Migration Complexity**: Moving from self-hosted Prometheus requires planning |
| **Azure Application Insights** | [Traces](https://docs.microsoft.com/en-us/azure/azure-monitor/app/distributed-tracing) <br/> [Dependencies](https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-dependencies) | Included with App Service <br/> Application Insights pricing <br/> [Application Insights Pricing](https://azure.microsoft.com/en-us/pricing/details/monitor/) | [Azure Application Insights](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview) with [OpenTelemetry](https://docs.microsoft.com/en-us/azure/azure-monitor/app/opentelemetry-enable) | Azure's APM solution with automatic instrumentation for Azure services and OpenTelemetry support for custom applications. Provides distributed tracing, performance monitoring, and intelligent diagnostics powered by Azure AI. | - **Auto-Instrumentation**: Zero-code monitoring for Azure App Services, Functions, and AKS <br/> - **OpenTelemetry Native**: Full OTEL support with vendor-neutral instrumentation <br/> - **AI-Powered Analytics**: Smart detection, anomaly detection, and failure analysis <br/> - **Live Metrics**: Real-time application performance monitoring <br/> - **Cross-Service Correlation**: Automatic tracing across Azure services and custom code | - **Application-Centric**: Less suitable for infrastructure-only monitoring <br/> - **Data Sampling**: High-volume applications may require sampling configuration <br/> - **Azure Optimization**: Best experience with Azure-hosted applications |
| **Azure Log Analytics** | [Logs](https://docs.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-overview) <br/> [KQL Queries](https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/) | Pay-per-GB ingested <br/> Commitment tiers <br/> [Log Analytics Pricing](https://azure.microsoft.com/en-us/pricing/details/monitor/) | [Azure Log Analytics](https://azure.microsoft.com/en-us/products/log-analytics) + [Azure Data Explorer](https://azure.microsoft.com/en-us/products/data-explorer) | Azure's log aggregation and analysis platform using KQL (Kusto Query Language). Integrates with Fluentd, Logstash, and other open source log collectors. Provides the backend for Azure Monitor and supports OpenTelemetry log ingestion. | - **Powerful Query Language**: KQL provides advanced analytics and correlation capabilities <br/> - **Massive Scale**: Handles petabytes of log data with sub-second query response <br/> - **Open Source Ingestion**: Supports Fluentd, Fluent Bit, Logstash, and OTEL collectors <br/> - **Cross-Workspace Queries**: Query across multiple Log Analytics workspaces and subscriptions <br/> - **Built-in Connectors**: Automatic log collection from all Azure services | - **Query Language Learning**: KQL has a learning curve compared to SQL <br/> - **Cost Management**: Log retention and query costs need careful planning <br/> - **Real-time Limitations**: Not optimized for real-time streaming analytics |
| **Azure Monitor Agent** | [Infrastructure Metrics](https://docs.microsoft.com/en-us/azure/azure-monitor/agents/azure-monitor-agent-overview) <br/> [Custom Metrics](https://docs.microsoft.com/en-us/azure/azure-monitor/agents/data-collection-rule-azure-monitor-agent) | Included with Azure VMs <br/> Custom metrics pricing applies <br/> [Azure Monitor Agent](https://docs.microsoft.com/en-us/azure/azure-monitor/agents/azure-monitor-agent-overview) | [Azure Monitor Agent](https://docs.microsoft.com/en-us/azure/azure-monitor/agents/azure-monitor-agent-overview) + [Azure Arc](https://azure.microsoft.com/en-us/products/azure-arc) | Next-generation monitoring agent for Azure and hybrid infrastructure. Supports data collection rules, integrates with Telegraf and other open source agents, and extends Azure monitoring to on-premises and multi-cloud environments through Azure Arc. | - **Hybrid Cloud Support**: Monitor Azure, on-premises, and other clouds through Azure Arc <br/> - **Data Collection Rules**: Flexible, policy-driven data collection configuration <br/> - **Open Source Integration**: Works alongside Telegraf, Prometheus node exporter, and other agents <br/> - **Security Enhanced**: Managed identity authentication and encrypted data transmission <br/> - **Cost Optimization**: Precise control over what data is collected and where it's sent | - **Migration Required**: Requires migration from legacy monitoring agents <br/> - **Configuration Complexity**: Data collection rules require Azure expertise <br/> - **Arc Dependency**: Hybrid scenarios require Azure Arc agent deployment |

<!-- START BADGE -->
<div align="center">
  <img src="https://img.shields.io/badge/Total%20views-1022-limegreen" alt="Total views">
  <p>Refresh Date: 2025-07-11</p>
</div>
<!-- END BADGE -->
