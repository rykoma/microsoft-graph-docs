
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const series = {
  name: "name-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series')
		.post({workbookChartSeries : series});
	console.log(res);
} catch (error) {
	throw error;
}

```