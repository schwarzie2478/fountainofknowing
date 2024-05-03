---
{"dg-publish":true,"tags":["concept/SRE/cloud/azure"],"type":"term","definition":"An functional account credential to provide non-interactive access to resources.","ms-learn-url":"(https://learn.microsoft.com/en-us/cli/azure/azure-cli-sp-tutorial-1?tabs=bash)","creation_date":"2024-05-02 22:00","permalink":"/concepts/service-principle/","dgPassFrontmatter":true}
---



Often used in scripts

[[Concepts/AZ Powershell Module\|AZ Powershell Module]]:
> [!important] 
> [[Concepts/AZ Powershell Module#^325307\| About creating Service Credentials with Powershell]]

[[Concepts/Azure CLI\|Azure CLI]]
> [!example] 
> az login --service-principal -u <app-id> -p <password-or-cert> --tenant <tenant>