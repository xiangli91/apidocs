# List plans

Retrieve a list of plan objects shared with the user.
### Prerequisites
The following **scopes** are required to execute this API: 

Group.ReadWrite.All AND Tasks.ReadWrite

### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /users/<objectId>/plans
```
### Optional query parameters
None

### Request headers
| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  | string  | Value should be set to "Bearer (access-token)" |

### Request body
Do not supply a request body for this method.
### Response
If successful, this method returns a `200 OK` response code and collection of [plan](../resources/plan.md) objects in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_plans"
}-->
```http
GET https://graph.microsoft.com/beta/users/<objectId>/plans
```
##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.plan",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 153

{
  "value": [
    {
      "createdBy": "createdBy-value",
      "owner": "owner-value",
      "title": "title-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List plans",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->