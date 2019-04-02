
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const fill = {
  color: "#FF0000"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$A$1')/format/fill')
		.update({workbookRangeFill : fill});
	console.log(res);
} catch (error) {
	throw error;
}

```