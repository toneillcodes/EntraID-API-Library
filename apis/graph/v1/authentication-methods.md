# Authentication Methods Endpoints
Base URI: ```https://graph.microsoft.com/v1.0/```

## List Authentication Methods
| Method   | URI |
| :------- | :------- |
| GET | /me/authentication/methods |
| GET  | /users/{id \| userPrincipalName}/authentication/methods |

### Example Response
If successful, this method returns a 200 OK response code and a collection of authenticationMethod objects in the response body.
```
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.fido2AuthenticationMethod",
      "id": "-2_GRUg2-HYz6_1YG4YRAQ2",
      "displayName": "Red key",
      "creationDateTime": "2020-08-10T06:44:09Z",
      "aaGuid": "2fc0579f-8113-47ea-b116-555a8db9202a",
      "model": "NFC key",
      "attestationCertificates": [
          "dbe793efdf1945e2df25d93653a1e8a3268a9075"
      ],
      "attestationLevel": "attested"
    },
    {
    "@odata.type": "#microsoft.graph.windowsHelloForBusinessAuthenticationMethod",
    "id": "b5e01f81-1f81-b5e0-811f-e0b5811fe0b5",
    "displayName": "Jordan's Surface Book",
    "createdDateTime": "2020-11-27T23:12:49Z",
    "keyStrength": "normal"
    }
  ]
}
```
Source: [MS Graph: Authentication Methods List Response](https://learn.microsoft.com/en-us/graph/api/authentication-list-methods?view=graph-rest-1.0&tabs=http#response-1)
