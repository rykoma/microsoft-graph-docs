
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const copyToNotebook = {
  id: "id-value",
  groupId: "groupId-value",
  renameAs: "renameAs-value"
};

let res = await client.api('/me/onenote/sections/{id}/copyToNotebook')
	.post({String : copyToNotebook});

```