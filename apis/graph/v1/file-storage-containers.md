# Storage Endpoints

Base URI: ```https://graph.microsoft.com/v1.0/```

## List File Storage Containers
| Method   | URI |
| :------- | :------- |
| GET | /storage/fileStorage/containers?$filter=containerTypeId eq {containerTypeId} |
| GET | /storage/fileStorage/containers?$filter=containerTypeId eq {containerTypeId} and viewpoint/effectiveRole eq 'principalOwner' |

### Query Parameters
This method requires the containerTypeId parameter. It supports the $expand OData query parameter, except for the drive, permissions, and customProperties properties. If other $filter conditions are used, the endpoint might return intermediate pages with partial results or even no results, and the caller must continue to read all pages to get all applicable results. 

## Get File Storage Container
| Method   | URI |
| :------- | :------- |
| GET | /storage/fileStorage/containers/{containerId} |

[MS Graph: Get fileStorageContainer](https://learn.microsoft.com/en-us/graph/api/filestoragecontainer-get?view=graph-rest-1.0&tabs=http)

## List File Storage Container Permissions
| Method   | URI |
| :------- | :------- |
| GET | /storage/fileStorage/containers/{containerId}/permissions |

[MS Graph: List fileStorageContainer permissions](https://learn.microsoft.com/en-us/graph/api/filestoragecontainer-list-permissions?view=graph-rest-1.0&tabs=http)
