# Role Assignment Endpoints
Resource: [unifiedRoleAssignment resource type](https://learn.microsoft.com/en-us/graph/api/resources/unifiedroleassignment?view=graph-rest-1.0)  
Base API URI: ```https://graph.microsoft.com/v1.0/```

## List
| Method   | URI |
| :------- | :------- |
| GET | /roleManagement/directory/roleAssignments |
| GET | /roleManagement/entitlementManagement/roleAssignments |

### Optional Parameters
This method supports the $filter, $expand, and $select OData query parameters to help customize the response.

## Get
| Method   | URI |
| :------- | :------- |
| GET | /roleManagement/directory/roleAssignments/{id} |
| GET | /roleManagement/entitlementManagement/roleAssignments/{id} |

### Optional Parameters
This method supports th $select and $expand OData query parameters to help customize the response.