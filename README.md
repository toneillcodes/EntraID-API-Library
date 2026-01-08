# Entra ID API Library
A collection of useful API endpoints and how to use them.
The majority of the information found here is well documented by Microsoft and poorly documented by myself.
> [!CAUTION]
> Disclaimer: Intended only for use on systems that you are legally authorized to access.
## Table of Contents
- [Microsoft API Fundamentals](fundamentals/microsoft-api-fundamentals.md)
  - [RESTful APIs](fundamentals/microsoft-api-fundamentals.md#restful-apis)
  - [Graph vs Azure Resource Manager](fundamentals/microsoft-api-fundamentals.md#microsoft-graph-vs-azure-resource-manager)
- [Usage](fundamentals/usage.md)
  - [Tokens](fundamentals/usage.md#tokens)
    - [Obtain a Token](fundamentals/usage.md#obtain-a-token) 
  - [Tools](fundamentals/usage.md#tools)
  - [Request Patterns](fundamentals/usage.md#request-patterns)
	  - [Graph API Pattern](fundamentals/usage.md#graph-api-pattern)
	  - [ARM API Pattern](fundamentals/usage.md#arm-api-pattern)
	  - [ARM Subdomains](fundamentals/usage.md#arm-subdomains)
	  - [HTTP Methods](fundamentals/usage.md#http-methods)
      - [Using PowerShell](fundamentals/usage.md#using-powershell)
      - [Using curl](fundamentals/usage.md#using-curl)
  - [References](fundamentals/usage.md#references)
- **Graph APIs**
  - **Identity and Sign-in**
    - [Authentication Methods](apis/graph/v1/authentication-methods.md)
    - [Microsoft Authenticator](apis/graph/v1/authenticator.md)
    - [Conditional Access Policies](apis/graph/v1/conditional-access-policies.md)
  - [People](apis/graph/v1/people.md)
  - [Roles](apis/graph/v1/roles.md)
    - [List](apis/graph/v1/roles.md#list)
    - [Get](apis/graph/v1/roles.md#get)
  - [Role Assignment](apis/graph/v1/role-assignment.md)
    - [List](apis/graph/v1/role-assignment.md#list)
    - [Get](apis/graph/v1/role-assignment.md#get)
  - [User](apis/graph/v1/user.md)
    - [List](apis/graph/v1/user.md#list)
    - [Get](apis/graph/v1/user.md#get)
    - [Change Password](apis/graph/v1/user.md#change-password)
  - [User Groups](apis/graph/v1/user-groups.md)
    - [List Joined Teams](apis/graph/v1/user-groups.md#list-teams)
    - [List Direct Memberships](apis/graph/v1/user-groups.md#list-direct-memberships)
    - [List Transitive Memberships](apis/graph/v1/user-groups.md#list-transitive-memberships)
  - [Group](apis/graph/v1/group.md)
    - [List](apis/graph/v1/group.md#list)
    - [Get](apis/graph/v1/group.md#get)
  - **Calendar**
    - [Calender]
      - [List](apis/graph/v1/calendar.md#list)
      - [Get](apis/graph/v1/calendar.md#get)
      - [List events](apis/graph/v1/calendar.md#list-events)
      - [Create event](apis/graph/v1/calendar.md#create-event)
      - [Get event]
      - [Update event]
      - [Delete](apis/graph/v1/calendar.md#delete)
  - **Files**
    - [File Storage Containers](apis/graph/v1/file-storage-containers.md)
    - [Recycle Bin](apis/graph/v1/recycle-bin.md)    
- **Azure Resource Manager (ARM) API**
  - [Resource Groups](apis/arm/resource-groups.md)
    - [List](apis/arm/resource-groups.md#list)
    - [Get](apis/arm/resource-groups.md#get)
  - [Resources](apis/arm/resources.md)
    - [List](apis/arm/resources.md#list)
    - [Get](apis/arm/resources.md#get)
  - [Key Vaults](apis/arm/key-vaults.md)
    - [Vaults](apis/arm/key-vaults.md)
      - [List](apis/arm/key-vaults.md#list)
      - [Get](apis/arm/key-vaults.md#get)
    - [Keys](apis/arm/vault-keys.md)
      - [List](apis/arm/vault-keys.md#list)
      - [Get](apis/arm/vault-keys.md#get)
      - [Recover](apis/arm/vault-keys.md#recover)
    - [Secrets](apis/arm/vault-secrets.md)
      - [List](apis/arm/vault-secrets.md#list)
      - [Get](apis/arm/vault-secrets.md#get)
      - [Recover](apis/arm/vault-secrets.md#recover)
    - [Certificates](apis/arm/vault-certificates.md)
      - [List](apis/arm/vault-certificates.md#list)
      - [Get](apis/arm/vault-certificates.md#get)
      - [Recover](apis/arm/vault-certificates.md#recover)
- **Web APIs**
  - **Reconnaissance**
    - [OpenID Connect (OIDC) Discovery](apis/web/recon/oidc-discovery.md)
    - [User Realm Discovery](apis/web/recon/user-realm-discovery.md)
# References
[Microsoft Graph REST API v1](https://learn.microsoft.com/en-us/graph/?view=graph-rest-1.0)  
[Microsoft Azure Resource Manager API](https://learn.microsoft.com/en-us/rest/api/resources/)
