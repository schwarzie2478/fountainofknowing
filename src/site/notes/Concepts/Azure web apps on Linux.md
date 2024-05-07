---
{"status":"planted","dg-publish":true,"tags":["concept/SRE/cloud/azure"],"creation_date":"2024-05-05 08:51","definition":"undefined","ms-learn-url":"undefined","url":"undefined","permalink":"/concepts/azure-web-apps-on-linux/","dgPassFrontmatter":true}
---


| MetaData   |                                              |
| ---------- | -------------------------------------------- |
| Definition | `VIEW[{definition}][text(renderMarkdown)]`   |
| Homesite   | `VIEW[{url}][text(renderMarkdown)]`          |
| MS Learn   | `VIEW[{ms-learn-url}][text(renderMarkdown)]` |
You can deploy to [[Concepts/Azure Web App\|Azure Web App]]
But take note of this:

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/azure-app-service-on-linux/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




### Limitations

App Service on Linux does have some limitations:

- App Service on Linux isn't supported on [[Concepts/Azure App Service Plan#^cb1520\|Shared pricing tier]].
- The Azure portal shows only features that currently work for Linux apps.
- When deployed to built-in images, your code and content are allocated a storage volume for web content, backed by Azure Storage. **The disk latency of this volume is higher and more variable than the latency of the container filesystem**. Apps that require heavy read-only access to content files may benefit from the custom container option, which places files in the container filesystem instead of on the content volume.



</div></div>

