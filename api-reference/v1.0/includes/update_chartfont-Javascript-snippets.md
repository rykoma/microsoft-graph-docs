
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const font = {
  bold: true,
  color: "color-value",
  italic: true,
  name: "name-value",
  size: 99,
  underline: "underline-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/format/font')
		.update({workbookChartFont : font});
	console.log(res);
} catch (error) {
	throw error;
}

```