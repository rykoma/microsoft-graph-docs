
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const add = {
  index: {
  },
  values: [
    {
    }
  ]
};

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/columns/add')
	.version('beta')
	.post({Int32 : add});

```