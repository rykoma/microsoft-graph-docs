
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const setSolidColor = {
  color: "color-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts('name')/format/fill/setSolidColor')
		.version('beta')
		.post({String : setSolidColor});
	console.log(res);
} catch (error) {
	throw error;
}

```