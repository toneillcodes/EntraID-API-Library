# Resource Groups Endpoints
Resource: [Resource Groups](https://learn.microsoft.com/en-us/rest/api/resources/resource-groups?view=rest-resources-2021-04-01)  
Base API URI: ```https://management.azure.com/subscriptions/{subscriptionId}```

## List
| Operation | Method | URI |
| :------- | :------- | :------- |
| Gets all the resource groups for a subscription | GET | /resourcegroups?api-version=2021-04-01 |
| Gets all the resource groups for a subscription with options | GET | /resourcegroups?$filter={$filter}&$top={$top}&api-version=2021-04-01 |
Source: [MS ARM: Resource Groups List](https://learn.microsoft.com/en-us/rest/api/resources/resource-groups/list?view=rest-resources-2021-04-01)

### Response
ResourceGroupListResult - List of resource groups.
| Name | Type | Description |
| :------- | :------- | :------- |
| nextLink | string | The URL to use for getting the next set of results. |
| value | ResourceGroup[] | An array of resource groups. |
Source: [MS ARM: Resource Groups RersourceGroupListResult](https://learn.microsoft.com/en-us/rest/api/resources/resource-groups/list?view=rest-resources-2021-04-01#resourcegrouplistresult)

## Get
| Operation | Method | URI |
| :------- | :------- | :------- |
| Gets a resource group. | GET | /resourcegroups/{resourceGroupName}?api-version=2021-04-01 |
Source: [MS ARM: Resource Groups Get](https://learn.microsoft.com/en-us/rest/api/resources/resource-groups/get?view=rest-resources-2021-04-01)