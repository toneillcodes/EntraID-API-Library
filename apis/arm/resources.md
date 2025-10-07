# Resources Endpoints
Resource: [Resources](https://learn.microsoft.com/en-us/rest/api/resources/resources?view=rest-resources-2021-04-01)  
Base API URI: ```https://management.azure.com/subscriptions/{subscriptionId}```

## List
| Operation | Method | URI |
| :------- | :------- | :------- |
| Gets all the resources in a subscription | GET | /resources?api-version=2021-04-01 |
| Gets all the resources in a specific resource group | GET | /resourceGroups/{resourceGroupName}/resources?api-version=2021-04-01 |

## Get
| Operation | Method | URI |
| :------- | :------- | :------- |
| Gets a resource by name | GET | /resourcegroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{parentResourcePath}/{resourceType}/{resourceName}?api-version=2021-04-01 |
| Gets a resource by ID | GET | https://management.azure.com/{resourceId}?api-version=2021-04-01 |


