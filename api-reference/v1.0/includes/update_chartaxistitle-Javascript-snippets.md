
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const title = {
  text: "text-value",
  visible: true
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/title')
		.update({workbookChartAxisTitle : title});
	console.log(res);
} catch (error) {
	throw error;
}

```