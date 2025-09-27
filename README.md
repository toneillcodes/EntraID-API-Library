# Entra ID Offensive API Endpoints
A collection of useful API endpoints and how to use them.
> [!CAUTION]
> Disclaimer: Intended only for use on systems that you are legally authorized to access.
## Table of Contents
- [Microsoft API Fundamentals](microsoft-api-fundamentals.md)
  - [RESTful APIs](microsoft-api-fundamentals.md#restful-apis)
  - [Graph vs Azure Resource Manager](microsoft-api-fundamentals.md#microsoft-graph-vs-azure-resource-manager)
- [Usage](usage.md)
  - API Patterns
	  - [Graph API Pattern](usage.md#graph-api-pattern)
	  - [ARM API Pattern](usage.md#arm-api-pattern)
	  - [ARM Subdomains](usage.md#arm-subdomains)
	  - [HTTP Methods](usage.md#http-methods)
  - [Tokens](usage.md#tokens)
    - [Obtain a Token](usage.md#obtain-a-token)
  - [Tools](usage.md#tools)
  - [Request Response Patterns](usage.md#request-response-patterns)
  - [References](usage.md#references)
- Graph APIs
  - Identity and Sign-in
    - [Authentication Methods](apis/graph/v1/authentication-methods.md)
    - [Microsoft Authenticator](apis/graph/v1/authenticator.md)
    - [Conditional Access Policies](apis/graph/v1/conditional-access-policies.md)
  - [People](apis/graph/v1/people.md)
  - [Roles](apis/graph/v1/roles.md)
  - Files
    - [File Storage Containers](apis/graph/v1/file-storage-containers.md)
    - [Recycle Bin](apis/graph/v1/recycle-bin.md)
  - [User](apis/graph/v1/user.md)
- Azure Resource Manager (ARM) APIs
  - Key Vault
    - Certificates
    - Vaults
    - Keys
    - Secrets
- Web APIs
  - Recon
    - [OpenID Connect (OIDC) Discovery](apis/web/recon/oidc-discovery.md)
    - [User Realm Discovery](apis/web/recon/user-realm-discovery.md)
# References
[Microsoft Graph REST API v1](https://learn.microsoft.com/en-us/graph/?view=graph-rest-1.0)  
[Microsoft Azure Resource Manager API](https://learn.microsoft.com/en-us/rest/api/resources/)
