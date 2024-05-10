---
{"status":"planted","dg-publish":true,"tags":["concept/SRE/cloud/azure"],"ms-learn-url":"https://learn.microsoft.com/en-us/azure/architecture/best-practices/background-jobs#azure-web-apps-and-webjobs","creation_date":"2024-05-02 22:00","definition":"You can use Azure WebJobs to execute custom jobs as background tasks within an Azure Web App.","permalink":"/concepts/azure-app-service-web-jobs/","dgPassFrontmatter":true}
---

| MetaData   |                                              |
| ---------- | -------------------------------------------- |
| Definition | `VIEW[{definition}][text(renderMarkdown)]`   |
| Homesite   | `VIEW[{url}][text(renderMarkdown)]`          |
| MS Learn   | `VIEW[{ms-learn-url}][text(renderMarkdown)]` |

Uses  [[Code/Azure Webjob SDK\|Azure Webjob SDK]]
Similar to [[Concepts/Azure Functions\|Azure Functions]] but,

## WebJobs are a better solution when:

- You want the code to be a part of an existing [[Concepts/Azure Web App\|Azure Web App]] and to be managed as part of that application, for example in the same [[Concepts/Azure DevOps\|Azure DevOps]] environment.
- You need close control over the object that listens for events that trigger the code.


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/azure-functions/#difference-with-azure-app-service-web-jobs" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



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

</div></div>
 

> [!tip]
> To minimize the impact of jobs on the performance of the web app, consider creating an empty [[Concepts/Azure Web App\|Azure Web App]] instance in a new App Service plan to host long-running or resource-intensive WebJobs.
> 

## Configuring
- Run on demand
- Run on shedule
- Run continuously


