# Microsoft Graph API Usage
## Foundational Concepts
- REST APIs: A REST API is an application programming interface (API) that follows the design principles of the REST architectural style. REST is short for representational state transfer, and is a set of rules and guidelines about how you should build a web API.
- OData Namespace: The Microsoft Graph API defines most of its resources, methods, and enumerations in the OData namespace, microsoft.graph, in the Microsoft Graph metadata. 
- Tokens: Tokens provide access to specific resources, which is defined by the 'scope' of the token.

## REST API Pattern
```
{HTTP method} https://graph.microsoft.com/{version}/{resource}?{query-parameters}
```
### HTTP Methods
GET: Read data from a resource.  
POST: Create a new resource, or perform an action.  
PATCH: Update a resource with new values, or upsert a resource (create if resource doesn't exist, update otherwise).  
PUT: Replace a resource with a new one.  
DELETE: Remove a resource.

- For the CRUD methods GET and DELETE, no request body is required.
- The POST, PATCH, and PUT methods require a request body, usually specified in JSON format, that contains additional information, such as the values for properties of the resource.

## Tokens
Tokens can be obtained after a session has been established for a user or service.  
Tokens are implemented using Java Web Tokens, which allows them to be decoded and analyzed.

## Request Response Patterns
### Using PowerShell
Obtain a token
```
$GraphAccessToken = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR((Get-AzAccessToken -ResourceTypeName MSGraph -AsSecureString).Token))
```

Call the 'List people' endpoint for the authenticated user (/me/people) and output the result
```
$URI = "https://graph.microsoft.com/v1.0/me/people"
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

# References
[Microsoft Graph: Use the API](https://learn.microsoft.com/en-us/graph/use-the-api)
