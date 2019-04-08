---
title: "Create event"
description: "Use this API to create a new event."
author: "dkershaw10"
localization_priority: Priority
ms.prod: "groups"
---

# Create event
Use this API to create a new [event](../resources/event.md).

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
POST /groups/{id}/events
POST /groups/{id}/calendar/events
```

## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body
In the request body, supply a JSON representation of [event](../resources/event.md) object.

## Response
If successful, this method returns `201 Created` response code and [event](../resources/event.md) object in the response body.

## Example
#### Request
The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_event_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/events
Prefer: outlook.timezone="Pacific Standard Time"
Content-type: application/json

{
  "subject": "Team meeting",
  "body": {
    "contentType": "HTML",
    "content": "Monthly team meeting."
  },
  "start": {
      "dateTime": "2019-04-09T12:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2019-04-09T14:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "location":{
      "displayName":"Conf Room 1"
  },
  "attendees": []
}
```
In the request body, supply a JSON representation of [event](../resources/event.md) object.

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
	"@odata.etag":"W/"P8tzXbof6Eyv1DvnV4lZKgAAAAAOew=="",
	"id":"AQMkADYyYzE3OTI2LWEwYWYtNDUyNy04MzY3LTg1ZjY2AGI5MDc2MWMARgAAA6N59kpn6OZEoMnfCg9P4B8HAD-Lc126H_hMr9Q751eJWSoAAAIBDQAAAD-Lc126H_hMr9Q751eJWSoAAAIU-QAAAA==",
	"createdDateTime":"2019-04-08T01:50:27.9655729Z",
	"lastModifiedDateTime":"2019-04-08T01:50:31.163825Z",
	"changeKey":"P8tzXbof6Eyv1DvnV4lZKgAAAAAOew=="
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
