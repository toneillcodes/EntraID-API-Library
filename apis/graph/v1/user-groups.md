# User Groups Endpoints
Resource: [group resource type](https://learn.microsoft.com/en-us/graph/api/resources/group?view=graph-rest-1.0)  
Base API URI: ```https://graph.microsoft.com/v1.0/```

## List Teams
Get the teams in Microsoft Teams that the user is a direct member of.
| Operation | Method | URI |
| :------- | :------- | :------- |
| List joinedTeams for the current user | GET | /me/joinedTeams |
| List joinedTeams for a user | GET | /users/{id \| user-principal-name}/joinedTeams |
Source: [MS Graph: User Groups Joined Teams](https://learn.microsoft.com/en-us/graph/api/user-list-joinedteams?view=graph-rest-1.0&tabs=http)

### Example Response
```
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "172b0cce-e65d-44ce-9a49-91d9f2e8493a",
      "displayName": "Contoso Team",
      "description": "This is a Contoso team, used to showcase the range of properties supported by this API"
    }
  ]
}
```

## List Direct Memberships
Get groups, directory roles, and administrative units that the user is a direct member of.
| Operation | Method | URI |
| :------- | :------- | :------- |
| List direct memberships for the current user | GET | /me/memberOf |
| List direct memberships for a given user | GET | /users/{id \| userPrincipalName}/memberOf |
Source: [MS Graph: User Groups Direct Memberships](https://learn.microsoft.com/en-us/graph/api/user-list-memberof?view=graph-rest-1.0&tabs=http)

### Example Response
```
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.group",
      "displayName": "All Users",
      "mailEnabled": false,
      "securityEnabled": true
    }
  ]
}
```

## List Transitive Memberships
Get groups, directory roles, and administrative units that the user is a member of through either direct or transitive membership.
| Operation | Method | URI |
| :------- | :------- | :------- |
| List memberships (direct and transitive) for the current user | GET /me/transitiveMemberOf |
| List memberships (direct and transitive) for a given user | GET /users/{id \| userPrincipalName}/transitiveMemberOf |
Source: [MS Graph: User Groups List Transitive Membership](https://learn.microsoft.com/en-us/graph/api/user-list-transitivememberof?view=graph-rest-1.0&tabs=http)

### Example Response
```
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#directoryObjects",
  "value":[
    {
      "@odata.type":"#microsoft.graph.group",
      "displayName":"All_Contoso_Licensing",
      "mailEnabled":true,
      "mailNickname":"ContosoMailNickName",
      "securityEnabled":true
    }
  ]
}
```