
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const insert = {
  shift: "shift-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/names('name')/range/insert')
	.version('beta')
	.post({String : insert});

```