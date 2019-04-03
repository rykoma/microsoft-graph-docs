
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const add = {
  name: "name-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/add')
	.version('beta')
	.post({String : add});

```