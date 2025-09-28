# Vault Certificates Endpoints
Resource: [Vault Certificates](https://learn.microsoft.com/en-us/rest/api/keyvault/certificates/operation-groups?view=rest-keyvault-certificates-7.4)
Base API URI: ```{vaultBaseUrl}```

## List
| Operation | Method | URI |
| :------- | :------- | :------- |
| List Certificates | GET | {vaultBaseUrl}/certificates?api-version=7.4 |
| List Deleted Certificates | GET | {vaultBaseUrl}/deletedcertificates?api-version=7.4 |

## Get
| Operation | Method | URI |
| :------- | :------- | :------- |
| Get Certificate | GET | {vaultBaseUrl}/certificates/{certificate-name}/{certificate-version}?api-version=7.4 |
| Get Certificate Versions | GET | {vaultBaseUrl}/certificates/{certificate-name}/versions?api-version=7.4 |

## Recover
| Operation | Method | URI |
| :------- | :------- | :------- |
| Recover Deleted Certificate | POST | {vaultBaseUrl}/deletedcertificates/{certificate-name}/recover?api-version=7.4 |