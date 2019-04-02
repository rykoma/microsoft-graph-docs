
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const charts = {
  height: 99,
  left: 99
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts('name')')
		.version('beta')
		.update({workbookChart : charts});
	console.log(res);
} catch (error) {
	throw error;
}

```