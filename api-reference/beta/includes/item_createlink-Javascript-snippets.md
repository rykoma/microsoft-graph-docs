
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const createLink = {
  type: "view",
  scope: "anonymous"
};

let res = await client.api('/me/drive/items/{itemId}/createLink')
	.version('beta')
	.post({String : createLink});

```