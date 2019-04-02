
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const points = {
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/{series-id}/points')
		.post({workbookChartPoint : points});
	console.log(res);
} catch (error) {
	throw error;
}

```