
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const add = {
  type: "ColumnStacked",
  sourceData: "A1:B1",
  seriesBy: "Auto"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/add')
	.version('beta')
	.post({String : add});

```