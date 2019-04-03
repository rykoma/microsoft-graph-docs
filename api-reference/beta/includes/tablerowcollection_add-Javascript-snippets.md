
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const add = {
  index: null,
  values: [
    [1, 2, 3],
    [4, 5, 6]
  ]
};

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/rows/add')
	.version('beta')
	.post({Int32 : add});

```