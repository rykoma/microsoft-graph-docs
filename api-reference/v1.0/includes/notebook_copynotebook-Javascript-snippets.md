
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const copyNotebook = {
  groupId: "groupId-value",
  renameAs: "renameAs-value"
};

let res = await client.api('/me/onenote/notebooks/{id}/copyNotebook')
	.post({String : copyNotebook});

```