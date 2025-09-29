# Key Vault Endpoints
Resource: [Key Vault](https://learn.microsoft.com/en-us/rest/api/keyvault/?view=rest-keyvault-keyvault-2022-07-01)  
Base API URI: ```https://management.azure.com/subscriptions/{subscriptionId}```

## List
| Operation | Method | URI |
| :------- | :------- | :------- |
| List Vaults | GET  | /resources?$filter=resourceType eq 'Microsoft.KeyVault/vaults'&api-version=2025-04-01 |
| List Vaults with Optional Arguments | GET | /resources?$filter=resourceType eq 'Microsoft.KeyVault/vaults'&$top={$top}&api-version=2015-11-01 |
| List Vaults by Resource Group | GET | /resourceGroups/{resourceGroupName}/providers/Microsoft.KeyVault/vaults?api-version=2022-07-01 |
| List Vaults by Subscription | GET | /providers/Microsoft.KeyVault/vaults?api-version=2022-07-01 |
| Vaults - List Deleted | GET | /providers/Microsoft.KeyVault/deletedVaults?api-version=2022-07-01 |

## Get
| Operation | Method | URI |
| :------- | :------- | :------- |
| Vaults - Get | GET | /resourceGroups/{resourceGroupName}/providers/Microsoft.KeyVault/vaults/{vaultName}?api-version=2022-07-01 | 
| Vaults - Get Deleted | GET | /providers/Microsoft.KeyVault/locations/{location}/deletedVaults/{vaultName}?api-version=2022-07-01 |