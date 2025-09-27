# Recycle Bin

Base URI: ```https://graph.microsoft.com/v1.0/```

## List items
| Method   | URI |
| :------- | :------- |
| GET | /storage/fileStorage/containers/{containerId}/recycleBin/items |

### Query Parameters
This method supports the $select and $top OData query parameters to customize the response.

[MS Graph: Recycle Bin List items](https://learn.microsoft.com/en-us/graph/api/recyclebin-list-items?view=graph-rest-1.0&tabs=http)

## Restore Item
| Method   | URI |
| :------- | :------- |
| POST | /storage/fileStorage/containers/{containerId}/recycleBin/items/restore |

### Request Headers
| Method   | URI |
| :------- | :------- |
| Content-Type	| application/json |

### Example Request
```
POST  https://graph.microsoft.com/v1.0/storage/fileStorage/containers/b!ISJs1WRro0y0EWgkUYcktDa0mE8zSlFEqFzqRn70Zwp1CEtDEBZgQICPkRbil_5Z/recycleBin/items/restore
Content-Type: application/json

{
  "ids": ["5d625d33-338c-4a77-a98a-3e287116440c", "73133853-48f2-4956-bc4a-03f8d1675042"]
}
```

### Example Response
```
HTTP/1.1 207 Multi-Status
Content-Type: application/json

{
  "value": [
    {
      "id": "5d625d33-338c-4a77-a98a-3e287116440c"
    },
    {
      "id": "73133853-48f2-4956-bc4a-03f8d1675042"
    }
  ]
}
```
