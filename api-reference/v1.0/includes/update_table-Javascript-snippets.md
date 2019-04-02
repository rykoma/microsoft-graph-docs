
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const tables = {
  name: "name-value",
  showHeaders: true,
  showTotals: true,
  style: "style-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}')
		.update({workbookTable : tables});
	console.log(res);
} catch (error) {
	throw error;
}

```