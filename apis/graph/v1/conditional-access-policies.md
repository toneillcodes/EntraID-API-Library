# Conditional Access Policy Endpoints

Base URI: ```https://graph.microsoft.com/v1.0/```

## List policies
| Method   | URI |
| :------- | :------- |
| GET | /identity/conditionalAccess/policies |

### Query Parameters
This method supports the $skip, $top, $count, $filter, $orderby, and $select OData query parameters to help customize the response. 

### Example Response
```
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#conditionalAccess/policies",
    "value": [
        {
            "id": "2b31ac51-b855-40a5-a986-0a4ed23e9008",
            "templateId": null,
            "displayName": "CA001: Require multi-factor authentication for admins",
            "createdDateTime": "2021-11-02T14:17:09.1686157Z",
            "modifiedDateTime": "2024-01-03T20:07:59.0369305Z",
            "state": "enabled",
            "sessionControls": null,
            "conditions": {
                "userRiskLevels": [],
                "signInRiskLevels": [],
                "clientAppTypes": [
                    "all"
                ],
                "servicePrincipalRiskLevels": [],
                "insiderRiskLevels": null,
                "platforms": null,
                "locations": null,
                "devices": null,
                "clientApplications": null,
                "applications": {
                    "includeApplications": [
                        "All"
                    ],
                    "excludeApplications": [],
                    "includeUserActions": [],
                    "includeAuthenticationContextClassReferences": [],
                    "applicationFilter": null
                },
                "users": {
                    "includeUsers": [],
                    "excludeUsers": [],
                    "includeGroups": [],
                    "excludeGroups": [
                        "eedad040-3722-4bcb-bde5-bc7c857f4983"
                    ],
                    "includeRoles": [
                        "62e90394-69f5-4237-9190-012177145e10",
                        "194ae4cb-b126-40b2-bd5b-6091b380977d",
                        "f28a1f50-f6e7-4571-818b-6a12f2af6b6c",
                        "29232cdf-9323-42fd-ade2-1d097af3e4de",
                        "b1be1c3e-b65d-4f19-8427-f6fa0d97feb9",
                        "729827e3-9c14-49f7-bb1b-9608f156bbb8",
                        "b0f54661-2d74-4c50-afa3-1ec803f12efe",
                        "fe930be7-5e62-47db-91af-98c3a49a38b1",
                        "c4e39bd9-1100-46d3-8c65-fb160da0071f",
                        "9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3",
                        "158c047a-c907-4556-b7ef-446551a6b5f7",
                        "966707d0-3269-4727-9be2-8c3a10f19b9d",
                        "7be44c8a-adaf-4e2a-84d6-ab2649e08a13",
                        "e8611ab8-c189-46e8-94e1-60213ab1f814",
                        "f2ef992c-3afb-46b9-b7cf-a126ee74c451"
                    ],
                    "excludeRoles": [],
                    "includeGuestsOrExternalUsers": null,
                    "excludeGuestsOrExternalUsers": null
                }
            },
            "grantControls": {
                "operator": "OR",
                "builtInControls": [
                    "mfa"
                ],
                "customAuthenticationFactors": [],
                "termsOfUse": [],
                "authenticationStrength@odata.context": "https://graph.microsoft.com/v1.0/$metadata#policies/conditionalAccessPolicies('2b31ac51-b855-40a5-a986-0a4ed23e9008')/grantControls/authenticationStrength/$entity",
                "authenticationStrength": null
            }
        },
        {
            "id": "10ef4fe6-5e51-4f5e-b5a2-8fed19d0be67",
            "templateId": null,
            "displayName": "CA008: Require password change for high-risk users",
            "createdDateTime": "2021-11-02T14:26:29.1005248Z",
            "modifiedDateTime": "2024-01-30T23:11:08.549481Z",
            "state": "enabled",
            "conditions": {
                "userRiskLevels": [
                    "high"
                ],
                "signInRiskLevels": [],
                "clientAppTypes": [
                    "all"
                ],
                "servicePrincipalRiskLevels": [],
                "insiderRiskLevels": null,
                "platforms": null,
                "locations": null,
                "devices": null,
                "clientApplications": null,
                "applications": {
                    "includeApplications": [
                        "All"
                    ],
                    "excludeApplications": [],
                    "includeUserActions": [],
                    "includeAuthenticationContextClassReferences": [],
                    "applicationFilter": null
                },
                "users": {
                    "includeUsers": [
                        "All"
                    ],
                    "excludeUsers": [],
                    "includeGroups": [],
                    "excludeGroups": [
                        "eedad040-3722-4bcb-bde5-bc7c857f4983"
                    ],
                    "includeRoles": [],
                    "excludeRoles": [],
                    "includeGuestsOrExternalUsers": null,
                    "excludeGuestsOrExternalUsers": null
                }
            },
            "grantControls": {
                "operator": "AND",
                "builtInControls": [
                    "passwordChange"
                ],
                "customAuthenticationFactors": [],
                "termsOfUse": [],
                "authenticationStrength@odata.context": "https://graph.microsoft.com/v1.0/$metadata#policies/conditionalAccessPolicies('10ef4fe6-5e51-4f5e-b5a2-8fed19d0be67')/grantControls/authenticationStrength/$entity",
                "authenticationStrength": {
                    "id": "00000000-0000-0000-0000-000000000002",
                    "createdDateTime": "2021-12-01T08:00:00Z",
                    "modifiedDateTime": "2021-12-01T08:00:00Z",
                    "displayName": "Multifactor authentication",
                    "description": "Combinations of methods that satisfy strong authentication, such as a password + SMS",
                    "policyType": "builtIn",
                    "requirementsSatisfied": "mfa",
                    "allowedCombinations": [
                        "windowsHelloForBusiness",
                        "fido2",
                        "x509CertificateMultiFactor",
                        "deviceBasedPush",
                        "temporaryAccessPassOneTime",
                        "temporaryAccessPassMultiUse",
                        "password,microsoftAuthenticatorPush",
                        "password,softwareOath",
                        "password,hardwareOath",
                        "password,sms",
                        "password,voice",
                        "federatedMultiFactor",
                        "microsoftAuthenticatorPush,federatedSingleFactor",
                        "softwareOath,federatedSingleFactor",
                        "hardwareOath,federatedSingleFactor",
                        "sms,federatedSingleFactor",
                        "voice,federatedSingleFactor"
                    ],
                    "combinationConfigurations@odata.context": "https://graph.microsoft.com/v1.0/$metadata#policies/conditionalAccessPolicies('10ef4fe6-5e51-4f5e-b5a2-8fed19d0be67')/grantControls/authenticationStrength/combinationConfigurations",
                    "combinationConfigurations": []
                }
            },
            "sessionControls": {
                "disableResilienceDefaults": null,
                "applicationEnforcedRestrictions": null,
                "cloudAppSecurity": null,
                "persistentBrowser": null,
                "signInFrequency": {
                    "value": null,
                    "type": null,
                    "authenticationType": "primaryAndSecondaryAuthentication",
                    "frequencyInterval": "everyTime",
                    "isEnabled": true
                }
            }
        }
    ]
}
```
Source: [MS Graph: Conditional Access Policies List Response](https://learn.microsoft.com/en-us/graph/api/conditionalaccessroot-list-policies?view=graph-rest-1.0&tabs=http#response-1)
