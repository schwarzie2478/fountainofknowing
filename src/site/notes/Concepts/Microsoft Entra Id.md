---
{"status":"planted","dg-publish":true,"tags":["concept/SRE/cloud/azure"],"aliases":["AAD"],"definition":"Azure Identity Management service, previously known as Azure Active Directory","ms-learn-url":"https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles","creation_date":"2024-05-02 22:00","permalink":"/concepts/microsoft-entra-id/","dgPassFrontmatter":true}
---


## General

|Built-in role|Description|ID|
|---|---|---|
|[Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/general#contributor)|Grants full access to manage all resources, but does not allow you to assign roles in Azure RBAC, manage assignments in Azure Blueprints, or share image galleries.|b24988ac-6180-42a0-ab88-20f7382dd24c|
|[Owner](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/general#owner)|Grants full access to manage all resources, including the ability to assign roles in Azure RBAC.|8e3af657-a8ff-443c-a75c-2fe8c4bcb635|
|[Reader](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/general#reader)|View all resources, but does not allow you to make any changes.|acdd72a7-3385-48ef-bd42-f606fba81ae7|
|[Role Based Access Control Administrator](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/general#role-based-access-control-administrator)|Manage access to Azure resources by assigning roles using Azure RBAC. This role does not allow you to manage access using other ways, such as Azure Policy.|f58310d9-a9f6-439a-9e8d-f62e7b41a168|
|[User Access Administrator](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/general#user-access-administrator)|Lets you manage user access to Azure resources.|18d7d88d-d35e-4fb5-a5c3-7773c20a72d9|



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/microsoft-entra-id-privileged-role/#1175cd" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

<div class="markdown-embed-title">

# About Privilegde Roles

</div>


> [!warning] 
> Privileged role assignments can lead to elevation of privilege if not used in a secure and intended manner.

</div></div>



> [!info]
> In a Microsoft Entra ID directory where user setting **Users can register applications** has been set to **No**, you must be a member of one of the following Microsoft Entra ID built-in roles (which have the action: `microsoft.directory/applications/createAsOwner` or `microsoft.directory/applications/create`):
> 
> - [Application Developer](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference#application-developer)
> - [Application Administrator](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference#application-administrator)
> - [Cloud Application Administrator](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference#cloud-application-administrator)
> - [Global Administrator](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference#global-administrator)
> - [Hybrid Identity Administrator](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference#hybrid-identity-administrator)
