
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const add = {
  address: "A1:D8",
  hasHeaders: false
};

let res = await client.api('/me/drive/items/{id}/workbook/tables/$/add')
	.version('beta')
	.post({String : add});

```