
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const rows = {
  index: {
  }
};

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/rows/ItemAt')
	.version('beta')
	.post({workbookTableRow : rows});

```