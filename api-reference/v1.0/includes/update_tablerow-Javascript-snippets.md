
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const rows = {
  index: 99,
  values: "values-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/rows/{index}')
		.update({workbookTableRow : rows});
	console.log(res);
} catch (error) {
	throw error;
}

```