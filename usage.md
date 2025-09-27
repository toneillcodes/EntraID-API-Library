# API Usage

## Tokens
- Tokens can be obtained after a session has been established for a user or service.  
- Tokens have a 'scope' that indicates what permissions the caller has when using the token.  
- A specific scope can be requested by the client application during the initial authentication process.  
- Tokens are implemented using Java Web Tokens (JWT), which allows them to be decoded and analyzed.

### Obtain a Token
#### Get-AzAccessToken
Optional resource type name, supported values: AadGraph, AnalysisServices, AppConfiguration, Arm, Attestation, Batch, CommunicationEmail, DataLake, KeyVault, MSGraph, OperationalInsights, ResourceManager, Storage, Synapse. **Default value is Arm if not specified**.
#### Graph Token with MSGraph
```
$GraphAccessToken = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR((Get-AzAccessToken -ResourceTypeName MSGraph -AsSecureString).Token))
```

## Tools
- PowerShell
- curl
- Bruno: This is my current favorite GUI-based tool for interacting with APIs. There are other options - use whichever you prefer and works best for your workflow.  
  - "Bruno is a Git-friendly and offline-first open-source API client aimed at revolutionizing the status quo represented by tools like Postman and Insomnia." Source: [What Is Bruno?](https://docs.usebruno.com/)

## Request Patterns

### Graph API Pattern
```
{HTTP method} https://graph.microsoft.com/{version}/{resource}?{query-parameters}
```
### ARM API Pattern
```
{HTTP method} https://{resource-base-uri}/{resource-path}?{query-string}
```

### ARM Subdomains
Unlike Graph, the ARM APIs are spread across multiple subdomains.  
This is not a comprehensive table, but lists some relevant subdomains along with a brief description of their purpose.

| Azure Service	| Example Subdomain Pattern	| Purpose |
| :------- | :------- | :------- |
| Azure Management (General)	| *.management.azure.com | 	Primary endpoint for ARM and most Azure management operations. |
| Resource Provider Operations	| {provider-name}.{region}.resource.azure.com | 	Specific endpoints for some resource provider operations (less common than the primary ARM endpoint). |
| Azure Key Vault	| *.vault.azure.net | 	Used for Key Vault operations (data plane). |
| Azure Storage	| *.blob.core.windows.net, *.table.core.windows.net, *.queue.core.windows.net, *.file.core.windows.net| 	Used for storage operations (data plane). |
| Azure API Management	| *.azure-api.net | 	Default domain for the API Gateway and Developer Portal of an API Management instance. |
| Azure Websites/App Services	| *.azurewebsites.net | 	Default domains for hosted web apps. |

Source: [Azure Domains](https://learn.microsoft.com/en-us/azure/security/fundamentals/azure-domains)

### HTTP Methods
GET: Read data from a resource.  
POST: Create a new resource, or perform an action.  
PATCH: Update a resource with new values, or upsert a resource (create if resource doesn't exist, update otherwise).  
PUT: Replace a resource with a new one.  
DELETE: Remove a resource.

- For the CRUD methods GET and DELETE, no request body is required.
- The POST, PATCH, and PUT methods require a request body, usually specified in JSON format, that contains additional information, such as the values for properties of the resource.

### Using PowerShell

Call the 'List users' endpoint (/me/users) and output the result
```
$URI = "https://graph.microsoft.com/v1.0/me/users"
$RequestParams = @{
	Method = 'GET'
	Uri = $URI
	Headers = @{
		'Authorization' = "Bearer $GraphAccessToken" 
	}
	ContentType = "application/json"
}
$ApiResult = Invoke-RestMethod @RequestParams
$ApiResult
```

### Using curl
```
$ curl  -H "Authorization: Bearer $GraphAccessToken" -H 'Content-Type: application/json' -X GET 'https://graph.microsoft.com/v1.0/users'
```

# References
[Microsoft Graph: Use the API](https://learn.microsoft.com/en-us/graph/use-the-api)
