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
Source: [MS Graph: Authenticator Methods List Response](https://learn.microsoft.com/en-us/graph/api/microsoftauthenticatorauthenticationmethod-list?view=graph-rest-1.0&tabs=http#response-1)

## Get Method
| Method   | URI |
| :------- | :------- |
| GET | /me/authentication/microsoftAuthenticatorMethods/{microsoftAuthenticatorAuthenticationMethodId} |
| GET | /users/{id \| userPrincipalName}/authentication/microsoftAuthenticatorMethods/{microsoftAuthenticatorAuthenticationMethodId} |

### Example Response
```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.microsoftAuthenticatorAuthenticationMethod",
    "id": "6803c096-c096-6803-96c0-036896c00368",
    "displayName": "Sandeep's iPhone",
    "deviceTag": "",
    "phoneAppVersion": "6.5.4",
    "createdDateTime": "2020-12-03T23:16:12Z"
  }
}
```
Source: [MS Graph: Authenticator Get Method Response](https://learn.microsoft.com/en-us/graph/api/microsoftauthenticatorauthenticationmethod-get?view=graph-rest-1.0&tabs=http#response-1)

## Delete Method
| Method   | URI |
| :------- | :------- |
| DELETE | /me/authentication/microsoftAuthenticatorMethods/{microsoftAuthenticatorAuthenticationMethodId} |
| DELETE | /users/{id \| userPrincipalName}/authentication/microsoftAuthenticatorMethods/{microsoftAuthenticatorAuthenticationMethodId} |

### Example Response
```
HTTP/1.1 204 No Content
```
Source: [MS Graph: Authenticator Method Delete Response](https://learn.microsoft.com/en-us/graph/api/microsoftauthenticatorauthenticationmethod-delete?view=graph-rest-1.0&tabs=http#response-1)
