
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const createSession = {
  persistChanges: true
};

let res = await client.api('/me/drive/items/{id}/workbook/createSession')
	.version('beta')
	.post({workbook : createSession});

```