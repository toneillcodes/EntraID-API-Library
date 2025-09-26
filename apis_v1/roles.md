# Role Endpoints
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
