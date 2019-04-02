
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const add = {
  type: "ColumnStacked",
  sourceData: "A1:B1",
  seriesBy: "Auto"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/add')
		.version('beta')
		.post({String : add});
	console.log(res);
} catch (error) {
	throw error;
}

```