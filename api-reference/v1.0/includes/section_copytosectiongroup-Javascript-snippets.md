
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const copyToSectionGroup = {
  id: "id-value",
  groupId: "groupId-value",
  renameAs: "renameAs-value"
};

let res = await client.api('/me/onenote/sections/{id}/copyToSectionGroup')
	.post({String : copyToSectionGroup});

```