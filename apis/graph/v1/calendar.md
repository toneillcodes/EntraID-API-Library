# Calendar Endpoints

Resource: [calendar resource type](https://learn.microsoft.com/en-us/graph/api/resources/calendar?view=graph-rest-1.0)  
Resource: [calendar group resource type](https://learn.microsoft.com/en-us/graph/api/resources/calendargroup?view=graph-rest-1.0)
Base URI: ```https://graph.microsoft.com/v1.0/```

## List
Note: Returns all of the user's calendars.
| Method   | URI |
| :------- | :------- |
| GET | /me/calendars |
| GET | /users/{id \| userPrincipalName}/calendars |

## List Calendars in a Specific 'calendarGroup'
| Method   | URI |
| :------- | :------- |
| GET | /me/calendarGroups/{calendar_group_id}/calendars |
| GET | /users/{id \| userPrincipalName}/calendarGroups/{calendar_group_id}/calendars |

### Query Parameters
This method supports the [OData query parameters](https://learn.microsoft.com/en-us/graph/query-parameters?tabs=http#odata-system-query-options) to help customize the response.

### References
[MS Graph: Calendar List](https://learn.microsoft.com/en-us/graph/api/user-list-calendars?view=graph-rest-1.0&tabs=http)  
[MS Graph: OData Query parameters](https://learn.microsoft.com/en-us/graph/query-parameters?tabs=http#odata-system-query-options)

## Get
Note: Returns a user or group's default calendar
| Method   | URI |
| :------- | :------- |
| GET | /me/calendar |
| GET | /users/{id \| userPrincipalName}/calendar |
| GET | /groups/{id}/calendar |

## Get Calender in Default 'calendarGroup'
| Method   | URI |
| :------- | :------- |
| GET | /me/calendars/{id} |
| GET | /users/{id \| userPrincipalName}/calendars/{id} |

## Get Calendar in a Specific 'calendarGroup'
| Method   | URI |
| :------- | :------- |
| GET | /me/calendarGroups/{id}/calendars/{id} |
| GET | /users/{id \| userPrincipalName}/calendarGroups/{id}/calendars/{id} |

### Query Parameters
This method supports the [OData query parameters](https://learn.microsoft.com/en-us/graph/query-parameters?tabs=http#odata-system-query-options) to help customize the response.

[MS Graph: User Get](https://learn.microsoft.com/en-us/graph/api/calendar-get?view=graph-rest-1.0&tabs=http)  
[MS Graph: OData Query parameters](https://learn.microsoft.com/en-us/graph/query-parameters?tabs=http#odata-system-query-options)

## Update
| Method   | URI |
| :------- | :------- |
| PATCH | /me/calendar |
| PATCH | /users/{id \| userPrincipalName}/calendar |
| PATCH | /groups/{id}/calendar |

| Method   | URI |
| :------- | :------- |
| PATCH | /me/calendars/{id} |
| PATCH | /users/{id \| userPrincipalName}/calendars/{id} |

| Method   | URI |
| :------- | :------- |
| PATCH | /me/calendarGroups/{id}/calendars/{id} |
| PATCH | /users/{id \| userPrincipalName}/calendarGroups/{id}/calendars/{id} |

### Request Body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.
| Property | Type | Description |
|----|----|----|
| color	| String |Specifies the color theme to distinguish the calendar from other calendars in a UI. The property values are: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1 |
| isDefaultCalendar	| Boolean | True if this calendar is the user's default calendar, false otherwise. |
| name | String | The calendar name. |
[MS Graph: Calendar Update - Request Body](https://learn.microsoft.com/en-us/graph/api/calendar-update?view=graph-rest-1.0&tabs=http#request-body)

### Response
If successful, this method returns a 200 OK response code and updated calendar object in the response body.

## Delete
| Method   | URI |
| :------- | :------- |
| DELETE | /me/calendars/{id} |
| DELETE | /users/{id \| userPrincipalName}/calendars/{id} |

### Response
If successful, this action returns a 204 No Content response code.

## Permanently Delete
| Method   | URI |
| :------- | :------- |
| POST | /users/{usersId}/calendar/permanentDelete |
| POST | /groups/{groupsId}/calendar/permanentDelete |

### Response
If successful, this action returns a 204 No Content response code.

## List Events
| Method   | URI |
| :------- | :------- |
| GET | /me/calendar/events |
| GET | /users/{id \| userPrincipalName}/calendar/events |
| GET | /groups/{id}/calendar/events |

| Method   | URI |
| :------- | :------- |
| GET | /me/calendars/{id}/events |
| GET | /users/{id \| userPrincipalName}/calendars/{id}/events |

| Method   | URI |
| :------- | :------- |
| GET | /me/calendarGroups/{id}/calendars/{id}/events |
| GET | /users/{id \| userPrincipalName}/calendarGroups/{id}/calendars/{id}/events |

### Query Parameters
This method supports the [OData query parameters](https://learn.microsoft.com/en-us/graph/query-parameters?tabs=http#odata-system-query-options) to help customize the response.

### Response
If successful, this action returns a 204 No Content response code.

## Create Event
| Method   | URI |
| :------- | :------- |
| POST | /me/calendar/events |
| POST | /users/{id \| userPrincipalName}/calendar/events |
| POST | /groups/{id}/calendar/events |

## Create Event in the Default Calendar Group
| Method   | URI |
| :------- | :------- |
| POST | /me/calendars/{id}/events |
| POST | /users/{id \| userPrincipalName}/calendars/{id}/events |

## Create Event in a Specific Calendar Group
| Method   | URI |
| :------- | :------- |
| POST | /me/calendarGroups/{id}/calendars/{id}/events |
| POST | /users/{id \| userPrincipalName}/calendarGroups/{id}/calendars/{id}/events |

### Request Body
The request body should contain a JSON representation of the event formatted as an [event resource type](https://learn.microsoft.com/en-us/graph/api/resources/event?view=graph-rest-1.0). An example can be found [here](https://learn.microsoft.com/en-us/graph/api/resources/event?view=graph-rest-1.0#json-representation).

### Response
If successful, this method returns 201 Created response code and [event resource object](https://learn.microsoft.com/en-us/graph/api/resources/event?view=graph-rest-1.0) in the response body.