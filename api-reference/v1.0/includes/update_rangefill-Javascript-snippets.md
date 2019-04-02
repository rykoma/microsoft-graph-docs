
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const fill = {
  color: "color-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/format/fill')
		.update({workbookRangeFill : fill});
	console.log(res);
} catch (error) {
	throw error;
}

```