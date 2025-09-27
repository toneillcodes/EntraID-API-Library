# Role Endpoints
Resource: [unifiedRoleDefinition resource type](https://learn.microsoft.com/en-us/graph/api/resources/unifiedroledefinition?view=graph-rest-1.0)  
Base URI: ```https://graph.microsoft.com/v1.0/```

## List
| Method   | URI |
| :------- | :------- |
| GET | /roleManagement/directory/roleDefinitions |
| GET | /roleManagement/entitlementManagement/roleDefinitions |

### Query Parameters
This method supports the $filter (eq and in operators) OData query parameter on id, displayName, and isBuiltIn properties. It also supports $expand on the relationships. 

### References
[MS Graph: List roleDefinitions](https://learn.microsoft.com/en-us/graph/api/rbacapplication-list-roledefinitions?view=graph-rest-1.0&tabs=http)  
[MS Graph: List roleDefinitions Query Parameters](https://learn.microsoft.com/en-us/graph/api/rbacapplication-list-roledefinitions?view=graph-rest-1.0&tabs=http#optional-query-parameters)  
[MS Graph: List roleDefinitions Permissions](https://learn.microsoft.com/en-us/graph/api/rbacapplication-list-roledefinitions?view=graph-rest-1.0&tabs=http#permissions)

## Get
| Method   | URI |
| :------- | :------- |
| GET | /roleManagement/directory/roleDefinitions/{id} |
| GET | /roleManagement/entitlementManagement/roleDefinitions/{id} |

### Query Parameters
This method supports the $select OData query parameter to help customize the response.
### References
[MS Graph: get roleDefintion](https://learn.microsoft.com/en-us/graph/api/unifiedroledefinition-get?view=graph-rest-1.0&tabs=http)  
[MS Graph: get roleDefintion Query Parameters](https://learn.microsoft.com/en-us/graph/api/unifiedroledefinition-get?view=graph-rest-1.0&tabs=http#optional-query-parameters)  
[MS Graph: get roleDefintion Permissions](https://learn.microsoft.com/en-us/graph/api/unifiedroledefinition-get?view=graph-rest-1.0&tabs=http#permissions)

