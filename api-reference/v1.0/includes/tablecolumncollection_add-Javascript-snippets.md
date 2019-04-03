
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const add = {
  index: 3,
  values: [
    {
    }
  ]
};

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/columns/add')
	.post({Int32 : add});

```