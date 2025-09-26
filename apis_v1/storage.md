# Storage Endpoints
## List File Storage Containers
| Method   | URI |
| :------- | :------- |
| GET | /storage/fileStorage/containers?$filter=containerTypeId eq {containerTypeId} |
| GET | /storage/fileStorage/containers?$filter=containerTypeId eq {containerTypeId} and viewpoint/effectiveRole eq 'principalOwner' |

### Query Parameters
This method requires the containerTypeId parameter. It supports the $expand OData query parameter, except for the drive, permissions, and customProperties properties. If other $filter conditions are used, the endpoint might return intermediate pages with partial results or even no results, and the caller must continue to read all pages to get all applicable results. 
