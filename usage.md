# API Usage

## Tools
- PowerShell
- curl
- Bruno: This is my current favorite GUI-based tool for interacting with APIs. There are other options - use whichever you prefer and works best for your workflow.  
  - "Bruno is a Git-friendly and offline-first open-source API client aimed at revolutionizing the status quo represented by tools like Postman and Insomnia." Source: [What Is Bruno?](https://docs.usebruno.com/)

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
### Obtain a token
```
$GraphAccessToken = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR((Get-AzAccessToken -ResourceTypeName MSGraph -AsSecureString).Token))
```

### Using PowerShell

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

### Using curl
```
$ curl  -H "Authorization: Bearer $GraphAccessToken" -H 'Content-Type: application/json' -X GET 'https://graph.microsoft.com/v1.0/me/people'
```

# References
[Microsoft Graph: Use the API](https://learn.microsoft.com/en-us/graph/use-the-api)
