# Vault Secrets Endpoints
Resource: [Vault Secrets](https://learn.microsoft.com/en-us/rest/api/keyvault/secrets/operation-groups?view=rest-keyvault-secrets-7.4)
Base API URI: ```{vaultBaseUrl}```

## List
| Operation | Method | URI |
| :------- | :------- | :------- |
| List Secrets | GET | {vaultBaseUrl}/secrets?api-version=7.4 |
| List Deleted Secrets | GET | {vaultBaseUrl}/deletedsecrets?api-version=7.4 |

## Get
| Operation | Method | URI |
| :------- | :------- | :------- |
| Get Secret | GET | {vaultBaseUrl}/secrets/{secret-name}/{secret-version}?api-version=7.4 |
| Get Secret Versions | GET | {vaultBaseUrl}/secrets/{secret-name}/versions?api-version=7.4 |

## Recover
| Operation | Method | URI |
| :------- | :------- | :------- |
| Recover Deleted Secret | POST | {vaultBaseUrl}/deletedsecrets/{secret-name}/recover?api-version=7.4 |
