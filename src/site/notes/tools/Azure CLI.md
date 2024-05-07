---
{"status":"planted","dg-publish":true,"ms-learn-url":"(https://learn.microsoft.com/en-us/cli/azure/)","tags":["concept/SRE/cloud/azure","tool"],"definition":"Azure commanline tool to manage Azure resources","aliases":["az"],"creation_date":"2024-05-02 22:00","permalink":"/tools/azure-cli/","dgPassFrontmatter":true}
---



## Login

Basic login
    az login

On windows you can use the Web Broker

```
az config set core.enable_broker_on_windows=true
az account clear
az login
```

When no browser is availible or you don't want to use the browser, use device code flow
    az login --use-device-code
`
Account info
    az account show

## Example Create Virtual Machine

`az group create -name examplevmgroup -location eastus`

## Example Update Plan for Max Burst


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/app-service-auto-scaling/#setting-max-burst-with-azure-cli-az" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



##### Setting Max Burst with [[tools/Azure CLI\|az]]
```shell
az appservice plan update --name <APP_SERVICE_PLAN> --resource-group <RESOURCE_GROUP> --elastic-scale true --max-elastic-worker-count <YOUR_MAX_BURST>
```


</div></div>


## Example Update Plan for minimal instance

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/app-service-auto-scaling/#setting-minimal-instances-with-azure-cli-az" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



##### Setting minimal instances with [[tools/Azure CLI\|az]]
```shell
az webapp update --resource-group <RESOURCE_GROUP> --name <APP_NAME> --minimum-elastic-instance-count <ALWAYS_READY_COUNT>
```


</div></div>



## Extra notes

### [[Concepts/Azure CLI Extentions\|Azure CLI Extentions]]

### Azure CLI uses python packages for extentions

Ref: [link](https://github.com/Azure/azure-cli/tree/master)  
Notable python package wheel ( *.whl)

Format:
  chardet-3.0.4-py2.py3-none-any.whl  
You can break this down into its tags:

* chardet is the package name.
* 3.0.4 is the package version of chardet.
* py2.py3 is the Python tag, meaning the wheel supports Python 2 and 3 with any Python implementation.
* none is the ABI tag, meaning the ABI isn’t a factor. ABI stands for application binary interface.
* any is the platform. This wheel will work on virtually any platform.

Usage:  
```shell
az version  
az upgrade  
az extension update --name azure-devops --verbose
```
