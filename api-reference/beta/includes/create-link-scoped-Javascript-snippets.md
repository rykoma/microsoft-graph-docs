
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const createLink = {
  type: "edit",
  scope: "organization"
};

let res = await client.api('/me/drive/items/{item-id}/createLink')
	.version('beta')
	.post({String : createLink});

```