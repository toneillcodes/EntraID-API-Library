# Vault Key Endpoints
Resource: [Vault Keys](https://learn.microsoft.com/en-us/rest/api/keyvault/keys/operation-groups?view=rest-keyvault-keys-7.4)  
Base API URI: ```{vaultBaseUrl}```

## List
| Operation | Method | URI |
| :------- | :------- | :------- |
| List Keys | GET | {vaultBaseUrl}/keys?api-version=7.4 |
| List Keys with maxResults | GET | {vaultBaseUrl}/keys?maxresults={maxresults}&api-version=7.4 |

## Get
| Operation | Method | URI |
| :------- | :------- | :------- |
| Get Key | GET | {vaultBaseUrl}/keys/{key-name}/{key-version}?api-version=7.4 |
| Get Key Versions | GET | {vaultBaseUrl}/keys/{key-name}/versions?api-version=7.4 |
| Get Key Rotation Policy | GET | GET {vaultBaseUrl}/keys/{key-name}/rotationpolicy?api-version=7.4 |
| Get Deleted Key | GET | {vaultBaseUrl}/deletedkeys/{key-name}?api-version=7.4 |

## Recover
| Operation | Method | URI |
| :------- | :------- | :------- |
| Recover Deleted Key | POST | {vaultBaseUrl}/deletedkeys/{key-name}/recover?api-version=7.4 |
