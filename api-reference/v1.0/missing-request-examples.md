---
title: "Define the /me as singleton"
description: "These are things I had to add in the docs to make sure the Markdown-Scanner"
localization_priority: Normal
---

# Helpers (examples that aren't included in the docs)

These are things I had to add in the docs to make sure the Markdown-Scanner
tool was able to properly handle the Graph docs.


## Define the /me as singleton

<!-- {"blockType": "request", "name": "get_current_user" } -->
```http
GET https://graph.microsoft.com/v1.0/me
```

<!-- {"blockType": "response", "@odata.type": "microsoft.graph.user", truncated: true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```
#### Sample Code
# [C#](#tab/CS)
[!INCLUDE [Sample Code]( ../includes/get_current_user-C#-snippets.md)]

# [Javascript](#tab/Javascript)
[!INCLUDE [Sample Code]( ../includes/get_current_user-Javascript-snippets.md)]

---



## Define drives as an queryable entityset
<!-- {"blockType": "request", "name": "get_drive_from_id" } -->
```http
GET https://graph.microsoft.com/v1.0/drives/{drive-id}
```

<!-- {"blockType": "response", "@odata.type": "microsoft.graph.drive", truncated: true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```
#### Sample Code
# [C#](#tab/CS)
[!INCLUDE [Sample Code]( ../includes/get_drive_from_id-C#-snippets.md)]

# [Javascript](#tab/Javascript)
[!INCLUDE [Sample Code]( ../includes/get_drive_from_id-Javascript-snippets.md)]

---



## define users as an queryable entityset

<!-- {"blockType": "request", "name": "get_users" } -->
```http
GET https://graph.microsoft.com/v1.0/users/{user-id}
```

<!-- {"blockType": "response", "@odata.type": "microsoft.graph.user", truncated: true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```
