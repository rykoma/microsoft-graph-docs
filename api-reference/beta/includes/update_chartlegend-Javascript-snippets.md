
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const legend = {
  visible: true,
  position: "position-value",
  overlay: true
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts('name')/legend')
		.version('beta')
		.update({workbookChartLegend : legend});
	console.log(res);
} catch (error) {
	throw error;
}

```