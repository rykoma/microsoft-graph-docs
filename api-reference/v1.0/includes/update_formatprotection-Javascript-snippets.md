
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const protection = {
  locked: true,
  formulaHidden: true
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/format/protection')
		.update({workbookFormatProtection : protection});
	console.log(res);
} catch (error) {
	throw error;
}

```