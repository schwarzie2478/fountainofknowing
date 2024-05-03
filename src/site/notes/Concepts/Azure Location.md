---
{"dg-publish":true,"tags":["concept/SRE/cloud/azure"],"definition":"Regions covered by Azure datacenters locally","aliases":["Azure Region"],"creation_date":"2024-05-02 22:00","permalink":"/concepts/azure-location/","dgPassFrontmatter":true}
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

[[Concepts/Azure Resource Provider\|Azure Resource Provider]]

Output: [[Concepts/Azure Location Example Listing\|Azure Location Example Listing]]

