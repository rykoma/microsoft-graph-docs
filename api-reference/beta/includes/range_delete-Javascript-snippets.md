
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const delete = {
  shift: "shift-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/names('name')/range/delete')
	.version('beta')
	.post({String : delete});

```