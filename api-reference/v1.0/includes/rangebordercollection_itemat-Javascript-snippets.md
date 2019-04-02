
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const borders = {
  index: 1
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/format/borders/itemAt')
		.post({workbookRangeBorder : borders});
	console.log(res);
} catch (error) {
	throw error;
}

```