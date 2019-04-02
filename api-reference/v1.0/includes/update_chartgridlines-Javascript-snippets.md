
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const minorGridlines = {
  visible: true
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/minorGridlines')
		.update({workbookChartGridlines : minorGridlines});
	console.log(res);
} catch (error) {
	throw error;
}

```