
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const series = {
  index: 2
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/itemAt')
	.post({workbookChartSeries : series});

```