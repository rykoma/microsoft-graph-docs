
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const setData = {
  sourceData: "sourceData-value",
  seriesBy: "seriesBy-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/setData')
		.post({Json : setData});
	console.log(res);
} catch (error) {
	throw error;
}

```