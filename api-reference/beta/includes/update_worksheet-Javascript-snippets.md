
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const worksheets = {
  position: 99,
  name: "name-value",
  visibility: "visibility-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}')
		.version('beta')
		.update({workbookWorksheet : worksheets});
	console.log(res);
} catch (error) {
	throw error;
}

```