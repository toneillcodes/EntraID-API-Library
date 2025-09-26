# User Endpoints

Base URI: ```https://graph.microsoft.com/v1.0/```

## List
| Method   | URI |
| :------- | :------- |
| GET | /users |

### Query Parameters
This method supports the $count, $expand, $filter, $orderby, $search, $select, and $top OData query parameters to help customize the response. $skip isn't supported

### References
[MS Graph: User List](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0&tabs=http)  
[MS Graph: User List Query Parameters](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0&tabs=http#optional-query-parameters)

## Get
| Method   | URI |
| :------- | :------- |
| GET | /me |
| GET | /users/{id \| userPrincipalName} |

### Query Parameters
This method supports the $select OData query parameter to retrieve specific user properties, including those not returned by default.

[MS Graph: User Get](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0&tabs=http)  
[MS Graph: User Get Query Parameters](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0&tabs=http#optional-query-parameters)
