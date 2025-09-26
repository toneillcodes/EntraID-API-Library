# Authenticator Endpoints
Base URI: ```https://graph.microsoft.com/v1.0/```

## List Methods
| Method   | URI |
| :------- | :------- |
| GET | /me/authentication/microsoftAuthenticatorMethods |
| GET | /users/{id \| userPrincipalName}/authentication/microsoftAuthenticatorMethods |

### Example Response
```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.microsoftAuthenticatorAuthenticationMethod",
      "id": "6803c096-c096-6803-96c0-036896c00368",
      "displayName": "Sandeep's iPhone",
      "deviceTag": "",
      "phoneAppVersion": "6.5.4",
      "createdDateTime": "2020-12-03T23:16:12Z"
    }
  ]
}
```
Source: [MS Graph: Authenticator Methods List](https://learn.microsoft.com/en-us/graph/api/microsoftauthenticatorauthenticationmethod-list?view=graph-rest-1.0&tabs=http#response-1)
