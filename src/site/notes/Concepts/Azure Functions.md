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

> [!attention]
> Support for in-process functions is ending in November 2026

> [!NOTE]
> Migrate .NET apps from the in-process model to the isolated worker model

Azure Functions supports [[Concepts/Azure Function triggers\|triggers]], which are ways to start execution of your code, and [[Concepts/Azure Function Bindings\|bindings]], which are ways to simplify coding for input and output data. There are other integration and automation services in Azure and they all can solve integration problems and automate business processes. They can all define input, actions, conditions, and output.

## Difference with [[Concepts/Azure Logic Apps\|Azure Logic Apps]]

|                   | Azure Functions                                                       | Logic Apps                                                                                             |
| ----------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Development       | Code-first (imperative)                                               | Designer-first (declarative)                                                                           |
| Connectivity      | About a dozen built-in binding types, write code for custom bindings  | Large collection of connectors, Enterprise Integration Pack for B2B scenarios, build custom connectors |
| Actions           | Each activity is an Azure function; write code for activity functions | Large collection of ready-made actions                                                                 |
| Monitoring        | [[Azure Application Insights\|Azure Application Insights]]                                        | Azure portal, Azure Monitor logs                                                                       |
| Management        | REST API, Visual Studio                                               | Azure portal, REST API, PowerShell, Visual Studio                                                      |
| Execution context | Runs in Azure, or locally                                             | Runs in Azure, locally, or on premises                                                                 |
## Difference with [[Concepts/Azure App Service WebJobs\|Azure App Service WebJobs]]

> [!info]
> Azure Functions is built on the [[Code/Azure Webjob SDK\|Azure Webjob SDK]], so it shares many of the same event triggers and connections to other Azure services.

|                                                     | Functions                                                                                                                                                                                     | [[Concepts/Azure App Service WebJobs\|Azure App Service WebJobs]] with [[Code/Azure Webjob SDK\|Azure Webjob SDK]]                                                                                                       |
| --------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [[Serverless\|Serverless]] app model with [[automatic scaling\|automatic scaling]] | Yes                                                                                                                                                                                           | No                                                                                                                                                            |
| Develop and test in browser                         | Yes                                                                                                                                                                                           | No                                                                                                                                                            |
| [[Pay-per-use\|Pay-per-use]] pricing                             | Yes                                                                                                                                                                                           | No                                                                                                                                                            |
| Integration with [[Concepts/Azure Logic Apps\|Azure Logic Apps]]               | Yes                                                                                                                                                                                           | No                                                                                                                                                            |
| [[Trigger events\|Trigger events]]                                  | Timer  <br>Azure Storage queues and blobs  <br>Azure Service Bus queues and topics  <br>Azure Cosmos DB  <br>[[Azure Event Hubs\|Azure Event Hubs]]  <br>HTTP/WebHook (GitHub  <br>Slack)  <br>Azure Event Grid | Timer  <br>[[Azure Storage queue\|Azure Storage queue]] and [[blobs\|blobs]]  <br>[[Concepts/Azure Service Bus\|Azure Service Bus]] queues and topics  <br>[[unsorted/Azure Cosmos DB\|Azure Cosmos DB]]  <br>Azure Event Hubs  <br>File system |
|                                                     |                                                                                                                                                                                               |                                                                                                                                                               |
## Hosting Plans

Reference: [MS Learn](https://learn.microsoft.com/en-us/azure/azure-functions/dedicated-plan)

| Plan                                                | Benefits                                                                                                                                                                                                                                    |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[[Concepts/Azure Functions Consumption plan hosting\|Azure Functions Consumption plan hosting]]**    | This is the default hosting plan. It scales automatically and you only pay for compute resources when your functions are running. Instances of the Functions host are dynamically added and removed based on the number of incoming events. |
| **[[Concepts/Azure Functions Premium plan\|Azure Functions Premium plan]]**                | Automatically scales based on demand using pre-warmed workers, which run applications with no delay after being idle, runs on more powerful instances, and connects to virtual networks.                                                    |
| **[[Concepts/Dedicated hosting plans for Azure Functions\|Dedicated hosting plans for Azure Functions]]** | Run your functions within an [[Concepts/Azure App Service Plan\|Azure App Service Plan]] at regular App Service plan rates. Best for long-running scenarios where [[Concepts/Azure Durable Functions\|Azure Durable Functions]] can't be used.                                                                 |

> [!important] 
> Free and Shared tier App Service plans aren't supported by Azure Functions. For a lower-cost option hosting your function executions, you should instead consider the [Consumption plan](https://learn.microsoft.com/en-us/azure/azure-functions/consumption-plan), where you are billed based on function executions.


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/app-service-auto-scaling/#580ed5" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!caution]  
> Automatic Scaling is disabled when App Service web apps and Azure Function apps are in the same App Service Plan.

</div></div>



  There are two other hosting options, which provide the ==highest amount of control and isolation== in which to run your function apps.

| Hosting option                                                                                                                                                                                                                             | Details                                                                                                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[[Concepts/Application Service Environment\|ASE]]**                                                                                                                                                                                               | [App Service Environment (ASE)](https://learn.microsoft.com/en-us/azure/app-service/environment/intro) is an App Service feature that provides a fully isolated and dedicated environment for securely running App Service apps at high scale. |
| [[Concepts/Azure Functions on Kubernetes\|Azure Functions on Kubernetes]] ([Direct](https://learn.microsoft.com/en-us/azure/azure-functions/functions-kubernetes-keda) or [Azure Arc](https://learn.microsoft.com/en-us/azure/app-service/overview-arc-integration) [[Concepts/Azure Arc\|Azure Arc]]) | [[Concepts/Kubernetes\|Kubernetes]] provides a fully isolated and dedicated environment running on top of the Kubernetes platform.                                                                                                                                  |
## Function app timeout duration

> [!NOTE]
> The `functionTimeout` property in the _host.json_ project file specifies the timeout duration for functions in a function app.
> 


| Plan             | Default | Maximum   |
| ---------------- | ------- | --------- |
| Consumption plan | 5       | 10        |
| Premium plan     | 30      | Unlimited |
| Dedicated plan   | 30      | Unlimited |
## Storage account requirements

On any plan, a function app requires a general [[Concepts/Azure Storage Account\|Azure Storage Account]] , which supports Azure Blob, Queue, Files, and Table storage. This is because Functions rely on Azure Storage for operations such as managing triggers and logging function executions, but some storage accounts don't support queues and tables.

Function code files are stored on Azure files shares on the function's main storage account.

## Scale Azure Functions 

> [!info]
> Each instance of the Functions host in the Consumption plan is limited to 1.5 GB of memory and one CPU.

### Runtime scaling

Azure Functions uses a component called the _[[Concepts/scale controller\|scale controller]]_ to monitor the rate of events and determine whether to scale out or scale in. The scale controller uses heuristics for each trigger type. For example, when you're using an [[Concepts/Azure Queue storage\|Azure Queue storage]] trigger, it scales based on the queue length and the age of the oldest queue message.

> [!NOTE]
> The [[unit of scale\|unit of scale]] for Azure Functions is the function app. 

When the function app is scaled out, more resources are allocated to run multiple instances of the Azure Functions host. Conversely, as compute demand is reduced, the scale controller removes function host instances. The number of instances is eventually "scaled in" to zero when no functions are running within a function app.
![central-listener.png](/img/user/images/central-listener.png)

> [!attention]
> After your function app has been idle for a number of minutes, the platform may scale the number of instances on which your app runs in to zero. The next request has the added latency of scaling from zero to one. This latency is referred to as a _[[Concepts/cold start\|cold start]]_.

### Scaling behaviors

Scaling can vary on many factors, and scale differently based on the trigger and language selected. There are a few intricacies of scaling behaviors to be aware of:

#### **Maximum instances:** 

> [!NOTE]
> A single function app only scales out to a maximum of 200 instances.
 
 A single instance may process more than one message or request at a time though, so there isn't a set limit on number of concurrent executions.
    
#### **New instance rate:** 

> [!NOTE] Title
> Contents
For HTTP triggers, new instances are allocated, at most, ==once per second==. 

> [!NOTE]
> For non-HTTP triggers, new instances are allocated, at most, ==once every 30 seconds==.
>     

### Limit scale-out

You may wish to restrict the maximum number of instances an app used to scale out. This is most common for cases where a downstream component like a database has limited throughput. By default 
- Consumption plan functions scale out to as many as 200 instances
- Premium plan functions scales out to as many as 100 instances. 

> [!NOTE]
> You can specify a lower maximum for a specific app by modifying the `functionAppScaleLimit` value. 

The `functionAppScaleLimit` can be set to `0` or `null` for unrestricted, or a valid value between `1` and the app maximum.
## Always On

Must be enabled in the App Service Plan.
Otherwise the functions could go idle and stop, only a HttpTrigger can restart it again then.


> [!info] 
>  The Consumption plan is the fully _serverless_ hosting option for Azure Functions.
> In Consumption Plan always on is always enabled!

