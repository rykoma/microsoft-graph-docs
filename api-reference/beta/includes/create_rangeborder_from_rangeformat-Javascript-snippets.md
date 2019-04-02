
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const borders = {
  id: "id-value",
  color: "color-value",
  style: "style-value",
  sideIndex: "sideIndex-value",
  weight: "weight-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names('name')/range/format/borders')
		.version('beta')
		.post({workbookRangeBorder : borders});
	console.log(res);
} catch (error) {
	throw error;
}

```