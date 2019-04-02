
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const fill = {
  color: "#00FF00"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$B$1')/format/fill')
		.update({workbookRangeFill : fill});
	console.log(res);
} catch (error) {
	throw error;
}

```