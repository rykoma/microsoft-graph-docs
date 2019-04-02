
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const columns = {
  name: "name-value",
  index: 99,
  values: "values-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}')
		.version('beta')
		.update({workbookTableColumn : columns});
	console.log(res);
} catch (error) {
	throw error;
}

```