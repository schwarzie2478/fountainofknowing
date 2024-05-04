---
{"status":"planted","dg-publish":true,"tags":["concept/SRE/cloud/azure"],"type":"term","definition":"An functional account credential to provide non-interactive access to resources.","ms-learn-url":"(https://learn.microsoft.com/en-us/cli/azure/azure-cli-sp-tutorial-1?tabs=bash)","creation_date":"2024-05-02 22:00","permalink":"/concepts/service-principle/","dgPassFrontmatter":true}
---



Often used in scripts

[[Concepts/AZ Powershell Module\|AZ Powershell Module]]:

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/az-powershell-module/#325307" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!important] 
> Beginning with Az PowerShell module version 7.x, [New-AzADServicePrincipal](https://learn.microsoft.com/en-us/powershell/module/Az.Resources/New-AzADServicePrincipal) no longer assigns the [Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#contributor) role to the service principal by default. To assign a specific role to a service principal, see [Steps to add a role assignment](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-steps).

</div></div>


[[tools/Azure CLI\|Azure CLI]]
> [!example] 
> az login --service-principal -u <app-id> -p <password-or-cert> --tenant <tenant>
