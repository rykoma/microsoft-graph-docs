
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const add = {
  address: "",
  hasHeaders: false
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/tables/$/add')
	.version('beta')
	.post({String : add});

```