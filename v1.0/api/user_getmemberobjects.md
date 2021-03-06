# user: getMemberObjects
Return all of the groups and directory roles that the user is a member of. The check is transitive.

### Prerequisites
One of the following **scopes** is required to execute this API: 
*User.Read; User.ReadWrite; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /users/<objectId>/Microsoft.Graph.getMemberObjects
POST /users/<userPrincipalName>/Microsoft.Graph.getMemberObjects
```
### Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer %token%  |
| Content-Type  | application/json  |

### Request body
In the request body, provide a JSON object with the following parameters.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|securityEnabledOnly|Boolean|**true** to specify that only security groups that the user is a member of should be returned; **false** to specify that all groups and directory roles that the user is a member of should be returned. Note: The function can only be called on a user if the parameter is **true**.|

### Response
If successful, this method returns `200, OK` response code and String collection in the response body that contains the IDs of the groups and directory roles that the user is a member of.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "user_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/users/<objectId>/Microsoft.Graph.getMemberObjects
Content-type: application/json

{
  "securityEnabledOnly": true
}
```

##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    "f46e3e1f-17f3-4801-8a39-b2ccc58eb6be",
    "63243e64-228a-433b-a98a-aa8c832af7fe",
    "f5480dfd-7d77-4d0b-ba2e-3391953cc74a"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->