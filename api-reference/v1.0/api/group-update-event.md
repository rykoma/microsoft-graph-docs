---
title: "Update event"
description: "Update an event object."
author: "dkershaw10"
localization_priority: Normal
ms.prod: "groups"
---

# Update event
Update an [event](../resources/event.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Group.ReadWrite.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Not supported. |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/events/{id}
PATCH /groups/{id}/calendar/events/{id}
```

## Request headers
| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  | string  | Bearer {token}. Required. |

## Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

## Response
If successful, this method returns a `204 No Content` response code.

## Example
#### Request
The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "update_group_event"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groups/{id}/events/{id}
Prefer: outlook.timezone="Pacific Standard Time"
Content-type: application/json

{
  "location":{
      "displayName":"Conf Room 2"
  }
}
```

#### Response
The following is an example of the response.
>**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
	"@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups('7fe8323e-1b24-406c-924c-9d9ccf2bc13d')/events/$entity",
	"@odata.etag":"W/"P8tzXbof6Eyv1DvnV4lZKgAAAAAOoQ=="",
	"id":"AQMkADYyYzE3OTI2LWEwYWYtNDUyNy04MzY3LTg1ZjY2AGI5MDc2MWMARgAAA6N59kpn6OZEoMnfCg9P4B8HAD-Lc126H_hMr9Q751eJWSoAAAIBDQAAAD-Lc126H_hMr9Q751eJWSoAAAIU-QAAAA==",
	"createdDateTime":"2019-04-08T01:50:27.9655729Z",
	"lastModifiedDateTime":"2019-04-08T02:19:02.8127975Z",
	"changeKey":"P8tzXbof6Eyv1DvnV4lZKgAAAAAOoQ=="
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
