# People Endpoints
Description: Retrieve a collection of person objects ordered by their relevance to the user, which is determined by the user's communication and collaboration patterns, and business relationships.  

Base URI: ```https://graph.microsoft.com/v1.0/```

## List
| Method   | URI |
| :------- | :------- |
| GET      | /me/people    |
| GET      | /users/{id \| userPrincipalName}/people |

[MS Graph: List people](https://learn.microsoft.com/en-us/graph/api/user-list-people?view=graph-rest-1.0&tabs=http)

## Authorization
- People.Read - Use to make general people API calls; for example, https://graph.microsoft.com/v1.0/me/people/. People.Read requires end user consent.
- People.Read.All - Required to retrieve the people most relevant to a specified user in the signed-in user’s organization (https://graph.microsoft.com/v1.0/users/{id}/people) calls. People.Read.All requires admin consent.

[MS Graph: People Insights Authorization](https://learn.microsoft.com/en-us/graph/people-insights-overview#authorization)
