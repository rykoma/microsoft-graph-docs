
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const columns = {
  index: {
  }
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/columns/ItemAt')
		.version('beta')
		.post({workbookTableColumn : columns});
	console.log(res);
} catch (error) {
	throw error;
}

```