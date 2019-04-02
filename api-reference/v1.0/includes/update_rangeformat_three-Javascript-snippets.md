
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const format = {
  columnWidth: 135,
  horizontalAlignment: "Right",
  verticalAlignment: "Top",
  rowHeight: 49,
  wrapText: false
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$C$1')/format')
		.update({workbookRangeFormat : format});
	console.log(res);
} catch (error) {
	throw error;
}

```