# Group Endpoints
Resource: [group resource type](https://learn.microsoft.com/en-us/graph/api/resources/group?view=graph-rest-1.0)  
Base API URI: ```https://graph.microsoft.com/v1.0/```

## List
Get the teams in Microsoft Teams that the user is a direct member of.
| Method | URI |
| :------- | :------- |
| GET | /groups |
Source: [MS Graph: List groups](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0&tabs=http)

## Get
| Method | URI |
| :------- | :------- |
| GET | /groups/{id} |
Source: [MS Graph: Get group](https://learn.microsoft.com/en-us/graph/api/group-get?view=graph-rest-1.0&tabs=http)

### Request Parameters
You can use $select to get specific group properties, including those that aren't returned by default.