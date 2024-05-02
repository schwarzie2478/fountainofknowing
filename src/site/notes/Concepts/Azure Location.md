---
{"dg-publish":true,"permalink":"/concepts/azure-location/","tags":["concept/SRE/cloud/azure"]}
---


## How to get all possible locations for your subscription
[[Concepts/Azure CLI\|Azure CLI]]:

```
az account list-locations -o table
```
[[Concepts/AZ Powershell Module\|AZ Powershell Module]]
```powershell
Get-AzLocation | select Location
```

[[Concepts/Azure Resource Provider\|Azure Resource Provider]] Namespace : Microsoft.Storage

Output: [[Concepts/Azure Location Example Listing\|Azure Location Example Listing]]

