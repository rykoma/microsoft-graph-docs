
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const font = {
  underline: "Single",
  color: "#FFFFFF",
  size: 26
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$C$1')/format/font')
		.update({workbookRangeFont : font});
	console.log(res);
} catch (error) {
	throw error;
}

```