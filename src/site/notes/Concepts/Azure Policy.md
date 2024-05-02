---
{"dg-publish":true,"permalink":"/concepts/azure-policy/","tags":["concept/SRE/cloud/azure"]}
---



Used by [[Concepts/Azure Role Based Access Control\|Azure Role Based Access Control]]

[[Concepts/Policy Definition\|Policy definitions]] are combined in [[Concepts/Policy Initiative\|policy initiatives]] a.k.a. [[Concepts/Policy Set\|policy sets]].
Once defined they are assigned to a scope:
- [[Concepts/Azure Management groups\|Azure Management groups]]
- [[Concepts/Azure Resource Group\|Azure Resource Group]]
- [[Concepts/Azure Subscription\|Azure Subscription]]

Azure Policy has several permissions, known as operations, in two [[Concepts/Azure Resource Provider\|Resource Providers]]:
- [Microsoft.Authorization](https://learn.microsoft.com/en-us/azure/role-based-access-control/resource-provider-operations#microsoftauthorization)
- [Microsoft.PolicyInsights](https://learn.microsoft.com/en-us/azure/role-based-access-control/resource-provider-operations#microsoftpolicyinsights)
