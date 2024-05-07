---
{"status":"planted","dg-publish":true,"tags":["concept/SRE/cloud/azure","review"],"ms-learn-url":"https://learn.microsoft.com/en-us/azure/azure-functions/functions-overview?pivots=programming-language-csharp","definition":"Azure Functions is a serverless solution that allows you to write less code, maintain less infrastructure, and save on costs","creation_date":"2024-05-02 18:40","permalink":"/concepts/azure-functions/","dgPassFrontmatter":true}
---

| MetaData   |                                              |
| ---------- | -------------------------------------------- |
| Definition | `VIEW[{definition}][text(renderMarkdown)]`   |
| Homesite   | `VIEW[{url}][text(renderMarkdown)]`          |
| MS Learn   | `VIEW[{ms-learn-url}][text(renderMarkdown)]` |

Code: [[Code/Azure Function Scenarios\|Azure Function Scenarios]]
Deployment: [[Concepts/Azure Functions Deployement\|Azure Functions Deployement]]

Azure Functions supports [[unsorted/Azure Function triggers\|triggers]], which are ways to start execution of your code, and [[unsorted/Azure Function Bindings\|bindings]], which are ways to simplify coding for input and output data. There are other integration and automation services in Azure and they all can solve integration problems and automate business processes. They can all define input, actions, conditions, and output.

## Difference with [[Concepts/Azure Logic Apps\|Azure Logic Apps]]

|                   | Azure Functions                                                       | Logic Apps                                                                                             |
| ----------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Development       | Code-first (imperative)                                               | Designer-first (declarative)                                                                           |
| Connectivity      | About a dozen built-in binding types, write code for custom bindings  | Large collection of connectors, Enterprise Integration Pack for B2B scenarios, build custom connectors |
| Actions           | Each activity is an Azure function; write code for activity functions | Large collection of ready-made actions                                                                 |
| Monitoring        | Azure Application Insights                                            | Azure portal, Azure Monitor logs                                                                       |
| Management        | REST API, Visual Studio                                               | Azure portal, REST API, PowerShell, Visual Studio                                                      |
| Execution context | Runs in Azure, or locally                                             | Runs in Azure, locally, or on premises                                                                 |
## Difference with [[Concepts/Azure App Service WebJobs\|Azure App Service WebJobs]]

> [!info]
> Azure Functions is built on the WebJobs SDK, so it shares many of the same event triggers and connections to other Azure services.

| |Functions|WebJobs with WebJobs SDK|
|---|---|---|
|Serverless app model with automatic scaling|Yes|No|
|Develop and test in browser|Yes|No|
|Pay-per-use pricing|Yes|No|
|Integration with Logic Apps|Yes|No|
|Trigger events|Timer  <br>Azure Storage queues and blobs  <br>Azure Service Bus queues and topics  <br>Azure Cosmos DB  <br>Azure Event Hubs  <br>HTTP/WebHook (GitHub  <br>Slack)  <br>Azure Event Grid|Timer  <br>Azure Storage queues and blobs  <br>Azure Service Bus queues and topics  <br>Azure Cosmos DB  <br>Azure Event Hubs  <br>File system|
## Hosting Plans

Reference: [MS Learn](https://learn.microsoft.com/en-us/azure/azure-functions/dedicated-plan)


> [!important] 
> Free and Shared tier App Service plans aren't supported by Azure Functions. For a lower-cost option hosting your function executions, you should instead consider the [Consumption plan](https://learn.microsoft.com/en-us/azure/azure-functions/consumption-plan), where you are billed based on function executions.


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/app-service-auto-scaling/#580ed5" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!caution]  
> Automatic Scaling is disabled when App Service web apps and Azure Function apps are in the same App Service Plan.

</div></div>

### App Service Hosting Plan
#### Always On

Must be enabled in the App Service Plan.
Otherwise the functions could go idle and stop, only a HttpTrigger can restart it again then.
### Azure Functions Consumption plan hosting


> [!info] 
>  The Consumption plan is the fully _serverless_ hosting option for Azure Functions.

#### Always On

In Consumption Plan always on is always enabled!